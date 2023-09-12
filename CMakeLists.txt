cmake_minimum_required(VERSION 3.26)
project(Inheritance_Exercise)

set(CMAKE_CXX_STANDARD 17)

add_executable(Inheritance_Exercise main.cpp
        Account_Util.cpp
        Account_Util.h
        Account.cpp
        Account.h
        Checking_Account.cpp
        Checking_Account.h
        Savings_Account.cpp
        Savings_Account.h
        Trust_Account.cpp
        Trust_Account.h)
