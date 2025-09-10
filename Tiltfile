# Build Docker image with live updates
docker_build('clothing-spinner', '.', 
  live_update=[
    sync('./', '/usr/share/nginx/html/'),
    run('nginx -s reload', trigger=['index.html'])
  ]
)

# Deploy to Kubernetes
k8s_yaml('k8s.yaml')

# Create port forward
k8s_resource('clothing-spinner', port_forwards=3000)