What is a LimitRange?

A LimitRange in Kubernetes sets rules for resource usage (CPU, memory, storage) inside a namespace.
It prevents any one Pod or container from using too much or too little of the cluster’s resources.

Think of it like: Every car (Pod) in this lane (namespace) must stay between 40–80 km/h (resource min–max)
Why LimitRange is Important?

A user deploys a Pod without setting resource limits & Pod consumes all CPU and slows down others.	    
Solution - LimitRange can automatically apply default limits.
A user sets extremely low resources & Pod keeps crashing due to low memory.	        
Solution - LimitRange enforces a minimum resource request.
A single Pod uses excessive resources & One Pod uses 4GB RAM while others need space.	
Solution - LimitRange enforces a maximum per Pod or container.

A LimitRange can:

✅ Set minimum & maximum values for CPU/memory per container or Pod.

✅ Automatically assign default limits if user doesn’t specify them.

✅ Enforce request-to-limit ratios (e.g., limit ≤ 2 × request).

✅ Apply constraints to PVCs (for storage requests).