## NextJS API---> Logical Operators

### AND Operation
![](https://imgur.com/xE0rCpe.png)

```bash
// Two conditions must be true for the data to be fetched.
const readData = await prisma.employee.findMany({
            where: {
                AND: [
                    { name: { contains: "Wasim"} },
                    { salary: { gte: 35000 } },
                ]
            }
        });
```
---
