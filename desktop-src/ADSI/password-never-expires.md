---
title: La password non scade mai (provider LDAP)
description: Per abilitare l'opzione password never expires usando il provider LDAP, impostare il flag ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD sull'attributo useraccountControl.
ms.assetid: b8d7e7fe-c846-45c4-9c5f-770530453836
ms.tgt_platform: multiple
keywords:
- La password non scade mai ad ADSI, provider LDAP
- Provider LDAP ADSI, esempi di gestione degli utenti,Password non scade mai
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa48145fa2b78c7685cdf52ab58b1e681df48c7d10a80f0ac7462fa7d4cb868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838931"
---
# <a name="password-never-expires-ldap-provider"></a>La password non scade mai (provider LDAP)

Per abilitare l'opzione password never expires usando il provider LDAP, impostare il flag [**ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) sull'attributo [**useraccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000

Set usr = GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=Com")
flag = usr.Get("userAccountControl")
newFlag = flag Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "userAccountControl", newFlag
usr.SetInfo
```




```C++
#include <activeds.h>

IADsUser *pUser;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath = L"LDAP://serv1/cn=Jeff Smith,cn=Users,dc=Fabrikam,dc=com";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->Get(_bstr_t("userAccountControl"), &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(_bstr_t("userAccountControl"), var);

hr = pUser->SetInfo();
VariantClear(&var);
hr = pUser->Release();
```



 

 