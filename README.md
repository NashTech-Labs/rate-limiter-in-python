# Rate Limiter in Python
Python rate limiter is an utility program to prevent the frequency of an operation from exceeding some defined constraint. At an enterprise level application rate limiter is commonly used to protect underlying services and resources. </br>

# Prerequisite
```
Python3
Flask 
Postman 
```

# How to run 
```
python3 rate_limiter.py
```
![image](https://user-images.githubusercontent.com/76727343/216787747-f4518c87-9231-40e7-9db7-c4999fc50b64.png)

``` Copy the URL -> http://127.0.0.1:5000 ```

Go to Postman and Create new GET HTTP request with above URL, </br>
![image](https://user-images.githubusercontent.com/76727343/216787794-acd860f9-ae08-4159-8668-b18394c38ff8.png)

Now send 3 quick requests (within 5 sec difference between each request), on fourth request you will get message saying "Request blocked due to rate limiting." </br>
Again take a pause of 5 seconds and resend request, it should give a response. </br>

![image](https://user-images.githubusercontent.com/76727343/216787889-1941c5f2-4510-4542-8c14-ddb5c94cf10d.png)
</br>
![image](https://user-images.githubusercontent.com/76727343/216787908-3969fbed-e14a-4eb1-a174-751643f92cbd.png)
</br>
Idea is, within 5 seconds it can have at max 3 request, more than 3 would not be entertained. </br>
----
### Why use rate limiter?
- Used as a defensive measure for the shared services to stop themselves from excessive use, it could be intended/unintended in order to maintain service availability.
- Even though your system is highly available, you should have limits on consumption at some level.
- Rate limiting helps to ensure API-based services to be highly available by reducing chances of failures due to resource failure.
- Rate limiting could be applied at client side as well as server side to ensure maximum throughput and minimum latency accross large distributed systems.
- Useful to avoid resource starvation it could be intentional or unintentional.
    - intentional could be friendly-fire DDoS
    - unintentional could be DDoS

### How Rate limiting is applied in real time?
- It is applied by the service just before the contrained resource, with some resource usage limit margin.

### Use cases
- Managing policies and quotas
- Controlling Flow
- Avoid excess cost
