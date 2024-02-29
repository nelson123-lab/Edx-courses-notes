# Different types of ML System Architecture in Production
A Tradeoff between simplicity vs flexbility is happening in different architectures.

1) Embedded approach
   - Here the trained model is a dependency of the application.
     - Pretained model
     - Predict on the fly
     - eg: Embedded on mobile device like an app
     - To do model update we need to redeploy the application like creating an update of the mobile application.
  
2) Dedicated Model API
   - The trained model becomes a dependency of a separate API service.
     - Pretrained model
     - Predict on the fly
     - Flexibility of doing the model deployment separate from the application deployment.
     - Capability to scale our application or model miroservice separately depending on the traffic.

3) Model published os Data
   - This architecture leverages streaming platforms like apache kafka and ingest model at runtime not at build time.
     - Pretrained model
     - Predict on the fly
     - No need to redeploy the application due to ingestion of the model at runtime.

4) Offline predictions
   - This is a type of asynchronous prediction design. Predictions are collected in a database or in some form of storage and it will be displayed in the application as dashboard/ report.
     - Pretrained model
     - The prediction is not on the fly

# Architecture Comparison
<div align="center"><img src="https://github.com/nelson123-lab/Edx-courses-notes/blob/d976578342233e0ff312a65f29993361443991e3/Machine%20learning%20model%20development%20and%20deployment/Image%20data/ML%20system%20architecture%20Comparison.png" width="1100"/></div>

## References:
- [Udemy course Deployment of Machine leanring models](https://www.udemy.com/share/101Y5K3@4F-ZX0yaN8pRdq-RRXXVmUSmqwnlu2A781XUyrEKuovKNUcLXPg03Vs0mrvY1OiX-A==/)
