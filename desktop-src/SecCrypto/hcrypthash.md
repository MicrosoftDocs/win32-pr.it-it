---
description: Il tipo di dati HCRYPTHASH viene usato per rappresentare gli handle per gli oggetti hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b2d20d7aeb46adda162f8d5ec380143164690bad8ee88139f9653753f1e290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006559"
---
# <a name="hcrypthash"></a>HCRYPTHASH

Il **tipo di dati HCRYPTHASH** viene usato per rappresentare gli handle per gli oggetti [*hash*](../secgloss/h-gly.md). Questi handle indicano al modulo CSP quale hash viene usato in una determinata operazione. Il modulo CSP non consente la manipolazione diretta dei valori hash. Al contrario, l'utente modifica i valori hash tramite l'handle hash.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
