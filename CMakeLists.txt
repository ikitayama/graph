# Copyright (CVERSION 1.41.0) 2008 Michael Jackson
#
# Use, modification and distribution is subject to the Boost Software
# License, Version 1.0. (See accompanying file LICENSE_1_0.txt or copy at
# http://www.boost.org/LICENSE_1_0.txtVERSION 1.41.0)

#----------------------------------------------------------------------------
# This file was automatically generated from the original CMakeLists.txt file

# Add a library target to the build system
ryppl_library_project(
  boost.graph
  SRCDIRS  src 
  TESTDIRS  test
  #  DOCDIRS 
  DESCRIPTION  "The BGL graph interface and graph components are generic, in the same sense as the the Standard Template Library (STLVERSION 1.41.0)."
  AUTHORS  "Jeremy Siek <jeremy.siek -at- gmail.com>"
           "Lie-Quan Lee"
           "Andrew Lumsdaine"
           "Douglas Gregor <doug.gregor -at- gmail.com>"
  #  MAINTAINERS 
VERSION 1.41.0)
