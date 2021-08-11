---
title: Account disabilitato (provider WinNT)
description: Quando si usa il provider WinNT, un account può essere abilitato o disabilitato usando la proprietà IADsUser.AccountDisabled.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Account disabilitato (provider WinNT)
- Account disabilitato ADSI, provider WinNT
- Provider WinNT ADSI, esempi di gestione utenti, Account disabilitato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1659bad4ab930615aed7d02e3c54fc3899b60eb476999676ff765fe2a2e94f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178506"
---
# <a name="account-disabled-winnt-provider"></a>Account disabilitato (provider WinNT)

Quando si usa il provider WinNT, un account può essere abilitato o disabilitato usando la [**proprietà IADsUser.AccountDisabled.**](iadsuser-property-methods.md)

## <a name="example-1"></a>Esempio 1

L'esempio di codice seguente illustra come disabilitare un account usando Visual Basic con ADSI.


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

L'esempio di codice seguente illustra come disabilitare un account usando C++ con ADSI.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




