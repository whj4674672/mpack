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
src/mpack/mpack-common.c
src/mpack/mpack-expect.c
src/mpack/mpack-node.c
src/mpack/mpack-platform.c
src/mpack/mpack-reader.c
src/mpack/mpack-riter.c
""")

CPPPATH = [cwd + '/src/mpack']

if GetDepend(['PKG_USING_MSGPACK_EXAMPLE']):
    src += [('/examples/sax-example.c')]
    CPPPATH += [cwd + '/examples']


group = DefineGroup('msgpack', src, depend = ['PKG_USING_MSGPACK'], CPPPATH = CPPPATH)

Return('group')