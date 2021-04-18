---
title: Nessuna scadenza password (provider WinNT)
description: Per abilitare questa opzione tramite il provider ADSI di WinNT, impostare il \_ flag ADS UF \_ dont \_ expire \_ (0X10000) nell'attributo UserFlags. Nota per Windows 2000 e versioni successive, usare il provider ADSI LDAP per le operazioni di gestione degli utenti, come illustrato.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- Nessuna scadenza password (provider WinNT)
- La password non scade mai con ADSI, provider WinNT
- ADSI provider ADSI, esempi di gestione utenti, nessuna scadenza password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322017"
---
# <a name="password-never-expires-winnt-provider"></a><span data-ttu-id="3abb6-106">Nessuna scadenza password (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="3abb6-106">Password Never Expires (WinNT Provider)</span></span>

<span data-ttu-id="3abb6-107">Per abilitare questa opzione tramite il provider ADSI di WinNT, impostare il flag **Ads \_ UF \_ dont \_ expire \_** (0x10000) nell'attributo **UserFlags** .</span><span class="sxs-lookup"><span data-stu-id="3abb6-107">To enable this option using the WinNT ADSI provider, set the **ADS\_UF\_DONT\_EXPIRE\_PASSWD** (0x10000) flag on the **UserFlags** attribute.</span></span>

> [!Note]  
> <span data-ttu-id="3abb6-108">Per Windows 2000 e versioni successive, usare il provider ADSI LDAP per le operazioni di gestione degli utenti, come illustrato.</span><span class="sxs-lookup"><span data-stu-id="3abb6-108">For Windows 2000 and later, use the LDAP ADSI provider for user management operations as shown.</span></span> <span data-ttu-id="3abb6-109">Per ulteriori informazioni, vedere [Nessuna scadenza password (provider LDAP)](password-never-expires.md).</span><span class="sxs-lookup"><span data-stu-id="3abb6-109">For more information, see [Password Never Expires (LDAP Provider)](password-never-expires.md).</span></span>

 

## <a name="example-1"></a><span data-ttu-id="3abb6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3abb6-110">Example 1</span></span>

<span data-ttu-id="3abb6-111">Nell'esempio di codice seguente viene illustrato come impostare l'opzione Nessuna scadenza password utilizzando Visual Basic con ADSI.</span><span class="sxs-lookup"><span data-stu-id="3abb6-111">The following code example shows how to set the password never expires option using Visual Basic with ADSI.</span></span>


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="3abb6-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3abb6-112">Example 2</span></span>

<span data-ttu-id="3abb6-113">Nell'esempio di codice seguente viene illustrato come impostare l'opzione Nessuna scadenza password utilizzando C++ con ADSI.</span><span class="sxs-lookup"><span data-stu-id="3abb6-113">The following code example shows how to set the password never expires option using C++ with ADSI.</span></span>


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




