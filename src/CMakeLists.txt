ADD_SUBDIRECTORY(font)
ADD_SUBDIRECTORY(text)
ADD_SUBDIRECTORY(render)
ADD_SUBDIRECTORY(utils)

ADD_LIBRARY(freetype_direct_gl STATIC
  $<TARGET_OBJECTS:font>
  $<TARGET_OBJECTS:text>
  $<TARGET_OBJECTS:render>
  $<TARGET_OBJECTS:utils>
)

TARGET_INCLUDE_DIRECTORIES(render PRIVATE
  ${FREETYPE_INCLUDE_DIRS}
)
