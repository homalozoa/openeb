# Copyright (c) Prophesee S.A.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
# Unless required by applicable law or agreed to in writing, software distributed under the License is distributed
# on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and limitations under the License.

target_sources(metavision_hal_treuzell_protocol_obj PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/tz_camera_discovery.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/tz_libusb_board_command.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/tz_board_data_transfer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/tz_hw_identification.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/tz_control_frame.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/tz_libusb.cpp
)
