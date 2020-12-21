#
# File      : SConscript
# This file is part of RT-Thread RTOS/WebNet Server
# COPYRIGHT (C) 2011, Shanghai Real-Thread Technology Co., Ltd
#
# All rights reserved.
#
# Change Logs:
# Date           Author       Notes
# 2011-08-02     Bernard      the first version
#

Import('RTT_ROOT')
from building import *

cwd = GetCurrentDir()

src = Split("""
src/mpack/mpack_common.c
src/mpack/mpack_expect.c
src/mpack/mpack_node.c
src/mpack/mpack_platform.c
src/mpack/mpack_reader.c
src/mpack/mpack_riter.c
""")

CPPPATH = [cwd + '/src/mpack']

group = DefineGroup('msgpack', src, depend = ['PKG_USING_MSGPACK'], CPPPATH = CPPPATH)

Return('group')