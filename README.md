# ci-go-deploy-ec2
Treinamento CI com deply no AWS EC2

Passos:
1 - Criação de infraestrutura AWS com; EC2 e RDS (Postgres) 
2 - Modificação de go.yml com inclusão de job deploy_ec2
3 - Criação do script EC2.yml para deploy na infratestrutura AWS
4 - Modificação de db.go -> ConectaComBancoDeDados(): os.Getenv("PORT") para os.Getenv("DBPORT")
5 - Modificação de go.yml -> PORT: 5432 para DBPORT: 5432
6 - Modificação de Dockerfile -> PORT=5432 para DBPORT=5432
7 - EC2-SSH>sudo su
    EC2-SSH>yum update
    EC2-SSH>yum install -y golang
    EC2-SSH>Go version -> go version go1.21.0 windows/amd64
