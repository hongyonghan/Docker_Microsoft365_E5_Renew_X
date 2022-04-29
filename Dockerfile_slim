#设置依赖的镜像
FROM mcr.microsoft.com/dotnet/sdk:3.1 AS base
#设置镜像创建者
MAINTAINER hanhongyong
#设置工作目录
WORKDIR /app
#copy文件到app目录下
COPY Microsoft365_E5_Renew_X/. ./

ENV TZ Asia/Shanghai

FROM mcr.microsoft.com/dotnet/aspnet:3.1

WORKDIR /app
COPY --from=base /app .
ENTRYPOINT ["dotnet", "Microsoft365_E5_Renew_X.dll"]
