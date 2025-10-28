# How to find the JWT secret on local Supabase container?


```bash
# 1) Find the auth/gotrue container
docker ps --format "table {{.Names}}\t{{.Image}}\t{{.Status}}" | grep -i -E "auth|gotrue"

# 2) Print the env var
docker exec -it <AUTH_CONTAINER_NAME> printenv | grep -i GOTRUE_JWT_SECRET
```
