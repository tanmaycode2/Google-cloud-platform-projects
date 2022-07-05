# Create a Compute Engine Virtual Machine Instance

In this section, you use the Cloud Console to provision a new Compute Engine (VM) instance.

Create and connect to a virtual machine in the Console by clicking Navigation menu > Compute Engine > VM Instances.

## Install software on the VM instance
In the SSH session, to update the Debian package list, execute the following command:
`sudo apt-get update`

To install Git, execute the following command:

`sudo apt-get install git`

When prompted, enter Y to continue, accepting the use of additional disk space.

###To install Python, execute the following command:

`sudo apt-get install python3-setuptools python3-dev build-essential`

Again, when prompted, enter Y to continue, accepting the use of additional disk space.

To install pip, execute the following command:

`curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`

`sudo python3 get-pip.py`

### Configure the VM to Run Application SoftwareIn this section, you verify the software installation on your VM and run some sample code.

Verify Python installationStill in the SSH window, verify the installation by checking the Python and pip version:

`python3 --version`

`pip3 --version`

The output provides the version of Python and pip that you installed.

Clone the class repository:

`git clone https://github.com/GoogleCloudPlatform/training-data-analyst`

Change the working directory:

`cd ~/training-data-analyst/courses/developingapps/python/devenv/`


Run a simple web server:

`sudo python3 server.py`

Return to the Cloud Console VM instances list (Navigation menu > Compute Engine > VM Instances), and click on the External IP address for the dev-instance.

A browser opens and displays a Hello GCP dev! message from Python.

Return to the SSH window, and stop the application by pressing Ctrl+C.

Install the Python packages needed to enumerate Compute Engine VM instances:

`sudo pip3 install -r requirements.txt`

Now list your instance in Cloud Shell. Enter the following command to run a simple Python application that lists Compute Engine instances. Replace <PROJECT_ID> with your Project ID and <YOUR_VM_ZONE> is the region you specified when you created your VM. Find these values on the VM instances page of the console:

`python3 list-gce-instances.py <PROJECT_ID> --zone=<YOUR_VM_ZONE>`

Your instance name should appear in the SSH terminal window.

Example output:

`Instance in project qwiklabs-gcp-04-bcdd9ef8f952 and zone us-central1-a:`
 `- dev-instance`

Return to the SSH window, and stop the application by pressing Ctrl+C.

Install the Python packages needed to enumerate Compute Engine VM instances:

`sudo pip3 install -r requirements.txt`

Now list your instance in Cloud Shell. Enter the following command to run a simple Python application that lists Compute Engine instances. 
Replace <PROJECT_ID> with your Project ID and <YOUR_VM_ZONE> is the region you specified when you created your VM. 
Find these values on the VM instances page of the console:

`python3 list-gce-instances.py <PROJECT_ID> --zone=<YOUR_VM_ZONE>`

Your instance name should appear in the SSH terminal window.

Example output:

Instance in project qwiklabs-gcp-04-bcdd9ef8f952 and zone us-central1-a:
 `- dev-instance`
