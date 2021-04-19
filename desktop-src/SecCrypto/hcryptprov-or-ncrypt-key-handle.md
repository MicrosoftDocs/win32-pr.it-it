---
description: Viene usato come handle per un provider del servizio di crittografia (CSP) CryptoAPI o un CSP CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316155"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>\_handle di chiave HCRYPTPROV o \_ NCRYPT \_ \_

Il tipo di dati dell' **handle di \_ chiave HCRYPTPROV o \_ NCRYPT \_ \_** viene usato come handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) CryptoAPI o un CSP CNG. Questo handle deve essere un handle [**HCRYPTPROV**](hcryptprov.md) creato tramite la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) o un handle di **\_ \_ handle di chiave NCRYPT** creato utilizzando la funzione [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) . Le nuove applicazioni devono sempre passare l'handle della **\_ \_ chiave NCRYPT** a un CSP CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
