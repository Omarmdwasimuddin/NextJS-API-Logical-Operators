## NextJS API---> Logical Operators

### AND Operation
![](https://imgur.com/xE0rCpe.png)

`Two conditions must be true for the data to be fetched.`
```bash
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

### OR Operation
![](https://imgur.com/irKfbZi.png)

`One conditions must be true to get the data.`
```bash
const readData = await prisma.employee.findMany({
            where: {
                OR: [
                    { name: { contains: "Wasim"} },
                    { salary: { gte: 35000 } },
                ]
            }
        });
```
---

### NOT Operation
![](.png)

`Two conditions must be false to return the data. If any of the conditions is true, the data will not be returned.`
```bash
const readData = await prisma.employee.findMany({
            where: {
                NOT: [
                    { name: { contains: "Sayeed"} },
                    { salary: { gt: 35000 } },
                ]
            }
        });
```
---
