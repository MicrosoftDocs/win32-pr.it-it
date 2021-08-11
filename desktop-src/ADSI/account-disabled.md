---
title: Account disabilitato (provider LDAP)
description: Per disabilitare un account utente, impostare la proprietà AccountDisabled su TRUE nell'interfaccia IADsUser. È simile al provider WinNT. Gli esempi di codice seguenti illustrano come disabilitare un account utente.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Account disabilitato ADSI , provider LDAP
- Provider LDAP ADSI, esempi di gestione utenti,Account disabilitato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf753da0770e19504d496be20ba350f79bd4788a797eb5241e68261df844b626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181445"
---
# <a name="account-disabled-ldap-provider"></a>Account disabilitato (provider LDAP)

Per disabilitare un account utente, impostare la proprietà AccountDisabled su **TRUE** nell'interfaccia [**IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser) È simile al provider WinNT. Gli esempi di codice seguenti illustrano come disabilitare un account utente.

## <a name="example-1"></a>Esempio 1


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a>Esempio 2


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




