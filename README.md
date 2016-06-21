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
```
the response should be
```
NA/NaN argument

In call:
"test":"data"
```


# test json file
```
{
  "0": {
    "id": "1111",
    "age": "2016-04-02T22:00:00.000Z",
    "dob": "2016-04-02T22:00:00.000Z",
    "dot": "2016-04-02T22:00:00.000Z",
    "sex": "0",
    "education": "3",
    "test": [
      {
        "id": "DART-raw_score",
        "label": "raw score",
        "Dataset": "DART",
        "SPSS name": "DARTRAW",
        "highborder": "100.001",
        "highweb": "100",
        "lowborder": "20",
        "lowweb": "0",
        "value": 55
      },
      {
        "id": "HADS-anxiety",
        "label": "Anxiety scale",
        "Dataset": "HADS",
        "SPSS name": "HADS_anxiety",
        "highborder": "9.001",
        "highweb": "21",
        "lowborder": "0",
        "lowweb": "0",
        "value": 12
      },
      {
        "id": "HADS-depression",
        "label": "Depression scale",
        "Dataset": "HADS",
        "SPSS name": "HADS_depression",
        "highborder": "9.001",
        "highweb": "21",
        "lowborder": "0",
        "lowweb": "0",
        "value": 12
      },
      {
        "id": "HADS-total",
        "label": "total score",
        "Dataset": "HADS",
        "SPSS name": "HADS_total",
        "highborder": "13.001",
        "highweb": "42",
        "lowborder": "0",
        "lowweb": "0",
        "value": 12
      }
      ]
  },
  "1": {
    "id": "2222",
    "age": "2016-04-02T22:00:00.000Z",
    "dob": "2016-04-02T22:00:00.000Z",
    "dot": "2016-04-02T22:00:00.000Z",
    "sex": "1",
    "education": "2",
    "test": [
      {
        "id": "DART-raw_score",
        "label": "raw score",
        "Dataset": "DART",
        "SPSS name": "DARTRAW",
        "highborder": "100.001",
        "highweb": "100",
        "lowborder": "20",
        "lowweb": "0",
        "value": 55
      },
      {
        "id": "HADS-anxiety",
        "label": "Anxiety scale",
        "Dataset": "HADS",
        "SPSS name": "HADS_anxiety",
        "highborder": "9.001",
        "highweb": "21",
        "lowborder": "0",
        "lowweb": "0",
        "value": 12
      },
      {
        "id": "HADS-depression",
        "label": "Depression scale",
        "Dataset": "HADS",
        "SPSS name": "HADS_depression",
        "highborder": "9.001",
        "highweb": "21",
        "lowborder": "0",
        "lowweb": "0",
        "value": 12
      },
      {
        "id": "HADS-total",
        "label": "total score",
        "Dataset": "HADS",
        "SPSS name": "HADS_total",
        "highborder": "13.001",
        "highweb": "42",
        "lowborder": "0",
        "lowweb": "0",
        "value": 12
      }
      ]
  },
  "conf": "99",
  "sig": "oneTailedRight",
  "nomative": "2016-01-14"
}
```
