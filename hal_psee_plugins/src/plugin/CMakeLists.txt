# Copyright (c) Prophesee S.A.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
# Unless required by applicable law or agreed to in writing, software distributed under the License is distributed
# on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and limitations under the License.

target_sources(metavision_hal_psee_plugin_obj PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_plugin.cpp)

if(TARGET hal_plugin_gen3_fx3)
target_sources(hal_plugin_gen3_fx3 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen3_evk1.cpp)
endif()

if(TARGET hal_plugin_gen31_fx3)
target_sources(hal_plugin_gen31_fx3 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen31_evk1.cpp)
endif()

if(TARGET hal_plugin_gen31_evk2)
target_sources(hal_plugin_gen31_evk2 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen31_evk2.cpp)
endif()

if(TARGET hal_plugin_gen31_evk3)
target_sources(hal_plugin_gen31_evk3 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen31_evk3.cpp)
endif()

if(TARGET hal_plugin_gen4_fx3)
target_sources(hal_plugin_gen4_fx3 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen4_evk1.cpp)
endif()

if(TARGET hal_plugin_gen4_evk2)
target_sources(hal_plugin_gen4_evk2 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen4_evk2.cpp)
endif()

if(TARGET hal_plugin_gen41_evk2)
target_sources(hal_plugin_gen41_evk2 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen41_evk2.cpp)
endif()

if(TARGET hal_plugin_gen41_evk3)
target_sources(hal_plugin_gen41_evk3 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_gen41_evk3.cpp)
endif()

if(TARGET hal_plugin_imx636_evk2)
target_sources(hal_plugin_imx636_evk2 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_imx636_evk2.cpp)
endif()

if(TARGET hal_plugin_imx636_evk3)
target_sources(hal_plugin_imx636_evk3 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_imx636_evk3.cpp)
endif()

if(TARGET hal_plugin_imx636_evk4)
target_sources(hal_plugin_imx636_evk4 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_imx636_evk4.cpp)
endif()

if(TARGET hal_plugin_golden_fallbacks)
    target_sources(hal_plugin_golden_fallbacks PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_golden_fallbacks.cpp)
endif()

if(TARGET hal_plugin_prophesee)
target_sources(hal_plugin_prophesee PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/psee_universal.cpp)
if(HAL_GEN4_SUPPORT)
    target_compile_definitions(hal_plugin_prophesee PRIVATE "HAL_GEN4_SUPPORT")
endif(HAL_GEN4_SUPPORT)
endif()
