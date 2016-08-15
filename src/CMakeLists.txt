# all modules that aren't executables go here
#add_library(bbb-playground SHARED
#           )

# external include directories
include_directories(SYSTEM 
                    )

# libraries to link into the corso_rexarm.so we're creating
#target_link_libraries(bbb-playground
#                      m 
#                      stdc++ 
#                     )
# Following is for code that is for an actual executable
set(EXES 
    hello  
   )

foreach(exe ${EXES})
	add_executable(${exe} ${exe}.cpp)
#	target_link_libraries(${exe} bbb-playground)
endforeach()
