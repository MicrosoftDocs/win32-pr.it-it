---
description: Il tipo di dati HCRYPTKEY viene usato per rappresentare gli handle per le chiavi crittografiche.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78d50f7fb005d877f6520172631b4546b8d498c415de58502defd26831c65fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006439"
---
# <a name="hcryptkey"></a>HCRYPTKEY

Il tipo di dati **HCRYPTKEY** viene usato per rappresentare gli handle per [*le chiavi crittografiche.*](../secgloss/c-gly.md) Questi handle vengono usati per indicare al modulo CSP quale chiave viene usata in un'operazione specifica. Il modulo CSP non abilita l'accesso diretto ai valori della chiave. Al contrario, l'utente esegue funzioni usando il valore della chiave tramite l'handle della chiave.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
