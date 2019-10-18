FROM mt46/container:baseos

# Install python, pip, AWS CLI
RUN dnf -y install python3-pip \ 
&& curl -O https://bootstrap.pypa.io/get-pip.py && python3 get-pip.py --user \
&& export PATH=~/.local/bin:$PATH && source ~/.bash_profile \
&& pip3 install awscli --user \
&& echo 'pathmunge ~/.local/bin' > /etc/profile.d/awscli.sh \
&& chmod +x /etc/profile.d/awscli.sh \