# 5.14.14 kernel crash

```
Oct 24 20:43:27 localhost.localdomain nautilus[9703]: Connecting to org.freedesktop.Tracker3.Miner.Files
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.E>
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Wrong number of result metas returned by search provider org.gnome.seahorse.Application.desktop: expected 1 but got 0
Oct 24 20:43:27 localhost.localdomain dbus-daemon[1029]: [system] Activating via systemd: service name='org.bluez' unit='dbus-org.bluez.service' requested by ':1.410' (uid=1000 pid=9699 comm="/usr/libexec/gnome>
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
Oct 24 20:43:27 localhost.localdomain gnome-shell[2046]: Received error from D-Bus search provider org.gnome.seahorse.Application.desktop during GetResultMetas: Gio.DBusError: GDBus.Error:org.freedesktop.DBus.E>
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
