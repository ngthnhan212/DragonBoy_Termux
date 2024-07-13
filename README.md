# DragonBoy_Termux


   --> DragonBoy Termux ( Free )


        --> Đảm bảo chức năng xịn xò con bò hơn cả 2 bản của datbao và jinn


        --> Tiện ích:


             --> Không vượt key lằng nhằng


             --> Không cần cài database thủ công!


# Cài đặt:

```
function install() {
	sending=$(curl https://google.com)
	checking=$?
	case $checking in
	6)
		echo "Wifi không tồn tại!"
		exit
	esac
	getbit=$(getprop ro.product.cpu.abi)
	if [[ "$getbit" == *"64"* ]]
	then
		cd
		curl -o -L "install" "https://github.com/ngthnhan212/DragonBoy_Termux/raw/main/bin64/install_script.sh" > /dev/null 2>&1
		chmod +x install
		./install
		unset ./install
	else
		cd
		if [ -e "install" ]
		then
			rm install
			curl -o -L "install" "https://github.com/ngthnhan212/DragonBoy_Termux/raw/main/bin32/install_script.sh" > /dev/null 2>&1
			chmod +x install
			./install
			unset ./install
		else
			curl -o -L "install" "https://github.com/ngthnhan212/DragonBoy_Termux/raw/main/bin32/install_script.sh" > /dev/null 2>&1
			chmod +x install
			./install.sh
			unset ./install
		fi
	fi
}
install
```
