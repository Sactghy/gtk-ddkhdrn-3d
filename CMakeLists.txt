cmake_minimum_required(VERSION 3.5)

project(gtk4-ddchstar LANGUAGES C)

include_directories(/usr/include/gtk-4.0 /usr/include/glib-2.0 /usr/lib64/glib-2.0/include)
include_directories(/usr/lib64/glib-2.0/include /usr/include/cairo /usr/include/pango-1.0)
include_directories(/usr/include/harfbuzz /usr/include/gdk-pixbuf-2.0 /usr/lib64/graphene-1.0/include)
include_directories(/usr/include/graphene-1.0)

add_executable(gtk4-ddchstar main.c)
target_link_libraries(gtk4-ddchstar m)
target_link_libraries(gtk4-ddchstar gtk-4 pangocairo-1.0 pango-1.0 harfbuzz cairo-gobject cairo)
target_link_libraries(gtk4-ddchstar graphene-1.0 glib-2.0 gobject-2.0 gio-2.0 gdk_pixbuf-2.0)
