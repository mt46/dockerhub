FROM mt46/container:baseos

# Install python, pip, Ansible
RUN dnf -y install python3-pip \ 
&& curl -O https://bootstrap.pypa.io/get-pip.py && python3 get-pip.py --user \
&& export PATH=~/.local/bin:$PATH && source ~/.bash_profile \
&& echo 'pathmunge ~/.local/bin' > /etc/profile.d/pip.sh \
&& chmod +x /etc/profile.d/pip.sh \
&& pip3 install ansible --user