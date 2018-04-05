BootStrap: zypper
MirrorURL: http://download.opensuse.org/distribution/11.4/repo/oss/
Include: zypper

%runscript
    python "$@"

%post
    zypper ar https://download.opensuse.org/repositories/home:/pelupes:/branches:/devel:/gcc:/gcc/openSUSE_11.4/ gcc
    zypper ar https://download.opensuse.org/repositories/home:/pelupes:/amuse/openSUSE_11.4 amuse
    zypper --gpg-auto-import-keys refresh amuse
    zypper --gpg-auto-import-keys refresh gcc
    echo "install amuse inside the container (post)"
    zypper -n install --force-resolution libstdc++6 amuse
