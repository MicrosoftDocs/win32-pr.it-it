---
title: L'utente deve modificare la password all'accesso successivo (provider LDAP)
description: Per forzare un utente a modificare la password all'accesso successivo, impostare l'attributo pwdLastSet su zero (0). Per rimuovere questo requisito, impostare l'attributo pwdLastSet su -1. L'attributo pwdLastSet non può essere impostato su nessun altro valore, ad eccezione del sistema.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- L'utente deve modificare la password all'accesso successivo ADSI , provider LDAP
- Provider LDAP ADSI, esempi di gestione degli utenti, modifica della password all'accesso successivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103703381512e82eee608d452b921429c87ef3ce6b7d59017fd07bc081e75ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648841"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>L'utente deve modificare la password all'accesso successivo (provider LDAP)

Per forzare un utente a modificare la password all'accesso successivo, impostare **l'attributo pwdLastSet** su zero (0). Per rimuovere questo requisito, impostare **l'attributo pwdLastSet** su -1. **L'attributo pwdLastSet** non può essere impostato su nessun altro valore, ad eccezione del sistema.

Nell'esempio di codice seguente viene illustrato come impostare l'opzione "L'utente deve modificare la password all'accesso successivo".


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



Nell'esempio di codice seguente viene illustrato come impostare l'opzione "L'utente deve modificare la password all'accesso successivo".


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



 

 




