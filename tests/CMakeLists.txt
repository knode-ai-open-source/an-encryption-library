# SPDX-FileCopyrightText: 2024-2025 Knode.ai
# SPDX-License-Identifier: Apache-2.0
# Maintainer: Andy Curtis <contactandyc@gmail.com>
cmake_minimum_required(VERSION 3.10)

# Enable testing
enable_testing()

# Define the library to test
set(LIB_TO_TEST an-encryption-library)

# Set the directory for test sources
set(TEST_SOURCES_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
file(GLOB TEST_SOURCES ${TEST_SOURCES_DIR}/*.c)
set(THIRD_PARTY_PACKAGES OpenSSL::Crypto)
find_package(a-cmake-library REQUIRED)

include(BinaryConfig)
