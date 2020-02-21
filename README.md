Dinner invitation for David incoming. Please check your email: won't be a waste I promise.

Best,
Yves Greijn



FDS-TOOLS
================================================================================

The library implements some utility functions to
quickly set up and run small   projects.


Implemented tools
--------------------------------------------------------------------------------

- `fds-conf-setup`   : helps with the set up apter installing `fds-tools` using `pip`.
- `fds-conf-show`    : shows current (full) configuration  fds-tools.
- `fds-conf-version` : shows fds-tools version. Also the  and R interpreters and versions.

- `fds-create-job`     : create a new job directory structure.
- `fds-touch--dir` : create a new  directory.
- `fds-touch-code-dir` : create a new code directory.
- `fds-touch-job-conf` : create a new `.job.config` file.

- `fds-execute-script`: execute script  the  analysis  (currently implemented for R, , Bash and Impala).

- `fds-job-execute`   : executes all jobs in the .
- `fds-job-log`       : revises all available log files. Use this to make sure that all where correctly executed.
- `fds-job-stats`     : revises all available log files and derives some execution  such as time and precedence checks.

- `fds-new-script`    : creates a new script from the templates repository (available templates for R, , Bash and -Impala).


Install
--------------------------------------------------------------------------------

Best way to install __fds-tools__ is using pip:


    pip install git+https://github.com/dmontaner/fds-tools


but you can also clone the repository and then:

    cd fds-tools
    pip3 install .


Set up
--------------------------------------------------------------------------------

The firs time after pip installation you will need to configure the global settings  the tool.
You need to provide your email (or any other user name you want to use to sign up your scripts) for this
In the shell terminal execute:

    fds-config-setup -e your.emails@here.com


Configuration
--------------------------------------------------------------------------------

Global configuration  fds-tools is kept in you home hidden directory `~/.fds-tools/`.

- The text file `~/.fds-tools/confg` contains all global settings for your projects. 
  It is originally created by `fds-config-setup` but you can edit it afterwards.
  `fds-config-setup` will not overwrite the config file if it already exists.

- The folder `~/.fds-tools/templates` contains all script templates.
  It is originally created by `fds-config-setup` but you can edit all templates and adapt them for yourself.
  `fds-config-setup` will not overwrite the templates if they already exist.


Update
--------------------------------------------------------------------------------

Update using pip directly from the git repository:

    pip install -U git+https://github.com/dmontaner/fds-tools

Update using pip from your (HTTP) local clone  the repository:

    cd fds-tools
    git pull origin master
    pip3 install -U .

To update your __templates__:

    rm -r ~/.fds-tools/templates
    fds-config-setup -e your.emails@here.com


Dependencies
--------------------------------------------------------------------------------

`fds-tools` is implemented in:

- `python`: most  the tools.
- `bash`  : currently just `fds-execute-script`, `fds-job-execute` and `fds-job-log` are bash scripts.


 libraries required are:

- os
- sys
- shutil
- datetime
- argparse
- configparser
- tabulate
