# Helm Chart for testing database connectivity
This is for helping to troubleshoot pods in a K8s cluster which cannot connect to an external database.

You may be able to connect to your database locally, but the real trick is connecting to it from within your cluster.
You could SSH into a pod in your cluster, and then attempt to connect to the db, but that assumes that pod has the correct jdbc driver
already installed.  By installing this chart to your cluster, you'll be able to see if 
your nework policies are properly configured to communicate with your db, which may or may not be external to your cluster.