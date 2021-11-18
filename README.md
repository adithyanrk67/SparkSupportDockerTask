# SparkSupportDockerTask

1. Create a custom bridge network with  the name "mynet"
2. Create two docker containers with the above custom network with the alpine image in detached mode.
3.  Ping the containers each other by using the hostname.


>docker network create -d bridge mynet

3de72e37c5a66d685949283214595cc7b6354e19c2fe2f666f7db7ccbf6404cf

>docker network ls

NETWORK ID       NAME       DRIVER      SCOPE

33d2e96aee94     bridge     bridge      local

9eabc33b7208     host       host        local

3de72e37c5a6     mynet       bridge     local

3d2390e6d999     none       null        local



>docker network inspect mynet


>docker pull alpine
>

>docker run -dit --name alpine1 --network mynet alpine ash
>
>docker run -dit --name alpine2 --network mynet alpine ash





>docker attach alpine1

>ping −c 3 alpine2




