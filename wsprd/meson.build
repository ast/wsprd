project('wsprd', 'c')

cc = meson.get_compiler('c')

fftw3f   = dependency('fftw3f')
dispatch = cc.find_library('dispatch', required : true)
blocks   = cc.find_library('BlocksRuntime', required: true)
m        = cc.find_library('m', required: true)

sources = ['wsprd.c', 'fano.c', 'nhash.c',
           'wsprd_utils.c', 'wsprsim_utils.c', 'metric_tables.c', 'tab.c']

executable('wsprd',
	sources,
	dependencies: [fftw3f, dispatch, blocks,  m]
)
