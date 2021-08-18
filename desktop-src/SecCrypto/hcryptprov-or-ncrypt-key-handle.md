---
description: Viene usato come handle per un provider del servizio di crittografia CryptoAPI (CSP) o CNG CSP.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982ab2a37c1a2d6035f76cac5c55dcdae44c4cf38f86138c52590c73724b53e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006339"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>HANDLE DI CHIAVE HCRYPTPROV \_ \_ O NCRYPT \_ \_

Il tipo di dati **HCRYPTPROV \_ OR \_ NCRYPT \_ KEY \_ HANDLE** viene usato come handle per un [*provider*](../secgloss/c-gly.md) del servizio di crittografia CryptoAPI (CSP) o CNG CSP. Questo handle deve essere un handle [**HCRYPTPROV**](hcryptprov.md) creato usando la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) o un handle **NCRYPT \_ KEY \_ HANDLE** creato tramite la funzione [**NCryptOpenKey.**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) Le nuove applicazioni devono sempre passare l'handle **NCRYPT \_ KEY \_ HANDLE** a un CNG CSP.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
