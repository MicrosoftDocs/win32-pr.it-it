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
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a><span data-ttu-id="60814-107">L'utente deve modificare la password all'accesso successivo (provider LDAP)</span><span class="sxs-lookup"><span data-stu-id="60814-107">User Must Change Password at Next Logon (LDAP Provider)</span></span>

<span data-ttu-id="60814-108">Per forzare l'utente a modificare la password all'accesso successivo, impostare l'attributo **pwdLastSet** su zero (0).</span><span class="sxs-lookup"><span data-stu-id="60814-108">To force a user to change their password at next logon, set the **pwdLastSet** attribute to zero (0).</span></span> <span data-ttu-id="60814-109">Per rimuovere questo requisito, impostare l'attributo **pwdLastSet** su-1.</span><span class="sxs-lookup"><span data-stu-id="60814-109">To remove this requirement, set the **pwdLastSet** attribute to -1.</span></span> <span data-ttu-id="60814-110">L'attributo **pwdLastSet** non può essere impostato su qualsiasi altro valore tranne che dal sistema.</span><span class="sxs-lookup"><span data-stu-id="60814-110">The **pwdLastSet** attribute cannot be set to any other value except by the system.</span></span>

<span data-ttu-id="60814-111">Nell'esempio di codice seguente viene illustrato come impostare l'opzione "utente necessario modificare la password all'accesso successivo".</span><span class="sxs-lookup"><span data-stu-id="60814-111">The following code example shows how to set the "User must change password at next logon" option.</span></span>


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



<span data-ttu-id="60814-112">Nell'esempio di codice seguente viene illustrato come impostare l'opzione "utente necessario modificare la password all'accesso successivo".</span><span class="sxs-lookup"><span data-stu-id="60814-112">The following code example shows how to set the "User must change password at next logon" option.</span></span>


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



 

 




