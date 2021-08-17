---
title: Blocco account (provider WinNT)
description: Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per il numero di minuti specificato dall'attributo lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Blocco account ADSI , provider WinNT
- Provider WinNT ADSI, esempi di gestione degli utenti, blocco account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e28c2a4bf58f5559070af78ca55235e8b10c16b2b856a63a256767d4d67a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838361"
---
# <a name="account-lockout-winnt-provider"></a>Blocco account (provider WinNT)

Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per il numero di minuti specificato [**dall'attributo lockoutDuration.**](/windows/desktop/ADSchema/a-lockoutduration) La [**proprietà IADsUser.IsAccountLocked**](iadsuser-property-methods.md) sembra essere la proprietà da usare per leggere e modificare lo stato di blocco di un account utente, ma il provider ADSI WinNT presenta restrizioni che limitano l'uso della **proprietà IsAccountLocked.**

## <a name="resetting-the-account-lockout-status"></a>Reimpostazione dello stato di blocco dell'account

Quando si usa il provider WinNT, la [**proprietà IsAccountLocked**](iadsuser-property-methods.md) può essere impostata solo su **FALSE,** che sblocca l'account. Il tentativo di impostare la **proprietà IsAccountLocked** su **TRUE** avrà esito negativo. Solo il sistema può bloccare un account.

Nell'esempio di codice seguente viene illustrato come usare Visual Basic con ADSI per sbloccare un account utente.


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



L'esempio di codice seguente illustra come usare C++ con ADSI per sbloccare un account utente.


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a>Lettura dello stato di blocco dell'account

Con il provider WinNT, la [**proprietà IsAccountLocked**](iadsuser-property-methods.md) può essere usata per determinare se un account è bloccato. Se un account è bloccato, la **proprietà IsAccountLocked** conterrà **TRUE.** Se un account non è bloccato, la **proprietà IsAccountLocked** conterrà **FALSE.**

Nell'esempio di codice seguente viene illustrato come usare Visual Basic con ADSI per determinare se un account è bloccato.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



Nell'esempio di codice seguente viene illustrato come utilizzare C++ con ADSI per determinare se un account è bloccato.


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 