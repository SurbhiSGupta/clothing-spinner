# Build Docker image with anti-caching nginx config
docker_build('clothing-spinner', '.', 
  live_update=[
    sync('./', '/usr/share/nginx/html/'),
  ]
)

k8s_yaml('k8s.yaml')
k8s_resource('clothing-spinner', port_forwards=3000)