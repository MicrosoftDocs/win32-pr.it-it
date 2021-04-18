---
title: Blocco account (provider WinNT)
description: Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per il numero di minuti specificato dall'attributo lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Blocco account ADSI, provider WinNT
- ADSI del provider WinNT, esempi di gestione degli utenti, blocco degli account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300447"
---
# <a name="account-lockout-winnt-provider"></a>Blocco account (provider WinNT)

Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per il numero di minuti specificato dall'attributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) . La proprietà [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) sembra essere la proprietà da utilizzare per leggere e modificare lo stato di blocco di un account utente, ma il provider ADSI WinNT presenta restrizioni che limitano l'utilizzo della proprietà **IsAccountLocked** .

## <a name="resetting-the-account-lockout-status"></a>Reimpostazione dello stato di blocco dell'account

Quando si usa il provider WinNT, la proprietà [**IsAccountLocked**](iadsuser-property-methods.md) può essere impostata solo su **false**, per sbloccare l'account. Il tentativo di impostare la proprietà **IsAccountLocked** su **true** avrà esito negativo. Un account può essere bloccato solo dal sistema.

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare Visual Basic con ADSI per sbloccare un account utente.


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



Nell'esempio di codice riportato di seguito viene illustrato come utilizzare C++ con ADSI per sbloccare un account utente.


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

Con il provider WinNT, è possibile usare la proprietà [**IsAccountLocked**](iadsuser-property-methods.md) per determinare se un account è bloccato. Se un account è bloccato, la proprietà **IsAccountLocked** conterrà **true**. Se un account non è bloccato, la proprietà **IsAccountLocked** conterrà **false**.

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare Visual Basic con ADSI per determinare se un account è bloccato.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



Nell'esempio di codice riportato di seguito viene illustrato come utilizzare C++ con ADSI per determinare se un account è bloccato.


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



 

 