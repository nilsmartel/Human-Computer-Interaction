
# Human Computer Interaction


---
## 4th Lecture
### What is Fitts Law?
>	Fitts Law states that the **Movement Time** to a target is dependent on the **distance** to the target and the **size** of the target*
>
>*_can only be applied to pointing movements_

`Movement Time = a + b*log2(distance/size +1)`

> An implementation of this in Javascript might look like this
> 
```javascript
 	function createFittsFunction(a, b) {
 		return (distance, size) => a + b*Math.log2(distance/size + 1)
 	}  	
 	let getMovementTime = createFittsFunction(0, 1)
 	let movementTime = getMovementTime(obj.distance, obj.size)
```

---

> Movement generates Information
> ---
> Information is required to specify movement
> 
### What is
-	Index of  Dificulty (ID)
- 	Movement Time (MT)
-  Index of Performance (IP)


> Formulas
> ---
> - `ID = log2(D / W + 1)` (in bits)
> - `MT = a + b*ID`	(in seconds)
> - `IP = ID / MT` (in bits/second)
> 
> 	bits := Unit of Information

