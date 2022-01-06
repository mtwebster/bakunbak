project('bakunbak', version: '1.0.0')

install_bindir = join_paths(get_option('prefix'), get_option('bindir'))
install_mandir = join_paths(get_option('prefix'), get_option('datadir'), 'man', 'man1')

install_data(
    [
      'bakunbak'
    ],

    install_dir: install_bindir,
    install_mode: 'rwxr-xr-x'
)

manpage = custom_target('manpage',
    output: 'bakunbak.1',
    command: [
        'argparse-manpage',
        '--pyfile', join_paths(meson.source_root(), 'bakunbak'),
        '--function', 'get_parser',
        '--author', 'Michael Webster',
        '--author-email', 'miketwebster@gmail.com',
        '--project-name', 'bakunbak',
        '--url', 'https://github.com/mtwebster/bakunbak',
        '--output', '@OUTPUT@'
    ],
    install: true,
    install_dir: install_mandir
)

install_man('bak.1')
install_man('unbak.1')

meson.add_install_script('make_symlinks.sh')
