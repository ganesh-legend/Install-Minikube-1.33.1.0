First download given minikube deb file from current repo (version of minikube-1.33.1.0)

```bash
wget link_address_of_deb_file
```
then download kubectl command previous version having version less than minikube 
eg. kubectl-1.31

```bash
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl gnupg
```

```bash
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.31/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
sudo chmod 644 /etc/apt/keyrings/kubernetes-apt-keyring.gpg
```

```bash
echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.31/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo chmod 644 /etc/apt/sources.list.d/kubernetes.list   
```

```bash
sudo apt-get update
sudo apt-get install -y kubectl
```

then run below command 

```bash
sudo dpkg -i deb_file_name.deb
```

