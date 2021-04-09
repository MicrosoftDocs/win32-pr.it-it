---
title: L'utente deve modificare la password all'accesso successivo (provider LDAP)
description: Per forzare l'utente a modificare la password all'accesso successivo, impostare l'attributo pwdLastSet su zero (0). Per rimuovere questo requisito, impostare l'attributo pwdLastSet su-1. L'attributo pwdLastSet non può essere impostato su qualsiasi altro valore tranne che dal sistema.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- L'utente deve modificare la password all'accesso successivo ADSI, provider LDAP
- LDAP provider ADSI, esempi di gestione degli utenti, è necessario modificare la password all'accesso successivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784ee0defbe3c8ec9abe2d110c2532b8c9688019
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044048"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>L'utente deve modificare la password all'accesso successivo (provider LDAP)

Per forzare l'utente a modificare la password all'accesso successivo, impostare l'attributo **pwdLastSet** su zero (0). Per rimuovere questo requisito, impostare l'attributo **pwdLastSet** su-1. L'attributo **pwdLastSet** non può essere impostato su qualsiasi altro valore tranne che dal sistema.

Nell'esempio di codice seguente viene illustrato come impostare l'opzione "utente necessario modificare la password all'accesso successivo".


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



Nell'esempio di codice seguente viene illustrato come impostare l'opzione "utente necessario modificare la password all'accesso successivo".


```C++
/***************************************************************************

    SetUserMustChangePassword()

***************************************************************************/

HRESULT SetUserMustChangePassword(LPCWSTR pwszUserADsPath, 
                                  LPCWSTR pwszUsername, 
                                  LPCWSTR pwszPassword)
{
    IADs *pUser;
    HRESULT hr;

    hr = ADsOpenObject(pwszUserADsPath,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&pUser);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        hr = pUser->Put(CComBSTR("pwdLastSet"), var);
        hr = pUser->SetInfo();

        VariantClear(&var);
        pUser->Release();
    }

    return hr;
}
```



 

 




