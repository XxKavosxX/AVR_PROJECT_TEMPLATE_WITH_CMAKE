################################################################################
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in all
# copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
# SOFTWARE.
#
# Copyright (c) 2020 Maike Rodrigo
#
###############################################################################


# This command allows us not to specify the full path to the libraries or applications .h file in the main.c executable. 
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../src/libs)

# "add_avr_executable()" its been defined on CMakeLists.txt at ROOT_PATH (AVR_PROJECT_TEMPLARTE/)
# Make main.c a executable
add_avr_executable(MAIN main.c)

# add_target_link_libraries its been defined on CMakeLists.txt at ROOT_PATH (AVR_PROJECT_TEMPLATE/)
# This function will include libraries which has been added by "add_avr_library()" on another CMakeLists.txt
avr_target_link_libraries(MAIN LIBS_TO_INCLUDE)
