---
title: L'utente deve modificare la password all'accesso successivo (provider WinNT)
description: Per abilitare questa opzione, impostare l'attributo PasswordExpired dell'utente su uno (1). L'impostazione di questo attributo su zero (0) consente all'utente di accedere senza modificare la password.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- L'utente deve modificare la password all'accesso successivo (provider WinNT) ADSI
- L'utente deve modificare la password all'accesso successivo ADSI , provider WinNT
- Provider WINNT ADSI, esempi di gestione degli utenti, modifica della password all'accesso successivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be50e5cdccb4969e59a5b32516a35278b867062e8cced2e80d96b26c56c6173b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023039"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>L'utente deve modificare la password all'accesso successivo (provider WinNT)

Per abilitare questa opzione, impostare **l'attributo PasswordExpired** dell'utente su uno (1). L'impostazione di questo attributo su zero (0) consente all'utente di accedere senza modificare la password.

## <a name="example-1"></a>Esempio 1

Nell'esempio di codice seguente viene illustrato come impostare l'opzione change password on next logon usando Visual Basic con ADSI.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Esempio 2

Nell'esempio di codice seguente viene illustrato come impostare l'opzione change password on next logon usando C++ con ADSI.


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




