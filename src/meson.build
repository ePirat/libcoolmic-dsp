coolmic_dsp_sources = files(
    'buffer.c',
    'common_opus.c',
    'coolmic-dsp.c',
    'enc.c',
    'enc_vorbis.c',
    'iobuffer.c',
    'iohandle.c',
    'logging.c',
    'metadata.c',
    'shout.c',
    'simple.c',
    'snddev.c',
    'snddev_null.c',
#   'snddev_opensl.c',
#   'snddev_oss.c',
    'snddev_sine.c',
    'snddev_stdio.c',
    'tee.c',
    'transform.c',
    'util.c',
    'vumeter.c',
)

if libopus_dep.found()
    coolmic_dsp_sources += files('enc_opus.c')
    add_project_arguments('-DHAVE_ENC_OPUS', language : 'c')
endif

add_project_arguments('-DHAVE_SNDDRV_DRIVER_STDIO', language : 'c')

library('libcoolmic-dsp', coolmic_dsp_sources,
    include_directories : coolmic_dsp_incdir,
    dependencies : [coolmic_dsp_deps, libopus_dep],
    install : true)
