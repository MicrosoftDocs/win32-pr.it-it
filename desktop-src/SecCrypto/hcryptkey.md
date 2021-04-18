---
description: Il tipo di dati HCRYPTKEY viene utilizzato per rappresentare gli handle delle chiavi crittografiche.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316159"
---
# <a name="hcryptkey"></a>HCRYPTKEY

Il tipo di dati **HCRYPTKEY** viene utilizzato per rappresentare gli handle delle [*chiavi crittografiche*](../secgloss/c-gly.md). Questi handle vengono usati per indicare al modulo CSP quale chiave viene usata in un'operazione specifica. Il modulo CSP non consente l'accesso diretto ai valori di chiave. Al contrario, l'utente esegue le funzioni usando il valore della chiave tramite l'handle di chiave.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
