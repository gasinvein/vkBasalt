data_dir = get_option('datadir')

vulkan_layer_dir = join_paths(data_dir, 'vulkan', 'implicit_layer.d')
reshade_dir = join_paths(get_option('prefix'), data_dir, 'reshade')

configure_file(
    input : 'vkBasalt.json.in',
    output : 'vkBasalt.json',
    configuration : {'ld_lib_dir_vkbasalt' : ld_lib_dir_vkbasalt},
    install : true,
    install_dir : vulkan_layer_dir,
)

configure_file(
    input : 'vkBasalt.conf.in',
    output : 'vkBasalt.conf',
    configuration : {'RESHADE_DIR' : reshade_dir},
    install : true,
    install_dir : join_paths(get_option('sysconfdir'), 'vkBasalt')
)
