---
title: Account disabilitato (provider WinNT)
description: Quando si utilizza il provider WinNT, è possibile abilitare o disabilitare un account utilizzando la proprietà IADsUser. AccountDisabled.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Account disabilitato (provider WinNT)
- Account disabilitato ADSI, provider WinNT
- ADSI del provider WinNT, esempi di gestione degli utenti, account disabilitato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104401916"
---
# <a name="account-disabled-winnt-provider"></a><span data-ttu-id="2b7b4-106">Account disabilitato (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="2b7b4-106">Account Disabled (WinNT Provider)</span></span>

<span data-ttu-id="2b7b4-107">Quando si utilizza il provider WinNT, è possibile abilitare o disabilitare un account utilizzando la proprietà [**IADsUser. accountdisabled**](iadsuser-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="2b7b4-107">When using the WinNT provider, an account can be enabled or disabled using the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property.</span></span>

## <a name="example-1"></a><span data-ttu-id="2b7b4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b7b4-108">Example 1</span></span>

<span data-ttu-id="2b7b4-109">Nell'esempio di codice seguente viene illustrato come disabilitare un account utilizzando Visual Basic con ADSI.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-109">The following code example shows how to disable an account using Visual Basic with ADSI.</span></span>


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="2b7b4-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2b7b4-110">Example 2</span></span>

<span data-ttu-id="2b7b4-111">Nell'esempio di codice seguente viene illustrato come disabilitare un account utilizzando C++ con ADSI.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-111">The following code example shows how to disable an account using C++ with ADSI.</span></span>


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




