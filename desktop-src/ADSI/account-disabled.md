---
title: Account disabilitato (provider LDAP)
description: Per disabilitare un account utente, impostare la proprietà AccountDisabled su TRUE nell'interfaccia IADsUser. Questa operazione è simile al provider WinNT. Gli esempi di codice seguenti illustrano come disabilitare un account utente.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Account disabilitato ADSI, provider LDAP
- Provider LDAP ADSI, esempi di gestione degli utenti, account disabilitato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322020"
---
# <a name="account-disabled-ldap-provider"></a>Account disabilitato (provider LDAP)

Per disabilitare un account utente, impostare la proprietà AccountDisabled su **true** nell'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) . Questa operazione è simile al provider WinNT. Gli esempi di codice seguenti illustrano come disabilitare un account utente.

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



 

 




