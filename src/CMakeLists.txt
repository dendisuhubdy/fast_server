include_directories( 
    ${FAST_PUBLISHER_SOURCE_DIR}/include
    ${BOOST_INCLUDE_DIR}
    ${MFAST_INCLUDE_DIR}
)

link_directories(
    ${FAST_PUBLISHER_SOURCE_DIR}/lib
    ${BOOST_LIBRARY_DIR}
    ${MFAST_LIBRARY_DIRS}
)


FASTTYPEGEN_TARGET(MDRefreshSample 
                   MDRefreshSample.xml
)

add_executable (fast_publisher 
                ${FASTTYPEGEN_MDRefreshSample_OUTPUTS} 
                fast_publisher.cpp)

target_link_libraries (fast_publisher 
                    ${MFAST_LIBRARIES}
                    )

