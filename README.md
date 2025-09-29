# fire_alarm

1. Setup toolchain: 
- Set up môi trường: Tải file này và giải nén trong ổ C (hoặc đâu cũng được): https://dl.espressif.com/dl/esp32_win32_msys2_environment_and_toolchain-20181001.zip
sau khi giải nén sẽ thấy thư mục "msys32". Vào thư mục và chạy mingw32.exe (màu xám).
- Tải tool chain: https://dl.espressif.com/dl/xtensa-lx106-elf-gcc8_4_0-esp-2020r3-win32.zip , giải nén vào thư mục /home/<tên_user> trong folder /msys32.

2. Tải sdk:
- git clone --recursive https://github.com/pfalcon/esp-open-sdk.git
- git clone --recursive https://github.com/Superhouse/esp-open-rtos.git
clone hai cái này trong thư mục /home/<tên_user>
- Copy folder xtensa trong \esp-open-sdk\lx106-hal\include\ vào thư mục \esp-open-rtos\include
- Copy file "libhal.a" vào thư mục \esp-open-rtos\lib

3. export biến global:
   Thêm 3 dòng sau vào file .bashrc trong thư mục /home/<tên_user>:
export PATH="$HOME/xtensa-lx106-elf/bin/:$PATH"
export PATH="$HOME/esp-open-sdk/esptool:$PATH"
export PATH="/mingw32/bin:$PATH"
   
