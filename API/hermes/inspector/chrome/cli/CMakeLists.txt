# Copyright (c) Meta Platforms, Inc. and affiliates.
#
# This source code is licensed under the MIT license found in the
# LICENSE file in the root directory of this source tree.

set(HERMES_ENABLE_EH ON)
set(HERMES_ENABLE_RTTI ON)
add_hermes_tool(hcds
  main.cpp
  ${ALL_HEADER_FILES}
  )

target_link_libraries(hcds
  hermesapi
  hermes_inspector
  jsinspector
)

install(TARGETS hcds
  RUNTIME DESTINATION bin
)
