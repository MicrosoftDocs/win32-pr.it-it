---
title: Nessuna scadenza password (provider WinNT)
description: Per abilitare questa opzione tramite il provider ADSI di WinNT, impostare il \_ flag ADS UF \_ dont \_ expire \_ (0X10000) nell'attributo UserFlags. Nota per Windows 2000 e versioni successive, usare il provider ADSI LDAP per le operazioni di gestione degli utenti, come illustrato.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- Nessuna scadenza password (provider WinNT)
- La password non scade mai con ADSI, provider WinNT
- ADSI provider ADSI, esempi di gestione utenti, nessuna scadenza password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322017"
---
# <a name="password-never-expires-winnt-provider"></a>Nessuna scadenza password (provider WinNT)

Per abilitare questa opzione tramite il provider ADSI di WinNT, impostare il flag **Ads \_ UF \_ dont \_ expire \_** (0x10000) nell'attributo **UserFlags** .

> [!Note]  
> Per Windows 2000 e versioni successive, usare il provider ADSI LDAP per le operazioni di gestione degli utenti, come illustrato. Per ulteriori informazioni, vedere [Nessuna scadenza password (provider LDAP)](password-never-expires.md).

 

## <a name="example-1"></a>Esempio 1

Nell'esempio di codice seguente viene illustrato come impostare l'opzione Nessuna scadenza password utilizzando Visual Basic con ADSI.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a>Esempio 2

Nell'esempio di codice seguente viene illustrato come impostare l'opzione Nessuna scadenza password utilizzando C++ con ADSI.


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




