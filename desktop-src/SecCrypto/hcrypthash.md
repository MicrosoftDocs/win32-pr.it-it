---
description: Il tipo di dati HCRYPTHASH viene utilizzato per rappresentare gli handle per gli oggetti hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884057"
---
# <a name="hcrypthash"></a>HCRYPTHASH

Il tipo di dati **HCRYPTHASH** viene utilizzato per rappresentare gli handle per [*gli oggetti hash*](../secgloss/h-gly.md). Questi handle indicano al modulo CSP quale hash viene usato in una determinata operazione. Il modulo CSP non consente la manipolazione diretta dei valori hash. Il valore hash viene invece modificato dall'utente tramite l'handle hash.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
