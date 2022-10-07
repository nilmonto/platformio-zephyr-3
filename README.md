# platformio-zephyr-3

Work still in progress (need help bytheway), trying to translate new Zephyr 3 CMakeLists.txt format to platformio-build*.py scripts.

## Prepare to use zephyr from mainline on your Platformio VSCode IDE:
- Backup *package.json* file (will be needed after)
- Setup framework-zephyr on your *platformio.ini* file:

```shell
platform_packages =
    framework-zephyr @ <Zephyr git repository URL>
```

- Setup scripts from this repository on your installed zephyr package:

```shell
cd ~/.platformio/packages/framework-zephyr/scripts
git clone git@github.com:nilmonto/platformio-zephyr-3.git
```

- Perform a clean and then a Build command, hopefully it will build
> A warn about orphan section related to *__device_handles_pass1* happens due to still missing consideration about 3 phase build process done on
Zephyr 3.x, which considers zephyr_pre0, zephyr_pre1 and zephyr_final process (instead of only zephyr_prebuilt and zephyr_final as up to Zephyr 2.x)


To be fair, I haven't had time to test my applications but it would be a good start point to anyone that, like me, would like to have new features and still use platformio IDE environment. Any help is welcome =)