---
title: Lettura dell'utente non è possibile modificare la password (provider WinNT)
description: Informazioni su come determinare se un utente ha l'autorizzazione per modificare una password per il provider WinNT. La possibilità di un utente di modificare una password può essere concessa o negata.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Lettura dell'utente non è possibile modificare la password (provider WinNT) ADSI
- L'utente non può modificare la password (provider WinNT) ADSI , lettura
- Provider WinNT ADSI, esempi di gestione utenti,Utente non può modificare la password,lettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761a1ef0a332f1cdfd7dad1b20426b749618ed2286832c7ff16b207cee57c176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637551"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>Lettura dell'utente non è possibile modificare la password (provider WinNT)

La possibilità di un utente di modificare la propria password è un'autorizzazione che può essere concessa o negata. Per determinare se all'utente è stata concessa questa autorizzazione con il provider WinNT, leggere il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** dell'oggetto utente. Il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** è definito nell'enumerazione [**ADS \_ USER FLAG \_ \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)

## <a name="example-code"></a>Codice di esempio

L'esempio di codice seguente illustra come ottenere il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.


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



L'esempio di codice seguente illustra come ottenere il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.


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



 

 




