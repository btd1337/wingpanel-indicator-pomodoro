project ('pomodoro', ['vala', 'c'],
  version: '1.0.0',
  meson_version: '>=0.34'
)

add_project_arguments(['--vapidir', join_paths(meson.current_source_dir(), 'vapi')], language: 'vala')

glib = dependency('glib-2.0')
gobject = dependency('gobject-2.0')
gtk = dependency('gtk+-3.0')
granite = dependency('granite')
wingpanel = dependency('wingpanel-2.0')
notify = dependency('libnotify')

subdir ('src')
subdir ('po')

shared_module(meson.project_name (),
            sources,
            dependencies : [glib, gobject, gtk, granite, wingpanel, notify],
            install: true,
            install_dir : '/usr/lib/x86_64-linux-gnu/wingpanel/'
)
