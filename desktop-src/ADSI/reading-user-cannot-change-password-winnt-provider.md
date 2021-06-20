---
title: Lettura dell'utente che non può modificare la password (provider WinNT)
description: Informazioni su come determinare se un utente è autorizzato a modificare una password per il provider WinNT. La possibilità di un utente di modificare una password può essere concessa o negata.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Lettura dell'utente non è in grado di modificare la password (provider WinNT) ADSI
- L'utente non può modificare la password (provider WinNT) ADSI, lettura
- Provider WINNT ADSI, esempi di gestione degli utenti,Utente non può modificare la password,lettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd075bfb6700779b60f9e578a4e89957487a2646
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405914"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="5f551-107">Lettura dell'utente che non può modificare la password (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="5f551-107">Reading User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="5f551-108">La possibilità di un utente di modificare la propria password è un'autorizzazione che può essere concessa o negata.</span><span class="sxs-lookup"><span data-stu-id="5f551-108">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="5f551-109">Per determinare se all'utente è stata concessa questa autorizzazione con il provider WinNT, leggere il flag **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** dell'oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="5f551-109">To determine if the user has been granted this permission with the WinNT provider, read the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of the user object.</span></span> <span data-ttu-id="5f551-110">Il flag **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE** è definito nell'enumerazione [**ADS \_ USER FLAG \_ \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)</span><span class="sxs-lookup"><span data-stu-id="5f551-110">The **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag is defined in the [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) enumeration.</span></span>

## <a name="example-code"></a><span data-ttu-id="5f551-111">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="5f551-111">Example Code</span></span>

<span data-ttu-id="5f551-112">Nell'esempio di codice seguente viene illustrato come ottenere il flag **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="5f551-112">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



<span data-ttu-id="5f551-113">Nell'esempio di codice seguente viene illustrato come ottenere il flag **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** della **proprietà userFlags** di un oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="5f551-113">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



 

 




