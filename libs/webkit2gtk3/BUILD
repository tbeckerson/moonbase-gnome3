OPTS+="-DPORT=GTK \
   -DUSE_WOFF2=OFF \
   -DCMAKE_SKIP_RPATH=ON \
   -DENABLE_WEBKIT_LEGACY=OFF \
   -DCMAKE_INSTALL_PREFIX=/usr \
   -DUSE_SYSTEM_MALLOC=ON \
   -DLIB_INSTALL_DIR=/usr/lib \
   -DPYTHON_EXECUTABLE:FILEPATH=/usr/bin/python3"

if [[ $MINIBROWSER == "y" ]]; then
  OPTS+=" -DENABLE_MINIBROWSER=ON"
fi

default_cmake_build &&

# symlink plugin folder to a location webkit looks for it
if [ ! -e "/usr/lib/browser-plugins" ]; then
  ln -sf /usr/lib/lunar/plugins /usr/lib/browser-plugins
fi
