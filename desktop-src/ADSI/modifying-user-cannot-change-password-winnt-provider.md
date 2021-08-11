---
title: Modifica dell'utente non è possibile modificare la password (provider WinNT)
description: Informazioni su come negare a un utente l'autorizzazione per modificare una password per il provider WinNT. La possibilità di un utente di modificare la propria password può essere concessa o negata.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- Modifica dell'utente non è possibile modificare la password (provider WinNT)
- L'utente non può modificare la password (provider WinNT), modifica
- Provider WinNT ADSI, esempi di gestione utenti,Utente non può modificare la password, modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b510fb08172a178a454ee731110765844368ca78108047a7a5a738b78b6a196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178965"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a>Modifica dell'utente non è possibile modificare la password (provider WinNT)

La possibilità di un utente di modificare la propria password è un'autorizzazione che può essere concessa o negata. Per negare questa autorizzazione, aggiungere il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** alla **proprietà userFlags** dell'oggetto utente. Per concedere questa autorizzazione, rimuovere il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** dalla **proprietà userFlags** dell'oggetto utente.

## <a name="example-code"></a>Codice di esempio

L'esempio di codice seguente illustra come modificare il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Sub SetUserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String, fUserCannotChangePassword As Boolean)
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
    
    lUserFlags = oUser.Get("userFlags")
    
    If fUserCannotChangePassword Then
        lUserFlags = lUserFlags Or ADS_UF_PASSWD_CANT_CHANGE
    Else
        lUserFlags = lUserFlags And Not ADS_UF_PASSWD_CANT_CHANGE
    End If
    
    ' Modify the userFlags property.
    oUser.Put "userFlags", lUserFlags
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



L'esempio di codice seguente illustra come modificare il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.


```C++
//***************************************************************************
//  SetUserCannotChangePassword()
//***************************************************************************

HRESULT SetUserCannotChangePassword(LPCWSTR pwszDomain,
                                    LPCWSTR pwszUser, 
                                    LPCWSTR pwszUserCred, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    if(NULL == pwszDomain || 
        NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
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
        CComBSTR sbstrPropName = "userFlags";
        CComVariant svar;
        
        hr = pads->Get(sbstrPropName, &svar);
        if(SUCCEEDED(hr))
        {
            if(fCannotChangePassword)
            {
                svar.lVal |= ADS_UF_PASSWD_CANT_CHANGE;
            }
            else
            {
                svar.lVal &= ~ADS_UF_PASSWD_CANT_CHANGE;
            }

            // Perform the change.
            hr = pads->Put(sbstrPropName, svar);

            // Commit the change.
            hr = pads->SetInfo();
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




