
## Setup Process

For a simple jekyll-based website using the comprehensive minimal mistakes theme, locally developpable and previewable without internet access.

### Install Jekyll

* Ensure you have a suitable version of Ruby installed, for example on a recent version of Windows 10:
  * Enable linux subsystem for windows: 
    * Open the Start Menu (eg hit the windows key)
	* Type `powershell`
	* When powershell is highlighted, press `Ctrl-Shift-Enter` to open an Administrator Powershell prompt
	* In the resulting Administrator window, paste: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`
	* (wait for stuff to complete, accept the **violent reboot** when ready)
	* Open the Microsoft Store and get "Ubuntu" 
	* (wait for that to complete - takes a while as well)
    * In a `bash` window, update the installation: `sudo apt-get update -y && sudo apt-get upgrade -y`
  * Install Ruby, with user-level Gem support. Eg in a bash window:
    * `sudo apt-add-repository ppa:brightbox/ruby-ng`
    * `sudo apt-get update`
    * `sudo apt-get install ruby2.5 ruby2.5-dev build-essential dh-autoreconf`
    * Add a user-local Gem folder; in `nano ~/.bashrc`

            export GEM_HOME=$HOME/gems
            export PATH=$HOME/gems/bin:$PATH
    * Close & reopen bash to get the new .bashrc config
    * `gem update`
* Ensure you have jekyll installed; eg in the environment above, in a `bash` window:
  * `gem install jekyll bundler`
  * Check it's working: `jekyll -v`
* Ensure you have have the "zlib" headers for older jekyll support (for github-pages Gem):
   * `sudo apt-get install zlib1g-dev`
* Ensure you have a suitable git-supporting text editing environment, for example:
  * Download+Install Git: https://git-scm.com/download/win
  * Download+Install Visual Studio Code: https://code.visualstudio.com/download

### Get & Serve this website

* Get the code, eg in a git bash window, `git clone https://github.com/J-R-Pace/JRPace.git /c/JRPace-Website`
* Get the gems & try first serve, in a bash window:
  * `cd /mnt/c/JRPace-Website/docs`
  * `bundle update`
  * `bundle exec jekyll serve`
* ADD STEPS TO SET UP SHORTCUT(S)

## Authoring Workflow

To minimize the github-pages-related and jekyll-related overhead, here's what we've pared the process down to:

* IN YYY, do XXXXXX
* Review the results
* When ready (and connected to the internet), NNNNNNNN
  * Due to the Workspace-level settings in this project, Visual Studio Code should handle pushing and pulling automatically.

For a simple single-author flow, this seems to work fine, with few or no exceptions encountered.

Situations that would require a little more knowledge of Git include:

* Having multiple people working on the site content
* Modifying the site from more than one computer


