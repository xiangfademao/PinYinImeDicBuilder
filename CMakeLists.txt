cmake_minimum_required(VERSION 3.12)
project(PinYinImeDicBuilder)

set(CMAKE_CXX_STANDARD 14)


add_library(jni_pinyinime SHARED
        share/dictbuilder.cpp
        share/dictlist.cpp
        share/dicttrie.cpp
        share/lpicache.cpp
        share/matrixsearch.cpp
        share/mystdlib.cpp
        share/ngram.cpp
        share/pinyinime.cpp
        share/searchutility.cpp
        share/spellingtable.cpp
        share/spellingtrie.cpp
        share/splparser.cpp
        share/userdict.cpp
        share/utf16char.cpp
        share/utf16reader.cpp
        share/sync.cpp)


add_executable(PinYinImeDicBuilder ./command/pinyinime_dictbuilder.cpp  share/dictbuilder.cpp
        share/dictlist.cpp
        share/dicttrie.cpp
        share/lpicache.cpp
        share/matrixsearch.cpp
        share/mystdlib.cpp
        share/ngram.cpp
        share/pinyinime.cpp
        share/searchutility.cpp
        share/spellingtable.cpp
        share/spellingtrie.cpp
        share/splparser.cpp
        share/userdict.cpp
        share/utf16char.cpp
        share/utf16reader.cpp)