---
title: Scadenza account (provider LDAP)
description: Per impostare la data di scadenza dell'account, impostare la proprietà IADsUser.AccountExpirationDate sul valore di data desiderato.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- Scadenza account ADSI , provider LDAP
- Provider LDAP ADSI, esempi di gestione utenti,Scadenza account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645ce5e2e1ae72ace0a8a642642eb5c15e7eabd63d51dba3f03596869bfb9efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024069"
---
# <a name="account-expiration-ldap-provider"></a>Scadenza account (provider LDAP)

Per impostare la data di scadenza dell'account, impostare la proprietà [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) sul valore di data desiderato. Per disabilitare la data di scadenza dell'account, impostare [**l'attributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) su zero. Negli esempi di codice seguenti viene illustrato come impostare la data di scadenza.


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
> [**L'attributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) contiene la data di scadenza dell'account. Lo Utenti e computer di Active Directory snap-in MMC visualizza la data di scadenza dell'account alla fine di . In altri Utenti e computer di Active Directory snap-in MMC verrà visualizzata la data di scadenza dell'account come un giorno precedente alla data contenuta **nell'attributo accountExpires.**

 

 

 