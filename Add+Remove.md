# Things to add/remove from the Skytap Image (Version xx)
----------------

## To be added/changed
1. In directory _/home/student_, create a subdirectory called _generateSecret_.

  Into that sub-directory _/home/student/generateSecret_, copy all of the five files that you will find inside the attached _generateSecret.zip_ file:

      - _generateSecret.sh_ - `chmod 777` to make this rwx by everyone
      - _mqsc.txt_ - `chmod 666` to make this rw by everyone
      - _serverconf.yaml_ - `chmod 666` to make this rw by everyone
      - _setdbparms.txt_ - `chmod 666` to make this rw by everyone
      - _truststorePassword.txt_ - `chmod 666` to make this rw by everyone

1. Edit the file _/home/student/.profile_ to contain the following 2 lines at the end:

  ``` script
  # call mqsiprofile, so that ACE commands can be run`
  . /home/student/ace-11.0.0.3/server/bin/mqsiprofile
  ```

1. Into directory _/home/student_, place the file _order.json_, and make sure that it is `chmod 666` to make it rw by everyone.

1. Upgrade the ES installation to disable Message Indexing, using the instructions here : https://ibm.github.io/event-streams/administering/modifying-installation/. This will take a couple of minutes.

  The reason is that the Kafka Client inside ACE V11.0.0.4 is so old that the Event Streams UI method way of displaying messages (by indexing) doesn't show ACE-produced messages. A workaround is to disable that message indexing, and this then allows the Event Streams UI to show messages.

1. Make sure that all artefacts are left in the ACE workspace, thus:

  - Start the Ace Toolkit by executing `./ace-v11.0.0.3/ace toolkit`. (Note that the ACE Toolkit may start as a tiny window on the screen. Use the cursor to grab the corner of this screen and expand it.)
  - You should see these three applications: `Customer`, `orders` and `inventory`.

1. Change bookmarks in browser to change _10.0.0.1_ to _mycluster.icp_.

## To be removed
  - ACE: all deployed BAR Files (Integration Servers, aka deployed Helm Resources) to be removed **except** for the _inventory_ one.


