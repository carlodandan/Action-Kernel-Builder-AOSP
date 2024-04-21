## Action-Kernel-Builder-AOSP
Compile using the kernel build script similar to how Android Open Souce Project build one.

### Pre-requisite
* Kernel Manifest, it should consist of all the repositories and tools you need for building. Kindly check this [kernel/manifest](https://android.googlesource.com/kernel/manifest/) from AOSP or my personal collection of [kernel/manifest](https://github.com/cd-Crypton/android_kernel-manifest) for reference. Just pick a branch that is closely similar to your target kernel.

* A customized build.config.xxxxx, check this for reference [build.config.sm6375](https://github.com/carlodandan/android_kernel_samsung_sm6375/blob/A14/build.config.sm6375) for samsung/sm6375 that consists of all the make commands needed for compiling. Most of the commands are from [build.config.common](https://github.com/carlodandan/android_kernel_samsung_sm6375/blob/A14/build.config.common) here.

### Step
* Fork this repository.
* Go to Action Tab, then in left side, you'll see workflows - tap Kernel Builder.
* Click the `Run workflow` dropdown in right side of the screen, then complete the details needed.
    * `MANIFEST_URL`: Enter your kernel manifest URL.
    * `MANIFEST_BRANCH`: Enter your kernel manifest branch.
    * `BUILD_CONFIG`: Enter your customized build.config file here. (See pre-requisite above for details)
    * `KERNEL_IMAGE_NAME`: Enter your target kernel image name.
    * `ANYKERNEL3`: Just tick the box if you want to make a flashable kernel zip.
* Then click the green button - `Run workflow`.
* Check the release for the built kernel image.
