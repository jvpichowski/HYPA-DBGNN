FROM pytorch/pytorch:2.1.0-cuda12.1-cudnn8-runtime

# Update packages
RUN apt update
RUN apt install -y git
RUN apt install -y git-lfs
RUN apt install -y wget
RUN git lfs install

# Install Julia and PyJulia Dependencies
RUN wget https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz
RUN tar zxvf julia-1.9.3-linux-x86_64.tar.gz
RUN mkdir -p /opt/bin
RUN cp -r julia-1.9.3 /opt/bin/julia-1.9.3
ENV PATH="${PATH}:/opt/bin/julia-1.9.3/bin"
RUN julia -e 'using Pkg; Pkg.add("PyCall"); Pkg.add("Distributions")'

# Install packages with requirements.txt
COPY requirements.txt .
RUN pip3 --disable-pip-version-check --no-cache-dir install -r requirements.txt
RUN pip3 --disable-pip-version-check --no-cache-dir install pyg_lib torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-2.1.0+cu121.html
RUN pip3 --disable-pip-version-check --no-cache-dir install dgl -f https://data.dgl.ai/wheels/cu121/repo.html
RUN pip3 --disable-pip-version-check --no-cache-dir install  dglgo -f https://data.dgl.ai/wheels-test/repo.html
# Install Hypa
RUN git clone https://github.com/tlarock/hypa.git
RUN cd hypa && pip3 --disable-pip-version-check --no-cache-dir install -e .
# Install pathpyG
RUN pip3 install git+https://github.com/pathpy/pathpyg.git@0b8f243811c34e023acf49951cc41885d2b41fb8