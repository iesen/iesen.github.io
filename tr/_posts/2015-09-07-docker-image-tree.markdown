---
layout: post
title:  "Docker image larını tree olarak gösterme"
date:   2015-08-19 11:33:55
published: false
---
 
* Eski docker da şmages --tree olarak vardı.
* https://github.com/justone/dockviz ile artık yapılır.
* docker run --rm -v /var/run/docker.sock:/var/run/docker.sock nate/dockviz images --tree
* brew install graphviz 
* docker run --rm -v /var/run/docker.sock:/var/run/docker.sock nate/dockviz containers -d | dot -Tpng -o containers.png