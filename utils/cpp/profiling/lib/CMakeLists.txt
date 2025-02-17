# Copyright (c) Prophesee S.A.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
# Unless required by applicable law or agreed to in writing, software distributed under the License is distributed
# on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and limitations under the License.

# Boost::filesystem
find_package(Boost REQUIRED COMPONENTS filesystem system)

# Create shared library for internal profiling tools:
add_library(metavision_utils_profiling STATIC)
add_library(MetavisionUtils::profiling ALIAS metavision_utils_profiling) # Create alias target to refer to

target_include_directories(metavision_utils_profiling
    PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/../include>
)

target_link_libraries(metavision_utils_profiling PUBLIC Boost::filesystem Boost::system)

install(DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/../include/"
        DESTINATION include
        )