package(
    default_visibility = ["//visibility:public"],
)

cc_library(
    name = "openmp",
    srcs = glob(['*.c'], exclude=['taskloop.c', 'lock.c'])
      + glob(['*.h'], exclude=["omp.h"]) + glob([
          'stage/*.h',
      ]) + glob([
          'config/posix/*.c',
      ]) + glob([
          'config/posix/*.h',
      ])
    ,
    hdrs = [ "omp.h" ],
    textual_hdrs = [ "taskloop.c", "splay-tree.c", "omp.h.in" ],
    includes = [ 'stage', 'config/posix', './' ],
)
