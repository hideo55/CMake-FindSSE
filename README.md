# FindSSE.cmake

CMake module for check whether a SSE instructions can be used on the machine.

- Supports SSE2/SSE3/SSSE3/SSE4.1/SSE4.2
- Supports check GCC version(-msse4.2 can use on GCC 4.3 or later)

## Usage

```
SET (CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

INCLUDE(FindSSE)
FindSSE ()
IF(SSE3_FOUND)
    IF(SSSE3_FOUND)
            SET(CXX_DFLAGS -msse3 -mssse3)
    ENDIF(SSSE3_FOUND)
ENDIF(SSE3_FOUND)

IF(SSE4_2_FOUND)
        SET(CXX_DFLAGS -msse4.2 -mpopcnt)
ENDIF(SSE4_2_FOUND)
ADD_DEFINITIONS(${CXX_DFLAGS})
```
## Variables

- SSE2\_FOUND
- SSE3\_FOUND
- SSSE3\_FOUND
- SSE4\_1\_FOUND
- SSE4\_2\_FOUND

