ffmpeg-intelqsv
=========

This role will build ffmpeg with intel quicksync support on an Ubuntu server. This was primarily used for dizquetv but could really be used for anything with ffmpeg.

Requirements
------------

The role will automatically downlaod all required packages and source code to build. From a hardware standpoint you do need an intel cpu that supports QuickSync. If it's a VM make sure you've passed the correct cpu support to the VM.

Role Variables
--------------

default:

* bin: this is where all of the executables will go.
* src_base: where the source code goes

vars:

* vaapi_src: source code location for va-api
* ffmpeg_build: build folder for ffmpeg
* ffmpeg_src: base folder for ffmpeg and tools
* vaapi_workspace: base folder for va-api tools
* *_repo: github repos
* *_src: source code location
* *_build_src: build folders for individual tools
* nasm: nasm version to downlaod. At time of checkin current version is **nasm-2.14.02**
* nasm_dl: download path for nasm
* libvorbis: libvorbis version to download. Currently **libvorbis-1.3.6**
* libvorbis_dl: libvorbis download path
* ffmpeg_pkgs: required packages

Example Playbook
----------------

You can use the sample playbook included and run it as follows:

```console
ansible-playbook build-ffmpeg.yml -i server-to-run-against, 
```

To use this in your own playbook just copy ffmpeg-intelqsv to your own roles folder.

License
-------

BSD

Author Information
------------------

* Name: Shimron Trammell
* email: shimmyt@gmail.com
* discord: shimmyt#7131
