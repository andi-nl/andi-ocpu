# andi-ocpu
opencpu service for ANDI

# running docker container
```sh
docker run -t -p 80:80 -p 8004:8004 andinl/andiocpu
```

# talking to the API
```
POST on url <opencpu_server_ip>/library/andistats/R/normcomp/json
```

# testing on the command line
Test on the command line if the opencpu server is running
```
curl http://<ip address>:8004/ocpu/library/andistats/R/normcomp -d "myJSON={'test': 'data'}"
# the response should be
NA/NaN argument

In call:
"test":"data"
```
