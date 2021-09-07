from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

# add sm3041 src files.
if GetDepend('PKG_USING_SM3041'):
    src += Glob('src/sm30_device.c')

if GetDepend('PKG_USING_SM3041_SAMPLE'):
    src += Glob('sample/sm3041_sample.c')

# add sm3041 include path.
path = [cwd + '/inc']

group = DefineGroup('sm3041', src, depend = ['PKG_USING_SM3041'], CPPPATH = path)

Return('group')
