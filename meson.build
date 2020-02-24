project('libcoolmic-dsp', 'c',
    version : '0.1',
    default_options : ['warning_level=3'])

# External dependencies
coolmic_dsp_deps = [
    dependency('shout'),
    dependency('ogg'),
    dependency('vorbis'),
    dependency('vorbisenc'),
]

libopus_dep = dependency('opus', required : false)

# Subdirectories
coolmic_dsp_incdir = include_directories('include')
subdir('include/coolmic-dsp')
subdir('src')


# Create pkg-config .pc file
# pkg_mod = import('pkgconfig')
# pkg_mod.generate(libraries : foolib,
#                 version : '1.0',
#                 name : 'libfoobar',
#                 filebase : 'foobar',
#                 description : 'A Library to barnicate your foos.')
