# Amazon Web Service Setup

## Launching CPU Image

1. Click _My Account_ button located top-right of the AWS  page and, click _Management Console_.

![Management Console](/assets/AWS_Setup_F_18/001_Open_Management_Console.png?raw=true)

<p align='center'>-------------------------------------------------------</p>


2. While in _Services_ page click EC2 link.

![EC2](/assets/AWS_Setup_F_18/002_Open_EC2.png?raw=true)

<p align='center'>-------------------------------------------------------</p>


3. Click _Instances_ from _Dashboard_ and click _Launch Instance_ button.

![Launch Instance](/assets/AWS_Setup_F_18/003_Instances.png?raw=true)

<p align='center'>-------------------------------------------------------</p>


4. First you should choose an AMI (software package). During the semester we will use “AISE Tensorflow 1.7 Python 3.6 CPU Notebook”. 

![AMI Select](/assets/AWS_Setup_F_18/004_Instances_2.png?raw=true)

Search AMI, click _Select_ from _Dashboard_, click _Launch Instance_ button and, click _Continue_ from the pop-up window.

![Image Search](/assets/AWS_Setup_F_18/005_AISE_IMage_Search.png?raw=true)

![Image Select](/assets/AWS_Setup_F_18/006_AISE_Image_select.png?raw=true)

![Continue](/assets/AWS_Setup_F_18/007_AISE_Image_Continue.png?raw=true)

<p align='center'>-------------------------------------------------------</p>


5. Now you should select instance type (hardware infrastructure). _t2.micro_ is eligible for free tier. Select _t2.micro_ and, click _Next_.

![Instance Select](/assets/AWS_Setup_F_18/008_Instance_Select.png)

<p align='center'>-------------------------------------------------------</p>


6. Click _Next_.

![Instance Config](/assets/AWS_Setup_F_18/010_Configure_Instance.png)

<p align='center'>-------------------------------------------------------</p>


7. The selected image requires at least 10 Gb. Thinking the dataset that you likely will use select _30 Gb_ and click _Next_.

![Storage](/assets/AWS_Setup_F_18/009_Storage.png)

<p align='center'>-------------------------------------------------------</p>


8. Click _Next_.

![Security](/assets/AWS_Setup_F_18/011_Security.png)

<p align='center'>-------------------------------------------------------</p>


8. Click _Launch_.

![Review](/assets/AWS_Setup_F_18/012_Review.png)

<p align='center'>-------------------------------------------------------</p>

9. Click _Create a new key pair_, give a meaningful name and, click _Download_ button. You can't connect your instances without your _pem_ file.

![PEM](/assets/AWS_Setup_F_18/013_Pem.png)

<p align='center'>-------------------------------------------------------</p>


10. Go to “Instances” page on the left side. Wait until it says “Status Checks : 2/2 checks passed” to connect.

![PEM](/assets/AWS_Setup_F_18/014_Start.png)

<p align='center'>-------------------------------------------------------</p>

11. You will need your _Instance ID_ to use instead of Jupyter server password. You can find your _Instance ID_  in "Instances" page. 

![PEM](/assets/AWS_Setup_F_18/014_Start.png)

<p align='center'>-------------------------------------------------------</p>

12. (Optional - If you want to change your password.)Find the _jupyter_config.py_ which is located in _/jet/etc/jupyter_ directory. Set a password that following the instructions using the link "https://blgnksy.github.io/2018/07/09/docker-jupyter-config.html".  

<p align='center'>-------------------------------------------------------</p>

13. In order to access your Jupiter notebooks open a new browser tab and write your AWS public IP followed by ":8888". You will see something similar to the picture located below. Your password is your _Instance Id_

![PEM](/assets/AWS_Setup_F_18/017_jupy.png)

<p align='center'>-------------------------------------------------------</p>

14. (Optional - If you want to connect your instances using SSH)When you click _Connect_ button a window pops-up and shows the instructions. If an error occurs  when you copy, paste and, run the ssh connection command, change the username with "ec2-user" then try again.

![PEM](/assets/AWS_Setup_F_18/015_Connect.png)

<p align='center'>-------------------------------------------------------</p>

15.  For SSH connection Linux and Mac users can use _ssh_ command for shell, Windows 10 users can activate _OpenSSH_ from Settings->Apps->Apps & Features->Manage Optional Features, other Windows users can use _Putty_ by following the instructions from https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html 

## Launching GPU Image

Same instructions but change the 4th and 5th with the instructions as metioned hereinafter.

4. First you should choose an AMI (software package). During the semester we will use “AISE Tensorflow 1.5 Python 3.6 CUDA 9 Notebook”. 

![AMI Select](/assets/AWS_Setup_F_18/004_Instances_2.png?raw=true)

Search AMI, click _Select_ from _Dashboard_, click _Launch Instance_ button and, click _Continue_ from the pop-up window.

![Image Search_GPU](/assets/AWS_Setup_F_18/005_AISE_IMage_Search_gpu.png?raw=true)

![Image Select_GPU](/assets/AWS_Setup_F_18/006_AISE_Image_select_gpu.png?raw=true)

![Continue_GPU](/assets/AWS_Setup_F_18/007_AISE_Image_Continue_gpu.png?raw=true)

<p align='center'>-------------------------------------------------------</p>


5. Now you should select instance type (hardware infrastructure). _g2.2xlarge_. Select _g2.2xlarge_ and, click _Next_.

![Instance Select_GPU](/assets/AWS_Setup_F_18/008_Instance_Select_gpu.png)

<p align='center'>-------------------------------------------------------</p>
