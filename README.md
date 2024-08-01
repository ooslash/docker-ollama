# docker-ollama
Docker Ollama


## Host에서 NVIDIA Container를 활용하려면, 다음과 같이 nvidia-container-toolkit을 설치해야 한다.
```bash
sudo dnf update
curl -s -L https://nvidia.github.io/libnvidia-container/stable/rpm/nvidia-container-toolkit.repo \
    | sudo tee /etc/yum.repos.d/nvidia-container-toolkit.repo
sudo yum install -y nvidia-container-toolkit
sudo nvidia-ctk runtime configure --runtime=docker
sudo systemctl restart docker
```

# run ollama
```bash
docker compose up -d
```

# LLaMA 70B model
```bash
docker exec -it ollama ollama pull llama3.1:70b
```
