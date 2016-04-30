PROJECT(NAME_OF_PROJECT)

INCLUDE_DIRECTORIES( # the directories of the include files
  /usr/X11R6/include
  /usr/X11R6/include/X11
)

LINK_DIRECTORIES( # the directories of the library files
  /usr/lib
  /usr/local/lib
  /usr/X11R6/lib
)

ADD_EXECUTABLE(
  exe_name        # the name of the executable program   

  src/main.cpp    # the c/c++ files (here I put all my source codes in src directory, and CMakeLists.txt in the src's parent directory)
  src/bspline.cpp
)

TARGET_LINK_LIBRARIES(
  exe_name        # the name of the executable program   

  glut GL GLU     # the library files
)

# Notes: 
# For linux users: you need to install cmake and then type: "cmake CMakelists.txt"  or "cmake ." in order to create Makefile. After that, type: "make" to create the executable program.
# For windows users: you need to install cmake and then create the visual studio project file (.sln) through the CMake's GUI.
