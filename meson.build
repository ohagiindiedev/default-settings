project('elementary-default-settings')

meson.add_install_script('meson/post_install.py')

# Printer testpage
install_data(
    'default-testpage.pdf',
    install_dir: join_paths(get_option('datadir'), 'cups', 'data')
)

# Installer session lightdm.conf
install_data(
    'lightdm.conf',
    install_dir: join_paths(get_option('sysconfdir'), 'lightdm')
)

install_data(
    'policykit.desktop',
    install_dir: join_paths(get_option('datadir'), 'applications')
)

install_data(
    'settings.ini',
    install_dir: join_paths(get_option('sysconfdir'), 'gtk-3.0')
)

install_data(
    'sessioninstaller.desktop',
    install_dir: join_paths(get_option('datadir'), 'applications')
)

# TODO: dynamically generate appcenter.blacklist list using meson options
install_data(
    'appcenter.blacklist',
    install_dir: join_paths(get_option('sysconfdir'), 'appcenter')
)

# TODO: dynamically generate dockitem list using meson options
dock_items = [
    join_paths('.', 'plank', 'dock1', 'launchers', 'gala-multitaskingview.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'io.elementary.appcenter.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'org.gnome.Epiphany.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'org.pantheon.audience.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'org.pantheon.mail.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'org.pantheon.maya.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'org.pantheon.noise.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'org.pantheon.photos.dockitem'),
    join_paths('.', 'plank', 'dock1', 'launchers', 'org.pantheon.switchboard.dockitem'),
]

install_data(
    dock_items,
    install_dir: join_paths(get_option('sysconfdir'), 'skel', '.config', 'plank', 'dock1', 'launchers')
)

# TODO: glob all *.sh files
# TODO: move to ./profile.d/meson.build
profiles = [
    join_paths('.', 'profile.d', 'gtk-csd.sh'),
    join_paths('.', 'profile.d', 'pantheon-filechooser-module.sh'),
    join_paths('.', 'profile.d', 'qt-style-override.sh')
]

# TODO: glob all *.sh files
# TODO: move to ./profile.d/meson.build
install_data(
    profiles,
    install_dir: join_paths(get_option('sysconfdir'), 'profile.d')
)

# TODO: glob all files
# TODO: move to ./sudoers.d/meson.build
install_data(
    join_paths('.', 'sudoers.d', 'pwfeedback'),
    install_dir: join_paths(get_option('sysconfdir'), 'sudoers.d')
)

install_data(
    join_paths('.', 'wingpanel.d', 'ayatana.blacklist'),
    install_dir: join_paths(get_option('sysconfdir'), 'wingpanel.d')
)

# TODO: install the following:
# * dpms/
# * plymouth/
# * ubiquity-slideshow-elementary/
# * debian/elementary-default-settings.gsettings-override
# * debian/elementary-dpms-helper.1
# * make gtk-sound-theme-name configurable, Ubuntu/elementary should be 'ubuntu', otherwise 'freedesktop'
# * make gtk-fallback-icon-theme configurable, Loki should be 'gnome', Juno 'Adwaita'