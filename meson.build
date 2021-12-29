project('bakunbak', version: '1.0.0')

message('Did you run the tests?????')

install_bindir = join_paths(get_option('prefix'), get_option('bindir'))

install_data(
    [
      'bakunbak'
    ],

    install_dir: install_bindir,
    install_mode: 'rwxr-xr-x'
)

meson.add_install_script('make_symlinks.sh')
