# Things to add/remove from the Skytap Image (Version xx)
----------------

## To be added
  - In directory _/home/student_, create a subdirectory called _generateSecret_.

  Into that sub-directory _/home/student/generateSecret_, copy all of the five files that you will find inside the attached _generateSecret.zip_ file:

      - _generateSecret.sh_ - `chmod 777` to make this rwx by everyone
      - _mqsc.txt_ - `chmod 666` to make this rw by everyone
      - _serverconf.yaml_ - `chmod 666` to make this rw by everyone
      - _setdbparms.txt_ - `chmod 666` to make this rw by everyone
      - _truststorePassword.txt_ - `chmod 666` to make this rw by everyone

  - Edit the file _/home/student/.profile_ to contain the following 2 lines at the end:

  ``` script
  # call mqsiprofile, so that ACE commands can be run`
  . /home/student/ace-11.0.0.3/server/bin/mqsiprofile
  ```

  - Into directory _/home/student_, place the file _order.json_, and make sure that it is chmod 666 to make it rw by everyone.


## To be removed
  - ACE: all deployed BAR Files (Integration Servers, aka deployed Helm Resources) to be removed **except** for the _inventory_ one.


