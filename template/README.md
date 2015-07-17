# Templates to gather external information

Global **info.yaml** file is processed to obtain some human friendly *digits* as **VERSION**.

Besides, extra basic external information to be included is **GIT COMMIT HASH**. This way *code* and *documentation* are related by this piece of information.

![width=450px](https://github.com/xue2sheng/GenealogicalTree/blob/develop/image/cmake.png)

As well information on the machine where **cmake** was invoked is collected.

**Note:** Take into account that **the last commit** information will be processed; if there are new changes not yet committed, they will be included anyway. So in order to generate *final official* documentation first commit all your changes, generate the documentation and, if needed, commit that generated document.

**Note:** On Windows system it's supposed that *awk* is available at command line. For example, usual **GIT** installation provides a *GIT Bash* environment.


## Human friendly version 

Three digits can be independently updated at *CMakeLists.txt* as human friendly version for both **HARDCODED** and **DYNAMIC** code versions. As well those digits will be used by documentation templates.

## GIT Commit Hash  

In order to add the specific **git commit hash** into code & documentation, *templates* are defined in the *template* folder for **Doxyfile**, **header.tex** & **version.h** files.

![width=400px](https://github.com/xue2sheng/GenealogicalTree/blob/develop/image/version.png)

In order to **speed up** local compilations and let us hardcode our locally generated files, it's possible to instruct *cmake* to use this hardcoded header instead of usual GIT one.

The parameter to pass onto **cmake** is **VERSION_HARDCODED**:

          cmake <rest of options> -DVERSION_HARDCODED=TRUE ..

