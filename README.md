### NAME: SURYA P <br>
### REG NO: 212224230280

# EX. No. 1 : LINUX PROCESS API - FORK(), WAIT(), EXEC()

# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:

## C Program to create new process using Linux API system calls fork() and getpid() , getppid() and to print process ID and parent Process ID using Linux API system calls

```
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{
//variable to store calling function's process id
pid_t process_id;
//variable to store parent function's process id
pid_t p_process_id;
//getpid() - will return process id of calling function
process_id = getpid();
//getppid() - will return process id of parent function
p_process_id = getppid();
//printing the process ids
//printing the process ids
printf("The process id: %d\n",process_id);
printf("The process id of parent function: %d\n",p_process_id);
return 0; }
```

##OUTPUT

<img width="860" height="633" alt="image" src="https://github.com/user-attachments/assets/a7b1bcd8-c28c-4a8c-bf45-5fcd4ccb002a" />

## C Program to execute Linux system commands using Linux API system calls exec() , exit() , wait() family
```
 #include <stdio.h>
 #include<stdlib.h>
 int main()
 { int pid; 
pid=fork(); 
if(pid == 0) 
{ printf("Iam child my pid is %d\n",getpid()); 
printf("My parent pid is:%d\n",getppid()); 
exit(0); } 
else{ 
printf("I am parent, my pid is %d\n",getpid()); 
sleep(100); 
exit(0);} 
}
```


# OUTPUT:
<img width="902" height="253" alt="image" src="https://github.com/user-attachments/assets/d6415937-f68e-4b06-ae2b-a15c00833435" />

# RESULT:
The programs are executed successfully.
