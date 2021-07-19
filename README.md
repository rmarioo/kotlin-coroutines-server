# Spring Boot example server

This project contains example Controller serving a few endpoints.

Each endpoint:

* is delayed by a random number of milliseconds (using delay() suspending function, that's why coroutines are present)
* returns a string: "ok" or "not ok" (depending on simple logic)

To run a server (by default uses netty on port 8087):
```bash
$ ./gradlew bootRun
```

Note check max open file number

```
sysctl kern.maxfiles
sysctl kern.maxfilesperproc
```

To increase the max number of files opened do something like this  

```
sudo sysctl -w kern.maxfiles=1000000
sudo sysctl -w kern.maxfilesperproc=1000000
```

This change is temporary see more info here https://superuser.com/questions/433746/is-there-a-fix-for-the-too-many-open-files-in-system-error-on-os-x-10-7-1



