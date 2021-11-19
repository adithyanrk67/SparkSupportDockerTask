# SparkSupportDockerTask


>docker network create -d bridge mynet

3de72e37c5a66d685949283214595cc7b6354e19c2fe2f666f7db7ccbf6404cf

>docker network ls

NETWORK ID       NAME       DRIVER      SCOPE

33d2e96aee94     bridge     bridge      local

9eabc33b7208     host       host        local

3de72e37c5a6     mynet       bridge     local

3d2390e6d999     none       null        local






>docker run -dit --name alpine1 --network mynet alpine ash
>
>docker run -dit --name alpine2 --network mynet alpine ash





>docker attach alpine1

#ping −c 3 alpine2

#ping -c 3 google.com


PING google.com (142.250.67.78): 56 data bytes

64 bytes from 142.250.67.78: seq=0 ttl=37 time=64.186 ms

64 bytes from 142.250.67.78: seq=1 ttl=37 time=24.216 ms

64 bytes from 142.250.67.78: seq=2 ttl=37 time=24.379 ms


Endpoint and ping result

--- google.com ping statistics ---

3 packets transmitted, 3 packets received, 0% packet loss

round-trip min/avg/max = 24.216/37.593/64.186 ms




