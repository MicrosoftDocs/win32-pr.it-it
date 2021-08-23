---
description: Rappresenta un handle per un set di funzioni installabili OID (Object Identifier).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3926b78359450b780a9952aeae9d957157ebb56973a7f428824b07cbb43e9a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006469"
---
# <a name="hcryptoidfuncset"></a>HCRYPTOIDFUNCSET

Il tipo di dati **HCRYPTOIDFUNCSET** rappresenta un handle per un set di funzioni installabili OID [*(Object Identifier).*](../secgloss/o-gly.md) Le [**funzioni CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)e [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) usano questo tipo di dati.


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
