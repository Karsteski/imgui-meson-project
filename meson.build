project('imgui-meson-app', 'cpp')

# Internal libraries 
subdir('src/functions')
subdir('libs/imgui')


src_files = ['src/main.cpp']
include_dirs = ['src/functions']


lib_names = [
    'glfw3',
    'opengl'
]


deps = []


foreach lib : lib_names
    temp = dependency(lib, required : false)
    if not temp.found()
        temp = cpp_compiler.find_library(lib)
    endif

    deps += temp
endforeach


executable('imgui-meson-app',
    sources : src_files,
    dependencies : [deps, imgui_dep],
    include_directories : include_dirs,
    link_with : [functions_lib, imgui_lib]
)

message('Project built! :)')