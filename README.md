# script-for-cse489-p2-exp
A simple script that will run the two experiments required for the documentation part of this project.

The script will not run if its not located in the 'grader' directory of your project, this is because it needs to find the 'run_experiments' script.

The script will also ask you to give it the path to where your abt, gbn ,and sr binaries are located (you can enter either an absolute path or relative path e.g /home/<UBIT>/cse489/p1/<UBIT> or ../<UBIT>, i would go with the second option as its less typing)

The script will create two folders 'exp1' and 'exp2'

## Folder structure 

The exp1 folder will contain...

```
exp1 [folder]

  -abt [folder]

  -gbn[folder]

      -w10 [folder]    <- for all experiments of window size 10

      -w50 [folder]    <- for all experiments of window size 50

  -sr[folder]

       -w10 [folder]    <- for all experiments of window size 10     

       -w50 [folder]    <- for all experiments of window size 50

```

The second folder will contain...

    
```
exp2[folder]

   -abt[folder]

   -gbn [folder]

       -w10 [folder]    <- for all experiments of window size 10     

       -w50 [folder]    <- for all experiments of window size 50

       -w100 [folder]    <- for all experiments of window size 100     

       -w200 [folder]    <- for all experiments of window size 200

       -w500 [folder]    <- for all experiments of window size 500

   -sr[folder]

       -w10 [folder]    <- for all experiments of window size 10     

       -w50 [folder]    <- for all experiments of window size 50

       -w100 [folder]    <- for all experiments of window size 100     

       -w200 [folder]    <- for all experiments of window size 200

       -w500 [folder]    <- for all experiments of window size 500    
```
 
## File naming 

All output files will automatically be placed in one of these folders depending on what experiment the script is running.

For example if i want to run experiments on go-back-N with window size 50, 0.1 loss, and 0.2 corruption on the first experiment then the script will store it in 'exp1/gbn/w50/'

as a file named 'gbn_**l**0.0**c**0.0**w**50'.   


File naming are as follows <binaryName>_**l**<loss probability>**c**<corruption probability>**w**<window size>  (with no space)


example lets say I run an experiment on selective-repeat (**sr**) with

**l**oss = 0.2

**c**orruption = 0.2

**w**indow size = 100


The corresponding output file will look like 

sr_**l**0.2**c**0.2**w**100

## Other Info
Feel free to change it to your needs

Don't forget to make it executable if its not already with 
```chmod +x gen_exp.sh``` 
