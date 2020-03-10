# AVR C PROJECT TEMPLATE USING CMAKE WITH SUBDIRS ORGANIZATION
THIS PROJECT TEMPLATE USE CMAKE WITH THE FOLLOWING STRUCTURE

ROOT-
     |---CMakeLists.txt                                 //Define variables like MCU, F_CPU, BAUD and declare functions:
     |                              q                   //add_avr_library(), avr_target_link_libraries() and add_avr_executable() 
     |
     |---src
     |    |
     |    |---CMakeLists.txt                            //Search libs files and add libs with add_avr_library()
     |    |
     |    '---------------------libs
     |                            |---liba.c
     |                            |---liba.h
     |                            |---libb.c
     |                            '---libb.h
     |
     |---app
     |    |
     |    |---CMakeLists.txt                            //Declare main.c as executable and link declared libraries to it
     |    |
     |    '---main.c
     |
     |
     '---build
          |
          '--{~CMake files}

THE ROOT CMAKE FILES IS BASED ON 
    Igor Mikolic-Torreira 
    https://github.com/igormiktor/cmake-avr-toolchain
