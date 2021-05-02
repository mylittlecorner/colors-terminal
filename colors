#!/usr/bin/env bash
# Bold
col[0]='\033[1;30m'       # Black
col[1]='\033[1;31m'         # Red
col[2]='\033[1;32m'       # Green
col[3]='\033[1;33m'      # Yellow
col[4]='\033[1;34m'        # Blue
col[5]='\033[1;35m'      # Purple
col[6]='\033[1;36m'        # Cyan
col[7]='\033[1;37m'       # White

arr=${1:-$(</dev/stdin)}

textcolor() {
	declare -a arr=("${!1}")
        declare -a col=("${!2}")
	j=0
	for (( i=0 ; i < ${#arr} ; i++  ))
	do
		j=$((j+1))
		if [[ j -eq 7 ]]; then
		j=0
		fi
		arrVar+="${col[$j]}${arr:$i:1}"
	done
	ret="${arrVar[@]}${col[7]}"
}

textcolor arr[@] col[@]
echo -e $ret
