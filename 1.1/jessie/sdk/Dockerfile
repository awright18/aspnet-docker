FROM microsoft/aspnetcore-build:1.1.2-jessie 

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF

RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/5.0.1.1 main" > etc/apt/sources.list.d/mono-official.list \
    && apt-get update \
    && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl unzip netbase openssh-server \ 
    && rm -rf /var/lib/apt/lists/* /tmp/* \
    && npm install -g yarn \ 
    && curl -sSL https://aka.ms/getvsdbgsh | bash /dev/stdin -v latest -l ~/vsdbg