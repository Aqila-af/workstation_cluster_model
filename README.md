# Workstation Cluster

This case study is based on a cluster of workstations.

The system comprises two sub-clusters with N workstations connected in a star topology. The switches connecting each sub-cluster are joined by a central backbone. All components can break down and there is a single repair unit to service all components.

Study under which conditions the system guarantees that the following Quality of Service (QoS) levels are guaranteed:

**minimum QoS**: at least 3N/4 workstations are operational and connected via switches and backbone;

**premium QoS**: at least N workstations are operational and connected via switches and backbone.

## Running the model

```
!apt-get update
#Install Java 17 JDK
!apt-get install openjdk-17-jdk

!git clone https://github.com/quasylab/sibilla

!cd sibilla && ./gradlew build -x test && ./gradlew installDist
!cp -a sibilla/shell/src/dist/scripts/sibilla_py .
!cd sibilla_py && pip install .

import os
os.environ["SSHELL_PATH"]="/content/sibilla/shell/build/install/sshell/"
import sibilla

```
After you have installed [Sibilla](https://github.com/quasylab/sibilla), you can write the code in Sibilla syntax and use Google Colab for the frontend.
