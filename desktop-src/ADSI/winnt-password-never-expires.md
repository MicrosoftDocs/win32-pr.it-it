---
title: La password non scade mai (provider WinNT)
description: Per abilitare questa opzione usando il provider ADSI WinNT, impostare il flag ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD (0x10000) sull'attributo UserFlags. Nota Per Windows 2000 e versioni successive, usare il provider ADSI LDAP per le operazioni di gestione degli utenti, come illustrato.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- La password non scade mai (provider WinNT)
- La password non scade mai ad ADSI, provider WinNT
- Provider WinNT ADSI, esempi di gestione utenti, Password mai scaduta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47cdd7dc181c2875e8de06b66233d727c5b132963921b163b02fc09cbdc051d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082165"
---
# <a name="password-never-expires-winnt-provider"></a>La password non scade mai (provider WinNT)

Per abilitare questa opzione usando il provider ADSI WinNT, impostare il flag **ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD** (0x10000) sull'attributo **UserFlags.**

> [!Note]  
> Per Windows 2000 e versioni successive, usare il provider ADSI LDAP per le operazioni di gestione degli utenti, come illustrato. Per altre informazioni, vedere [Password Never Expires (LDAP Provider)](password-never-expires.md).

 

## <a name="example-1"></a>Esempio 1

Nell'esempio di codice seguente viene illustrato come impostare l'opzione password never expires usando Visual Basic con ADSI.


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

L'esempio di codice seguente illustra come impostare l'opzione password never expires usando C++ con ADSI.


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



 

 




