---
title: Impossibile modificare la password dell'utente (provider WinNT)
description: Informazioni su come negare a un utente l'autorizzazione per modificare una password per il provider WinNT. La possibilità di un utente di modificare la propria password può essere concessa o negata.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- Impossibile modificare la password dell'utente (provider WinNT)
- L'utente non può modificare la password (provider WinNT), modifica
- Provider WINNT ADSI, esempi di gestione degli utenti, utente non può modificare la password, modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33510fa36285fa49a413b84d91e29f8d5a367622
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408094"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="8bb23-107">Impossibile modificare la password dell'utente (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="8bb23-107">Modifying User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="8bb23-108">La possibilità di un utente di modificare la propria password è un'autorizzazione che può essere concessa o negata.</span><span class="sxs-lookup"><span data-stu-id="8bb23-108">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="8bb23-109">Per negare questa autorizzazione, aggiungere il flag **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** alla **proprietà userFlags** dell'oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="8bb23-109">To deny this permission, add the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag to the **userFlags** property of the user object.</span></span> <span data-ttu-id="8bb23-110">Per concedere questa autorizzazione, rimuovere il flag **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** dalla **proprietà userFlags** dell'oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="8bb23-110">To grant this permission, remove the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag from the **userFlags** property of the user object.</span></span>

## <a name="example-code"></a><span data-ttu-id="8bb23-111">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="8bb23-111">Example Code</span></span>

<span data-ttu-id="8bb23-112">Nell'esempio di codice seguente viene illustrato come modificare il flag **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="8bb23-112">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



<span data-ttu-id="8bb23-113">Nell'esempio di codice seguente viene illustrato come modificare il flag **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="8bb23-113">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



 

 




