# Adding the library
add_library(myfunc 
                    print_routines.c
)

target_compile_options(myfunc PRIVATE -Wall -O3)
# target_link_libraries(myfunc m) # the other version works also on MacOS
find_package(GSL REQUIRED)
target_link_libraries(myfunc m lapack GSL::gsl GSL::gslcblas)