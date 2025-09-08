№1
grep -o '^[^:]*' /etc/passwd | sort

№2
awk '{print $2, $1}' /etc/protocols | tail -n 5 | tac

№3
text="$*"
len=${#text}
width=$((len+2))
line="+$(printf '%*s' "$width" "" | tr ' ' '-')+"
text_line="| $text |"
 
echo "$line"
echo "$text_line"
echo "$line"

