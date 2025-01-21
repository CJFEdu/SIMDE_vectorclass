project('SIMDE_vectorclass', 'cpp',
        version : '0.1.0',
        default_options : ['warning_level=3', 'cpp_std=c++20'])

subdir('include')

simde_dep = dependency('simde')
SIMDE_vectorclass_dep = declare_dependency(
    link_with : SIMDE_vectorclass_lib,
    include_directories : include_directories('include')
)

if not meson.is_subproject()
    message('Building tests for subproject')
    executable(
        'SIMDE_vectorclass_tests',
        'src/test.cpp',
        dependencies : [SIMDE_vectorclass_dep,simde_dep]
    )
else
    message('Not building tests for subproject')
endif
