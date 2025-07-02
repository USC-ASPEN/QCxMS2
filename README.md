#**Setting Up QCxMS2**
#Log into CARC: 
`ssh <username>@discovery.usc.edu`
#Navigate into your directory within project brieda: 
`cd /project/brieda_368/<username>`
#Create test directory for qcxms2:
`mkdir <testQC>`

#Navigate into project brieda: 
`cd /project/brieda_368`
#Copy input (adamantane.xyz) to your personal directory: 
`cp adamantane.xyz <username>`
#Navigate into personal directory:
`cd /project/brieda_368/<username>`
Create run_qcxms2.slurm file by copying and pasting from run_qcxms2.slurm tab:
`nano run_qcxms2.slurm` 
Update run_qcxms2.slurm file with your personal email (you can also change input file/run time): 
`nano run_qcxms2.slurm `
Within nano, you can rewrite the script, then exit and save your changes 
**ONLY edit your own script**

Copy updated input (adamantane.xyz) and job file (run_qcxms2.slurm) to your test directory: 
`cp adamantane.xyz run_qcxms2.slurm <testQC>`
Within TEST DIRECTORY run: 
`sbatch run_qcxms2.slurm`
Go to QCXMS2 (Job Submission Google Sheet)[https://docs.google.com/spreadsheets/d/1DPYk6q5WWcy38770s3foaJSAHkoZPg71ZURx3tFMewE/edit?gid=958390659#gid=958390659 
] and Input Information
Job is now submitted to CARC, so wait for CARC to email you when your job is finished. 
To check on personal job run: `myqueue`

Once you get an email saying the job is finished, you can navigate back into your personal directory 
The output will be stored within qcxms2.out.
To see the output file, run `nano qcxms2.out`
*NOTE: old output file will get overwritten when starting a new job, so make sure to check qcxms2.out before starting a new job or change output file within .slurm file for different jobs.
