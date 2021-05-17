project('imgui-meson-app', 'cpp')

# Internal libraries 
subdir('src/functions')

glew_dep = dependency('glew')
imgui_dep = dependency('imgui', fallback : ['imgui', 'imgui_dep'])
gl_dep = dependency('opengl')
glfw3_dep = dependency('glfw3')

src_files = ['src/main.cpp']

include_dirs = [
    'src/functions',
]

executable('imgui-meson-app',
    sources : src_files,
    dependencies : [glew_dep, gl_dep, glfw3_dep, imgui_dep],
    include_directories : include_dirs,
    link_with : functions_lib
)