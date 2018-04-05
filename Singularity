BootStrap: localimage
From: /home/inti/zandbak/singularity/test/test.simg

%runscript
    echo "This is what happens when you run the container..."

%post
    zypper ar https://download.opensuse.org/repositories/home:/pelupes:/branches:/devel:/gcc:/gcc/openSUSE_11.4/ gcc
    zypper ar https://download.opensuse.org/repositories/home:/pelupes:/amuse/openSUSE_11.4 amuse
    zypper --gpg-auto-import-keys refresh amuse
    zypper --gpg-auto-import-keys refresh gcc
    echo "install amuse inside the container (post)"
    zypper -n install --force-resolution libstdc++6 amuse
