---
title: Lettura dell'utente non può modificare la password (provider WinNT)
description: La possibilità di modificare la propria password da parte di un utente è un'autorizzazione che può essere concessa o negata.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Lettura dell'utente non può modificare la password (provider WinNT) ADSI
- L'utente non può modificare la password (provider WinNT) ADSI, lettura
- ADSI provider ADSI, esempi di gestione utenti, l'utente non può modificare la password, leggere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab257f620d3e103866639f8ecacb57cc924efec4
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2020
ms.locfileid: "103956233"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>Lettura dell'utente non può modificare la password (provider WinNT)

La possibilità di modificare la propria password da parte di un utente è un'autorizzazione che può essere concessa o negata. Per determinare se all'utente è stata concessa questa autorizzazione con il provider WinNT, leggere il flag **Ads \_ UF \_ passwd \_ cant \_ Change** della proprietà **userflags** dell'oggetto utente. Il flag **Ads \_ UF \_ passwd \_ cant \_ Change** è definito nell'enumerazione di enumerazione [**\_ \_ flag \_ utente ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) .

## <a name="example-code"></a>Codice di esempio

Nell'esempio di codice riportato di seguito viene illustrato come ottenere il flag **Ads \_ UF \_ passwd \_ cant \_ Change** della proprietà **userflags** di un oggetto utente.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



Nell'esempio di codice riportato di seguito viene illustrato come ottenere il flag **Ads \_ UF \_ passwd \_ cant \_ Change** della proprietà **userflags** di un oggetto utente.


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




