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
# <a name="account-disabled-winnt-provider"></a>Account disabilitato (provider WinNT)

Quando si utilizza il provider WinNT, è possibile abilitare o disabilitare un account utilizzando la proprietà [**IADsUser. accountdisabled**](iadsuser-property-methods.md) .

## <a name="example-1"></a>Esempio 1

Nell'esempio di codice seguente viene illustrato come disabilitare un account utilizzando Visual Basic con ADSI.


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



## <a name="example-2"></a>Esempio 2

Nell'esempio di codice seguente viene illustrato come disabilitare un account utilizzando C++ con ADSI.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




