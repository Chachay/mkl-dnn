#===============================================================================
# Copyright 2016-2017 Intel Corporation
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#===============================================================================

include_directories(${CMAKE_SOURCE_DIR}/include)

add_executable(simple-net-c simple_net.c)
set_property(TARGET simple-net-c PROPERTY C_STANDARD 99)
target_link_libraries(simple-net-c ${LIB_NAME})
add_test(simple-net-c simple-net-c)

add_executable(simple-net-cpp simple_net.cpp)
set_property(TARGET simple-net-cpp PROPERTY C_STANDARD 99)
target_link_libraries(simple-net-cpp ${LIB_NAME})
add_test(simple-net-cpp simple-net-cpp)

add_test(simple-net-c simple-net-c)
add_test(simple-net-cpp simple-net-cpp)
