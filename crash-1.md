# 5.14.14 kernel crash
# AMD Ryzen 5900X

```
Oct 24 20:41:22 localhost.localdomain systemd[1]: Started Hostname Service.
Oct 24 20:41:22 localhost.localdomain nautilus[8955]: Called "net usershare info" but it failed: 'net usershare' returned error 255: net usershare: usershares are currently disabled
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:22 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.ControlCenter.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Contacts.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Documents' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Calculator.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Characters.BackgroundService' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain nautilus[8955]: Connecting to org.freedesktop.Tracker3.Miner.Files
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.clocks' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Notes.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain systemd[1980]: Starting GNOME Terminal Server...
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.ControlCenter.SearchProvider'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.clocks'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Characters.BackgroundService'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Calculator.SearchProvider'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Contacts.SearchProvider'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 20:41:41 localhost.localdomain systemd[1980]: Started GNOME Terminal Server.
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.bluez' unit='dbus-org.bluez.service' requested by ':1.394' (uid=1000 pid=9011 comm="/usr/libexec/gnome-contacts-search-provider ")
Oct 24 20:41:41 localhost.localdomain systemd[1]: Condition check resulted in Bluetooth service being skipped.
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Documents'
Oct 24 20:41:41 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.NoReply: Message recipient disconnected from message bus without replying
Oct 24 20:41:41 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Notes.SearchProvider'
Oct 24 20:41:41 localhost.localdomain bijiben-shell-s[9021]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain bijiben-shell-s[9021]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain bijiben-shell-s[9021]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.DiskUtility' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:41:41 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.DiskUtility'
Oct 24 20:41:52 localhost.localdomain systemd[1]: systemd-hostnamed.service: Deactivated successfully.
Oct 24 20:41:53 localhost.localdomain org.gnome.Notes.SearchProvider[9021]: Unable to load location /home/foo/.local/share/bijiben: Error opening directory '/home/foo/.local/share/bijiben': No such file or directory
Oct 24 20:42:00 localhost.localdomain polkit-agent-helper-1[9341]: gkr-pam: unable to locate daemon control file
Oct 24 20:42:00 localhost.localdomain polkit-agent-helper-1[9341]: gkr-pam: stashed password to try later in open session
Oct 24 20:42:00 localhost.localdomain polkitd[1041]: Operator of unix-session:1 successfully authenticated as unix-user:root to gain TEMPORARY authorization for action org.freedesktop.udisks2.filesystem-mount-system for system-bus-name::1.52 [/usr/libexec/gvfs/gvfs-udisks2-volume-monitor] (owned by unix-user:foo)
Oct 24 20:42:00 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:42:00 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:42:00 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Version 2021.8.22 external FUSE 29
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Mounted /dev/sdc3 (Read-Write, label "Decko", NTFS 3.1)
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Cmdline options: rw,nodev,nosuid,uid=1000,gid=100,windows_names,uhelper=udisks2
Oct 24 20:42:00 localhost.localdomain udisksd[2166]: Mounted /dev/sdc3 at /run/media/foo/Decko on behalf of uid 1000
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Mount options: nodev,nosuid,uhelper=udisks2,allow_other,nonempty,relatime,rw,default_permissions,fsname=/dev/sdc3,blkdev,blksize=4096
Oct 24 20:42:00 localhost.localdomain ntfs-3g[9367]: Global ownership and permissions enforced, configuration type 7
Oct 24 20:42:00 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Shell.HotplugSniffer' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:42:00 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Shell.HotplugSniffer'
Oct 24 20:42:02 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:02 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:02 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:03 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:03 localhost.localdomain kernel: xfs filesystem being remounted at /newroot/home/foo/.cache/gnome-desktop-thumbnailer/gstreamer-1.0 supports timestamps until 2038 (0x7fffffff)
Oct 24 20:42:06 localhost.localdomain dbus-daemon[1029]: [system] Failed to activate service 'org.bluez': timed out (service_start_timeout=25000ms)
Oct 24 20:42:46 localhost.localdomain org.gnome.Nautilus[9493]: Cannot load libcuda.so.1
Oct 24 20:42:46 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 20:42:54 localhost.localdomain systemd[1980]: Started Application launched by gsd-media-keys.
Oct 24 20:42:54 localhost.localdomain guake.desktop[2314]: INFO     Showing the terminal
Oct 24 20:42:54 localhost.localdomain gsd-media-keys[9572]: Sending 'toggle' message to Guake3
Oct 24 20:42:54 localhost.localdomain gnome-shell[2046]: meta_window_set_stack_position_no_sync: assertion 'window->stack_position >= 0' failed
Oct 24 20:42:55 localhost.localdomain gnome-shell[2046]: Window manager warning: last_user_time (1635100974) is greater than comparison timestamp (3985318).  This most likely represents a buggy client sending inaccurate timestamps in messages such as _NET_ACTIVE_WINDOW.  Trying to work around...
Oct 24 20:42:55 localhost.localdomain gnome-shell[2046]: Window manager warning: W87 appears to be one of the offending windows with a timestamp of 1635100974.  Working around...
Oct 24 20:42:56 localhost.localdomain sudo[9578]:      foo : TTY=pts/0 ; PWD=/home/foo ; USER=root ; COMMAND=/usr/bin/sync
Oct 24 20:42:56 localhost.localdomain sudo[9578]: pam_unix(sudo:session): session opened for user root(uid=0) by foo(uid=1000)
Oct 24 20:42:56 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:01 localhost.localdomain sudo[9578]: pam_unix(sudo:session): session closed for user root
Oct 24 20:43:01 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:04 localhost.localdomain guake.desktop[2314]: INFO     Spawning new terminal at /home/foo
Oct 24 20:43:04 localhost.localdomain guake[2314]: (../src/vtepty.cc:667):bool _vte_pty_spawn_sync(VtePty*, const char*, const char* const*, const char* const*, GSpawnFlags, GSpawnChildSetupFunc, gpointer, GDestroyNotify, GPid*, int, GCancellable*, GError**): runtime check failed: ((spawn_flags & ignored_spawn_flags()) == 0)
Oct 24 20:43:04 localhost.localdomain systemd[1980]: Started VTE child process 9585 launched by guake process 2314.
Oct 24 20:43:04 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:04 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:05 localhost.localdomain guake.desktop[2314]: INFO     Guake tabs saved to /home/foo/.config/guake/session.json
Oct 24 20:43:05 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:43:05 localhost.localdomain gnome-shell[2046]: Ignoring search provider /usr/share/gnome-shell/search-providers/firefox-search-provider.ini: missing DesktopId
Oct 24 20:43:14 localhost.localdomain gnome-session-binary[2030]: Entering running state
Oct 24 20:43:18 localhost.localdomain systemd[1]: Starting Temperature monitor...
Oct 24 20:43:18 localhost.localdomain systemd[1]: my-temp-monitor.service: Deactivated successfully.
Oct 24 20:43:18 localhost.localdomain systemd[1]: Finished Temperature monitor.
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Started Application launched by gnome-shell.
Oct 24 20:43:23 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.247' (uid=1000 pid=9627 comm="gnome-terminal ")
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Starting GNOME Terminal Server...
Oct 24 20:43:23 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Started GNOME Terminal Server.
Oct 24 20:43:23 localhost.localdomain systemd[1980]: Started VTE child process 9652 launched by gnome-terminal-server process 9634.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.ControlCenter.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Contacts.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Documents' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Nautilus' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Calculator.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Characters.BackgroundService' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.clocks' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Notes.SearchProvider' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating via systemd: service name='org.gnome.Terminal' unit='gnome-terminal-server.service' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain systemd[1980]: Starting GNOME Terminal Server...
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.ControlCenter.SearchProvider'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.clocks'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Nautilus'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Characters.BackgroundService'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Calculator.SearchProvider'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Terminal'
Oct 24 20:43:27 localhost.localdomain systemd[1980]: Started GNOME Terminal Server.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Documents'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Contacts.SearchProvider'
Oct 24 20:43:27 localhost.localdomain nautilus[9703]: Connecting to org.freedesktop.Tracker3.Miner.Files
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.UnknownMethod: No such interface “org.gnome.Shell.SearchProvider2” on object at path /org/gnome/seahorse/Application
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.bluez' unit='dbus-org.bluez.service' requested by ':1.410' (uid=1000 pid=9699 comm="/usr/libexec/gnome-contacts-search-provider ")
Oct 24 20:43:27 localhost.localdomain systemd[1]: Condition check resulted in Bluetooth service being skipped.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Notes.SearchProvider'
Oct 24 20:43:27 localhost.localdomain bijiben-shell-s[9711]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.Photos' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain bijiben-shell-s[9711]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.Photos'
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Activating service name='org.gnome.seahorse.Application' requested by ':1.11' (uid=1000 pid=2046 comm="/usr/bin/gnome-shell ")
Oct 24 20:43:27 localhost.localdomain bijiben-shell-s[9711]: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
Oct 24 20:43:27 localhost.localdomain systemd[1980]: Started Application launched by gnome-shell.
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1999]: [session uid=1000 pid=1999] Successfully activated service 'org.gnome.seahorse.Application'
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Timelines with detached actors are not supported
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.Error.NoReply: Message recipient disconnected from message bus without replying
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 7 threads of 3 processes of 1 users.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Successfully made thread 10144 of process 9914 owned by 'foo' RT at priority 10.
Oct 24 20:43:27 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
Oct 24 20:43:28 localhost.localdomain rtkit-daemon[1600]: Supervising 8 threads of 4 processes of 1 users.
```
