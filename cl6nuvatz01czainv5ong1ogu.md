## AWK : Linux Command

# Introduction 👋🏽

AWK command is widely used for text processing in the command line. Command is used to select data from the text on the basis of the pattern we provide.

# Syntax of the command

The syntax consists of 4 things

> - *command ( awk )*
> - *options (eg. -f , -F )*
> - *action in quotes( eg. ‘{ print }’ )*
> - *file name ( eg. yourFile.txt )*


# Type of commands


***‘{ action }’*** : is used to specify the actions we want to perform.


![Size Used Avail UseN Mounted on.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660147568262/wwKLWxBTy.png align="left")


# AWK variables

> $0 : Used to get the whole line

> $1 : Used to print the first field of the line or record

> $2 : Used to print the second field of the line or record.

> .

> .

> .

> .

> and so on…

**EX**
If you want to print just the first field of each record.> 


![Filesysten.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660147638244/oghEirtfR.png align="left")

# Options

> - -F
> - -f

### **-F** (Option)
This is used to specify the field separator by default it is blank space.

**Ex:**
We have a file example1.txt with comma(‘ , ’) separated words and you want to get the first words of every records


![This, is, the, perfect, example.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660147722016/-N40IJ4LR.png align="left")

### **-f** (Option)
Used to specify the file containing the awk script. Reads the awk program source from the specified file, instead of the first command-line argument


![Screenshot 2022-08-09 at 7.45.20 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660147737033/b4urzrAK6.png align="left")

# Special Expression Patterns

> - *BEGIN*
> - *END*

### BEGIN :
This special expression is used to execute an expression before starting to execute the first record.
### END :
This special expression is used to execute an expression after executing all the records.


![DISK INFORMATION.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660148497449/ngnweTv6m.png align="left")

# BIULT-IN AWK Variables

> - *NR*
> - *NF*
> - *FS*
> - *RS*
> - *OFS*

### NR (Number of Records) : 
Counts the number of input records (usually lines).

![Screenshot 2022-08-09 at 8.14.39 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660148780667/EsLj07r74.png align="left")

### NF (Number of Fields) : 
Counts the number of fields in the current input record and displays the last field of the file.

![Screenshot 2022-08-09 at 8.17.13 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660148826409/Oh9rgrdBX.png align="left")

### FS (Field separator) : 
Contains the character used to divide fields on the input line. The default separator is space, but you can use FS to reassign the separator to another character

![ubuntu@ip-172-31-41-115-$ cat example1.txt.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660148872466/F4zsLzH71.png align="left")

### RS (Record separator) :
Stores the current record separator character. The default input line is the input record, which makes a newline the default record separator.

![ubuntu@ip-172-31-41-115-$ cat example1.txt.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660148901516/IsaXdFnJh.png align="left")

### OFS (Output Field Separator) :
This stores a Separator which is applied on the output of the awk command.


![then defined OFS (Output Field Separator).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660148930457/4P4tVjyZ8.png align="left")

# AWK Statements

> - *for loop*
> - *while loop*
> - *if-else*
> - *break*


![Screenshot 2022-08-09 at 11.13.47 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660148970582/NIVi9Xlky.png align="left")


# AWK Patterns (regular expression)

Inserting a pattern in front of an action in awk acts as a selector. The selector determines whether to perform an action or not


![Results contain character t'.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660149042059/ov0sOqUZa.png align="left")

# AWK with previous Output

We can also use 'awk' command with the **Output** of previous command as an **Input**.

> ( | ) is used to pass the output of the previous command as an Input for the next command.


![Screenshot 2022-08-11 at 1.55.32 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660206594278/R0vkIAOjU.png align="left")

# Conclusion 🙇🏽‍♂️

In this post, I discussed about AWK command of linux which basically helps us for any text processing on any file.

> **NOTE** : Try these commands on your terminal side by side and experiment with these commands, you will get a lot of ideas for some automation, If not you will get to know in the later posts, so stay tuned...❤️

# Socials 🤝

> [ ***Twitter*** ](https://twitter.com/_s_k_yyy_)

> [ ***LinkedIn*** ](https://www.linkedin.com/in/akash-tiwari-03b3621b7/)

> [ ***Github*** ](https://github.com/akku750156)

