Steps to run env
1. install docker
2. `cd $GOPATH/src/github.com`
3. clone git https://github.com/fvrepo/port-domain.git in $GOPATH/src/github.com
4. clone git https://github.com/fvrepo/client-api.git in $GOPATH/src/github.com
5. clone git https://github.com/fvrepo/Env.git in $GOPATH/src/github.com
6. `cd ./Env`
7. docker-compose -f env.yml build 
8. docker-compose -f env.yml up -d

Test:
1. Send POST request to `http://127.0.0.1:8086/api/v1.0/ports` with `Content-Type:form-data` and Body `file:<ports.json>`
2. Send GET request to `http://127.0.0.1:8086/api/v1.0/ports?limit=10&skip=0`, where skip if like offset for pagination

