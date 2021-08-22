---
description: Rappresenta un handle per una funzione installabile dell'identificatore di oggetto (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb36bdd98332842d89533c9c34a880aecdc8555cd64bb03888c0bd146cea3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006549"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

Il **tipo di dati HCRYPTOIDFUNCADDR** rappresenta un handle per una funzione installabile dell'identificatore di oggetto (OID). [](../secgloss/o-gly.md) Le [**funzioni CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)e [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) e la struttura [**CERT STORE \_ \_ PROV \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) usano questo tipo di dati.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
