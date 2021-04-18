---
title: L'utente deve modificare la password all'accesso successivo (provider WinNT)
description: Per abilitare questa opzione, impostare l'attributo PasswordExpired dell'utente su uno (1). L'impostazione di questo attributo su zero (0) consente all'utente di accedere senza modificare la password.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- Modificare la password all'accesso successivo (provider WinNT) ADSI
- L'utente deve modificare la password all'accesso successivo ADSI, provider WinNT
- ADSI provider ADSI, esempi di gestione degli utenti, è necessario modificare la password all'accesso successivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322016"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a><span data-ttu-id="67da1-107">L'utente deve modificare la password all'accesso successivo (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="67da1-107">User Must Change Password at Next Logon (WinNT Provider)</span></span>

<span data-ttu-id="67da1-108">Per abilitare questa opzione, impostare l'attributo **PasswordExpired** dell'utente su uno (1).</span><span class="sxs-lookup"><span data-stu-id="67da1-108">To enable this option, set the **PasswordExpired** attribute of the user to one (1).</span></span> <span data-ttu-id="67da1-109">L'impostazione di questo attributo su zero (0) consente all'utente di accedere senza modificare la password.</span><span class="sxs-lookup"><span data-stu-id="67da1-109">Setting this attribute to zero (0) enables the user to log on without changing the password.</span></span>

## <a name="example-1"></a><span data-ttu-id="67da1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67da1-110">Example 1</span></span>

<span data-ttu-id="67da1-111">Nell'esempio di codice seguente viene illustrato come impostare l'opzione Cambia password all'accesso successivo utilizzando Visual Basic con ADSI.</span><span class="sxs-lookup"><span data-stu-id="67da1-111">The following code example shows how to set the change password on next logon option using Visual Basic with ADSI.</span></span>


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="67da1-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="67da1-112">Example 2</span></span>

<span data-ttu-id="67da1-113">Nell'esempio di codice seguente viene illustrato come impostare l'opzione Cambia password all'accesso successivo utilizzando C++ con ADSI.</span><span class="sxs-lookup"><span data-stu-id="67da1-113">The following code example shows how to set the change password on next logon option using C++ with ADSI.</span></span>


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



 

 




