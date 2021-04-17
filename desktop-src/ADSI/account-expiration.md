---
title: Scadenza account (provider LDAP)
description: Per impostare la data di scadenza dell'account, impostare la proprietà IADsUser. AccountExpirationDate sul valore di data desiderato.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- ADSI scadenza account, provider LDAP
- Provider LDAP ADSI, esempi di gestione degli utenti, scadenza dell'account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300426"
---
# <a name="account-expiration-ldap-provider"></a>Scadenza account (provider LDAP)

Per impostare la data di scadenza dell'account, impostare la proprietà [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) sul valore di data desiderato. Per disabilitare la data di scadenza dell'account, impostare l'attributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) su zero. Negli esempi di codice seguenti viene illustrato come impostare la data di scadenza.


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> L'attributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) contiene la data di scadenza dell'account. Lo snap-in MMC utenti e computer Active Directory Visualizza la data in cui l'account scadrà alla fine di. Lo snap-in di MMC utenti e computer Active Directory visualizzerà quindi la data di scadenza dell'account come un giorno prima della data inclusa nell'attributo **accountExpires** .

 

 

 