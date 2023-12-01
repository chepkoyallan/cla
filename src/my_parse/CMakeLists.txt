# Parser Library
#set(PARSER_SRC_DIR, "${CMAKE_CURRENT_SOURCE_DIR}")
#set(PARSER_DIR "${CMAKE_CURRENT_BINARY_DIR}/parse")
#
#set(LEXER_OUT "${PARSER_DIR}/lexer.c")
#set(PARSER_OUT "${PARSER_DIR}/parser.c")
#
#set(LEXER_LIBRARY_SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/my_lib.cc")
#set(LIBRARY_HEADERS "${CMAKE_CURRENT_SOURCE_DIR}/my_lib.h")


find_package(FLEX 2.6 REQUIRED)
find_package(BISON 2.3 REQUIRED)



flex_target(LEXER "../chem/scan.ll" "${CMAKE_CURRENT_SOURCE_DIR}/parse/scan.cc")
#bison_target(PARSER "${CMAKE_CURRENT_SOURCE_DIR}/parser.y" "${CMAKE_CURRENT_SOURCE_DIR}/parse" DEFINES_FILE "${CMAKE_CURRENT_SOURCE_DIR}/parser.h")

#add_flex_bison_dependency(LEXER)
#add_library(LIBRARY_NAME, STATIC ${FLEX_Scanner_OUTPUTS})


#target_include_directories(${LEXICAL_LIBRARY_NAME} PUBLIC ${LIBRARY_INCLUDES})