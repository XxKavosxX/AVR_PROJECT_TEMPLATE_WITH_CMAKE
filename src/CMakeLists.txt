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


# "add_avr_library()" its been defined on CMakeLists.txt at ROOT_PATH (AVR_PROJECT_TEMPLARTE/)
# Make a LIB
add_avr_library(LIBS_TO_INCLUDE
                libs/liba.c
                libs/liba.h
                libs/libb.c 
                libs/libb.h)

# Make sure the compiler can find include files for our LIBS_TO_INCLUDE library when other libraries
# or executables link to LIBS_TO_INCLUDE
target_include_directories(LIBS_TO_INCLUDE PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/src")