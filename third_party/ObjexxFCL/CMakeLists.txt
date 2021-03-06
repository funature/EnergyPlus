set( target_name objexx )

if(MSVC)
  ADD_DEFINITIONS("-Za") # Disables MS language extensions
endif()

if (UNIX)
  SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC")
endif()

set(src
  src/ObjexxFCL/array.iterator.hh
  src/ObjexxFCL/ArrayTraits.hh
  src/ObjexxFCL/Backspace.cc
  src/ObjexxFCL/Backspace.hh
  src/ObjexxFCL/BArray.fwd.hh
  src/ObjexxFCL/BArray.hh
  src/ObjexxFCL/bit.hh
  src/ObjexxFCL/byte.fwd.hh
  src/ObjexxFCL/byte.hh
  src/ObjexxFCL/CArray.fwd.hh
  src/ObjexxFCL/CArray.hh
  src/ObjexxFCL/CArray.io.hh
  src/ObjexxFCL/CArrayP.fwd.hh
  src/ObjexxFCL/CArrayP.hh
  src/ObjexxFCL/CArrayP.io.hh
  src/ObjexxFCL/char.constants.cc
  src/ObjexxFCL/char.constants.hh
  src/ObjexxFCL/char.functions.cc
  src/ObjexxFCL/char.functions.hh
  src/ObjexxFCL/Chunk.hh
  src/ObjexxFCL/ChunkExponent.hh
  src/ObjexxFCL/ChunkVector.fwd.hh
  src/ObjexxFCL/ChunkVector.hh
  src/ObjexxFCL/ChunkVector.io.hh
  src/ObjexxFCL/Cstring.cc
  src/ObjexxFCL/Cstring.fwd.hh
  src/ObjexxFCL/Cstring.hh
  src/ObjexxFCL/Dimension.cc
  src/ObjexxFCL/Dimension.fwd.hh
  src/ObjexxFCL/Dimension.hh
  src/ObjexxFCL/DimensionExpression.cc
  src/ObjexxFCL/DimensionExpression.hh
  src/ObjexxFCL/DimensionExpressionCon.hh
  src/ObjexxFCL/DimensionExpressionCube.hh
  src/ObjexxFCL/DimensionExpressionDiv.hh
  src/ObjexxFCL/DimensionExpressionMax.hh
  src/ObjexxFCL/DimensionExpressionMin.hh
  src/ObjexxFCL/DimensionExpressionMul.hh
  src/ObjexxFCL/DimensionExpressionPow.hh
  src/ObjexxFCL/DimensionExpressionRef.cc
  src/ObjexxFCL/DimensionExpressionRef.hh
  src/ObjexxFCL/DimensionExpressions.hh
  src/ObjexxFCL/DimensionExpressionSquare.hh
  src/ObjexxFCL/DimensionExpressionSub.hh
  src/ObjexxFCL/DimensionExpressionSum.hh
  src/ObjexxFCL/DimensionSlice.fwd.hh
  src/ObjexxFCL/DimensionSlice.hh
  src/ObjexxFCL/DynamicIndexRange.cc
  src/ObjexxFCL/DynamicIndexRange.fwd.hh
  src/ObjexxFCL/DynamicIndexRange.hh
  src/ObjexxFCL/environment.cc
  src/ObjexxFCL/environment.hh
  src/ObjexxFCL/FArray.all.fwd.hh
  src/ObjexxFCL/FArray.all.hh
  src/ObjexxFCL/FArray.all.io.hh
  src/ObjexxFCL/FArray.functions.hh
  src/ObjexxFCL/FArray.fwd.hh
  src/ObjexxFCL/FArray.hh
  src/ObjexxFCL/FArray.io.hh
  src/ObjexxFCL/FArray1.all.fwd.hh
  src/ObjexxFCL/FArray1.all.hh
  src/ObjexxFCL/FArray1.fwd.hh
  src/ObjexxFCL/FArray1.hh
  src/ObjexxFCL/FArray1.io.hh
  src/ObjexxFCL/FArray1.Project.MArray.hh
  src/ObjexxFCL/FArray1A.fwd.hh
  src/ObjexxFCL/FArray1A.hh
  src/ObjexxFCL/FArray1D.fwd.hh
  src/ObjexxFCL/FArray1D.hh
  src/ObjexxFCL/FArray1P.fwd.hh
  src/ObjexxFCL/FArray1P.hh
  src/ObjexxFCL/FArray1S.fwd.hh
  src/ObjexxFCL/FArray1S.hh
  src/ObjexxFCL/FArray1S.io.hh
  src/ObjexxFCL/FArray1S.Project.MArray.hh
  src/ObjexxFCL/FArray2.all.fwd.hh
  src/ObjexxFCL/FArray2.all.hh
  src/ObjexxFCL/FArray2.fwd.hh
  src/ObjexxFCL/FArray2.hh
  src/ObjexxFCL/FArray2.io.hh
  src/ObjexxFCL/FArray2.Project.MArray.hh
  src/ObjexxFCL/FArray2A.fwd.hh
  src/ObjexxFCL/FArray2A.hh
  src/ObjexxFCL/FArray2D.fwd.hh
  src/ObjexxFCL/FArray2D.hh
  src/ObjexxFCL/FArray2P.fwd.hh
  src/ObjexxFCL/FArray2P.hh
  src/ObjexxFCL/FArray2S.fwd.hh
  src/ObjexxFCL/FArray2S.hh
  src/ObjexxFCL/FArray2S.io.hh
  src/ObjexxFCL/FArray2S.Project.MArray.hh
  src/ObjexxFCL/FArray3.all.fwd.hh
  src/ObjexxFCL/FArray3.all.hh
  src/ObjexxFCL/FArray3.fwd.hh
  src/ObjexxFCL/FArray3.hh
  src/ObjexxFCL/FArray3.io.hh
  src/ObjexxFCL/FArray3A.fwd.hh
  src/ObjexxFCL/FArray3A.hh
  src/ObjexxFCL/FArray3D.fwd.hh
  src/ObjexxFCL/FArray3D.hh
  src/ObjexxFCL/FArray3P.fwd.hh
  src/ObjexxFCL/FArray3P.hh
  src/ObjexxFCL/FArray3S.fwd.hh
  src/ObjexxFCL/FArray3S.hh
  src/ObjexxFCL/FArray3S.io.hh
  src/ObjexxFCL/FArray4.all.fwd.hh
  src/ObjexxFCL/FArray4.all.hh
  src/ObjexxFCL/FArray4.fwd.hh
  src/ObjexxFCL/FArray4.hh
  src/ObjexxFCL/FArray4.io.hh
  src/ObjexxFCL/FArray4A.fwd.hh
  src/ObjexxFCL/FArray4A.hh
  src/ObjexxFCL/FArray4D.fwd.hh
  src/ObjexxFCL/FArray4D.hh
  src/ObjexxFCL/FArray4P.fwd.hh
  src/ObjexxFCL/FArray4P.hh
  src/ObjexxFCL/FArray4S.fwd.hh
  src/ObjexxFCL/FArray4S.hh
  src/ObjexxFCL/FArray4S.io.hh
  src/ObjexxFCL/FArray5.all.fwd.hh
  src/ObjexxFCL/FArray5.all.hh
  src/ObjexxFCL/FArray5.fwd.hh
  src/ObjexxFCL/FArray5.hh
  src/ObjexxFCL/FArray5.io.hh
  src/ObjexxFCL/FArray5A.fwd.hh
  src/ObjexxFCL/FArray5A.hh
  src/ObjexxFCL/FArray5D.fwd.hh
  src/ObjexxFCL/FArray5D.hh
  src/ObjexxFCL/FArray5P.fwd.hh
  src/ObjexxFCL/FArray5P.hh
  src/ObjexxFCL/FArray5S.fwd.hh
  src/ObjexxFCL/FArray5S.hh
  src/ObjexxFCL/FArray5S.io.hh
  src/ObjexxFCL/FArray6.all.fwd.hh
  src/ObjexxFCL/FArray6.all.hh
  src/ObjexxFCL/FArray6.fwd.hh
  src/ObjexxFCL/FArray6.hh
  src/ObjexxFCL/FArray6.io.hh
  src/ObjexxFCL/FArray6A.fwd.hh
  src/ObjexxFCL/FArray6A.hh
  src/ObjexxFCL/FArray6D.fwd.hh
  src/ObjexxFCL/FArray6D.hh
  src/ObjexxFCL/FArray6P.fwd.hh
  src/ObjexxFCL/FArray6P.hh
  src/ObjexxFCL/FArray6S.fwd.hh
  src/ObjexxFCL/FArray6S.hh
  src/ObjexxFCL/FArray6S.io.hh
  src/ObjexxFCL/FArrayInitializer.fwd.hh
  src/ObjexxFCL/FArrayInitializer.hh
  src/ObjexxFCL/FArrayRS.fwd.hh
  src/ObjexxFCL/FArrayRS.hh
  src/ObjexxFCL/FArrayS.all.fwd.hh
  src/ObjexxFCL/FArrayS.all.hh
  src/ObjexxFCL/FArrayS.all.io.hh
  src/ObjexxFCL/FArrayS.functions.hh
  src/ObjexxFCL/FArrayS.fwd.hh
  src/ObjexxFCL/FArrayS.hh
  src/ObjexxFCL/FArrayS.io.hh
  src/ObjexxFCL/FArrayTail.fwd.hh
  src/ObjexxFCL/FArrayTail.hh
  src/ObjexxFCL/floops.hh
  src/ObjexxFCL/Fmath.hh
  src/ObjexxFCL/fmt.cc
  src/ObjexxFCL/fmt.hh
  src/ObjexxFCL/fmt.manipulators.hh
  src/ObjexxFCL/Format.cc
  src/ObjexxFCL/Format.hh
  src/ObjexxFCL/FormattedIO.hh
  src/ObjexxFCL/Fstring.cc
  src/ObjexxFCL/Fstring.fwd.hh
  src/ObjexxFCL/Fstring.hh
  src/ObjexxFCL/gio.cc
  src/ObjexxFCL/gio.hh
  src/ObjexxFCL/gio_Fmt.fwd.hh
  src/ObjexxFCL/gio_Fmt.hh
  src/ObjexxFCL/GlobalStreams.cc
  src/ObjexxFCL/GlobalStreams.hh
  src/ObjexxFCL/Index.cc
  src/ObjexxFCL/Index.fwd.hh
  src/ObjexxFCL/Index.hh
  src/ObjexxFCL/IndexRange.cc
  src/ObjexxFCL/IndexRange.fwd.hh
  src/ObjexxFCL/IndexRange.hh
  src/ObjexxFCL/IndexSlice.cc
  src/ObjexxFCL/IndexSlice.fwd.hh
  src/ObjexxFCL/IndexSlice.hh
  src/ObjexxFCL/InitializerSentinel.hh
  src/ObjexxFCL/Inquire.cc
  src/ObjexxFCL/Inquire.hh
  src/ObjexxFCL/IOFlags.cc
  src/ObjexxFCL/IOFlags.fwd.hh
  src/ObjexxFCL/IOFlags.hh
  src/ObjexxFCL/MArray.all.fwd.hh
  src/ObjexxFCL/MArray.all.hh
  src/ObjexxFCL/MArray.all.io.hh
  src/ObjexxFCL/MArray.functions.hh
  src/ObjexxFCL/MArray.fwd.hh
  src/ObjexxFCL/MArray.hh
  src/ObjexxFCL/MArray.io.hh
  src/ObjexxFCL/MArray1.fwd.hh
  src/ObjexxFCL/MArray1.hh
  src/ObjexxFCL/MArray1.io.hh
  src/ObjexxFCL/MArray1.Project.MArray.hh
  src/ObjexxFCL/MArray2.fwd.hh
  src/ObjexxFCL/MArray2.hh
  src/ObjexxFCL/MArray2.io.hh
  src/ObjexxFCL/MArray3.fwd.hh
  src/ObjexxFCL/MArray3.hh
  src/ObjexxFCL/MArray3.io.hh
  src/ObjexxFCL/MArray4.fwd.hh
  src/ObjexxFCL/MArray4.hh
  src/ObjexxFCL/MArray4.io.hh
  src/ObjexxFCL/MArray5.fwd.hh
  src/ObjexxFCL/MArray5.hh
  src/ObjexxFCL/MArray5.io.hh
  src/ObjexxFCL/MArray6.fwd.hh
  src/ObjexxFCL/MArray6.hh
  src/ObjexxFCL/MArray6.io.hh
  src/ObjexxFCL/MArrayR.fwd.hh
  src/ObjexxFCL/MArrayR.hh
  src/ObjexxFCL/numeric.cc
  src/ObjexxFCL/numeric.hh
  src/ObjexxFCL/ObjexxFCL.fwd.hh
  src/ObjexxFCL/ObjexxFCL.hh
  src/ObjexxFCL/ObjexxFCL.Project.hh
  src/ObjexxFCL/Observer.cc
  src/ObjexxFCL/Observer.fwd.hh
  src/ObjexxFCL/Observer.hh
  src/ObjexxFCL/ObserverGraph.cc
  src/ObjexxFCL/ObserverGraph.hh
  src/ObjexxFCL/ObserverMediator.cc
  src/ObjexxFCL/ObserverMediator.hh
  src/ObjexxFCL/ObserverMulti.cc
  src/ObjexxFCL/ObserverMulti.hh
  src/ObjexxFCL/ObserverSingle.hh
  src/ObjexxFCL/Omit.cc
  src/ObjexxFCL/Omit.fwd.hh
  src/ObjexxFCL/Omit.hh
  src/ObjexxFCL/Optional.fwd.hh
  src/ObjexxFCL/Optional.hh
  src/ObjexxFCL/Print.fwd.hh
  src/ObjexxFCL/Print.hh
  src/ObjexxFCL/proxy_const_assert.hh
  src/ObjexxFCL/ProxySentinel.hh
  src/ObjexxFCL/random.cc
  src/ObjexxFCL/random.hh
  src/ObjexxFCL/Read.cc
  src/ObjexxFCL/Read.fwd.hh
  src/ObjexxFCL/Read.hh
  src/ObjexxFCL/Reference.fwd.hh
  src/ObjexxFCL/Reference.hh
  src/ObjexxFCL/Required.fwd.hh
  src/ObjexxFCL/Required.hh
  src/ObjexxFCL/Rewind.cc
  src/ObjexxFCL/Rewind.hh
  src/ObjexxFCL/rvalue_cast.hh
  src/ObjexxFCL/sbyte.fwd.hh
  src/ObjexxFCL/sbyte.hh
  src/ObjexxFCL/SetWrapper.fwd.hh
  src/ObjexxFCL/SetWrapper.hh
  src/ObjexxFCL/Star.cc
  src/ObjexxFCL/Star.fwd.hh
  src/ObjexxFCL/Star.hh
  src/ObjexxFCL/StaticIndexRange.fwd.hh
  src/ObjexxFCL/StaticIndexRange.hh
  src/ObjexxFCL/Sticky.fwd.hh
  src/ObjexxFCL/Sticky.hh
  src/ObjexxFCL/Stream.cc
  src/ObjexxFCL/stream.functions.cc
  src/ObjexxFCL/stream.functions.hh
  src/ObjexxFCL/Stream.fwd.hh
  src/ObjexxFCL/Stream.hh
  src/ObjexxFCL/string.constants.cc
  src/ObjexxFCL/string.constants.hh
  src/ObjexxFCL/string.functions.cc
  src/ObjexxFCL/string.functions.hh
  src/ObjexxFCL/Time_Date.cc
  src/ObjexxFCL/Time_Date.hh
  src/ObjexxFCL/TraitsA.hh
  src/ObjexxFCL/TraitsB.hh
  src/ObjexxFCL/TraitsE.hh
  src/ObjexxFCL/TraitsF.hh
  src/ObjexxFCL/TraitsG.hh
  src/ObjexxFCL/TraitsI.hh
  src/ObjexxFCL/TraitsLD.hh
  src/ObjexxFCL/TypeTraits.hh
  src/ObjexxFCL/ubyte.fwd.hh
  src/ObjexxFCL/ubyte.hh
  src/ObjexxFCL/Vector2.fwd.hh
  src/ObjexxFCL/Vector2.hh
  src/ObjexxFCL/Vector3.fwd.hh
  src/ObjexxFCL/Vector3.hh
  src/ObjexxFCL/Write.cc
  src/ObjexxFCL/Write.fwd.hh
  src/ObjexxFCL/Write.hh
)

set( test_src
  tst/unit/Backspace.unit.cc
  tst/unit/bit.unit.cc
  tst/unit/byte.unit.cc
  tst/unit/CArray.unit.cc
  tst/unit/CArrayP.unit.cc
  tst/unit/char.functions.unit.cc
  tst/unit/Chunk.unit.cc
  tst/unit/ChunkVector.unit.cc
  tst/unit/Cstring.unit.cc
  tst/unit/Dimension.unit.cc
  tst/unit/DimensionSlice.unit.cc
  tst/unit/DynamicIndexRange.unit.cc
  tst/unit/FArray.unit.cc
  tst/unit/FArray1.unit.cc
  tst/unit/FArray2.unit.cc
  tst/unit/FArray3.unit.cc
  tst/unit/FArray4.unit.cc
  tst/unit/FArray5.unit.cc
  tst/unit/FArray6.unit.cc
  tst/unit/FArrayS.unit.cc
  tst/unit/floops.unit.cc
  tst/unit/Fmath.unit.cc
  tst/unit/fmt.unit.cc
  tst/unit/Fstring.unit.cc
  tst/unit/gio.unit.cc
  tst/unit/GlobalStreams.unit.cc
  tst/unit/Index.unit.cc
  tst/unit/IndexSlice.unit.cc
  tst/unit/main.cc
  tst/unit/MArray.unit.cc
  tst/unit/numeric.unit.cc
  tst/unit/ObjexxFCL.unit.hh
  tst/unit/Optional.unit.cc
  tst/unit/Print.unit.cc
  tst/unit/Read.unit.cc
  tst/unit/Reference.Optional.unit.cc
  tst/unit/Reference.unit.cc
  tst/unit/Required.unit.cc
  tst/unit/StaticIndexRange.unit.cc
  tst/unit/Stream.unit.cc
  tst/unit/string.functions.unit.cc
  tst/unit/TypeTraits.unit.cc
  tst/unit/ubyte.unit.cc
  tst/unit/Vector2.unit.cc
  tst/unit/Vector3.unit.cc
  tst/unit/Write.unit.cc
)


add_library( ${target_name} ${src} )

CREATE_TEST_TARGETS( ${target_name} "${test_src}" "" )

