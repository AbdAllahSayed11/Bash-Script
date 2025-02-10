lab3 - bash script

#!/usr/bin/bash


#1
#read -p " please write any word " character
#case $character in

#[A-Z])
#	echo upper character
	# ;;
#[a-z])
#	echo lower character
# ;;
#[A-z])
#	echo mixed character
	# ;;	
#[0-9])
#	echo numbers
	# ;;
#*)
#	echo Nothing enterd
#esac


#2
#read -p " please write any word " word
#case $word in

#[A-Z]*)
#	echo upper word
	# ;;
#[a-z]*)
#	echo lower word
	# ;;
#[A-z]*)
#	echo mixed word
	# ;;	
#[0-9]*)
#	echo numbers
	# ;;
#*)
#	echo Nothing enterd
#esac

#3
#dir="$1"
#if [[ -r $1 ]]; 
#then
 #   chmod -R +x "$dir"
  #  echo "execute permissions have been added to $dir and all its contents."
#else
 #   echo "error: $dir is not a valid or readable directory."
#fi


#dir="$1"
#    for item in "$dir"/*; 
 #   do
 #       if [[ -f "$item" ]]; 
 #       then
 #           chmod +x "$item"
 #           echo "x permission added to file: $item"
 #       elif [[ -d "$item" ]];
 #        then
 #           chmod +x "$item"
 #           echo "x permission added to directory: $item"
 #       fi
 #   done



#4

#dir="$1"
#backup_dir="$2"

#    for file in "$dir"/*; 
 #   do
 #       if [[ -f "$file" ]]; 
 #       then
 #           cp "$file" "$backup_dir"
#            echo "Backup of $file created at $backup_dir"
#       	 fi
#    done
#    echo "complete for files in this dir $dir."
#

#



#5

#mail_file="fmail"  #or path

#for user in $(cut -d: -f1 /etc/passwd); 
#do

  #  mail -s "$user" < "$mail_file"
 #   echo "mail sent to $user"
#done


#6

#username=$(whoami)

#mail_file="/var/mail/electronica"

#last_size=$(stat --format=%s "$mail_file")

#while true;
 #do
#    current_size=$(stat --format=%s "$mail_file") 
#
#    if [[ "$current_size" -gt "$last_size" ]]; 
#    then
#        echo " new mail sent"
 #       last_size="$current_size" 
#    fi
#
#    sleep 10
#done






#username=$(whoami)
#mail_file="/var/mail/electronica" 
#last_content=$(cat "$mail_file")
#
#while true; 
#do
#    current_content=$(cat "$mail_file")
#
#    if [[ "$current_content" != "$last_content" ]]; 
#    then
#        echo "new mail sent"
#        last_content="$current_content" 
#    fi
#
#    sleep 10
#done







#Bonus 7 
#will be error 
#((n2=$n2+1)) without () it will be string 
#((n1=$n1+1)) arthematic operation
#if we change it  the output will be like (n1=1,n2=2,n1=2,n2=3,n1=3,infint)




#8
#PS3"please select command"
#select name in "ls" "ls -a" "exit"
#do
#case $name in
#"ls")
#	ls 
#	;;
#"ls -a")
#	ls -a 
#	;;
#"exit")
#	break
#	;;
#*)
#	echo ERROR
#esac
#done



# 9  && 10 

#read -p "enter array size: " size
#sum=0
#for ((i=0;i<$size;i++))
#do
#	read -p "please enter elem $((i+1)): " arr[$i]
#	((sum+=${arr[$i]}))
#done
#echo ${arr[@]}
#echo $sum
#((avg=$sum/$size))
#echo $avg

#for num in $@
#do
#	echo $num
#done


#11

#square() {

 #    num=$1
#     square=$((num * num))
#}

#square 9
#echo $square







#!/bin/bash

declare n1
declare n2
n1=1
n2=1

while test $n1 -eq $n2
do
    n2=$((n2 + 1)) 
    echo  $n1
   
    if [ $n1 -gt $n2 ]; 
    then
        break
    else
        continue
    fi
    
    n1=$((n1 + 1))
    echo $n2
done













