Trying to fix and build rpms for initial installation of ros_deps. 

Figured out that the best solution is to either follow fully the recommendation given for RPMs, as they are created for CentOS, or to stick to one on the Fedora versions, and to make a build that is additionally filled with both CentOS and Fedora (25) RPMs.

For now, I'm sticking to 25 Fedora, when I don't have a chance of finding the package needed.

There are also several complications that I met on the way while I was trying to compile/recompile some of the RPMs. There were several cases of extensive usage of RPMs with same name, however, in such cases, the most problematic part was that the packages were not supposed to be working at the same time, as (for ex.) one was designed for use under CentOS and the other for Fedora(25)

Now, I'm stuck with ahving major dependencies, like:
```
No package gazebo-devel available.
No package python-qt5 available.
No package ffmpeg-devel available.
No package pydot available.
No package python-qt5 available.
```
Having these, and trying to find a workaround for the gazebo, I'm stuck with conflicting versions of LibHalf.so (6 or 12?) 

And Gazebo wont install unless I install the player, which is a community-created project on Git, as I understood.
```
player-devel is needed by gazebo-7.4.0-2.el7.x86_64
```
