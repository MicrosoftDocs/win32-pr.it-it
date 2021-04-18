---
title: Blocco account (provider WinNT)
description: Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per il numero di minuti specificato dall'attributo lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Blocco account ADSI, provider WinNT
- ADSI del provider WinNT, esempi di gestione degli utenti, blocco degli account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300447"
---
# <a name="account-lockout-winnt-provider"></a><span data-ttu-id="36835-105">Blocco account (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="36835-105">Account Lockout (WinNT Provider)</span></span>

<span data-ttu-id="36835-106">Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per il numero di minuti specificato dall'attributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="36835-106">When the number of failed logon attempts is exceeded, the user account becomes locked out for the number of minutes specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="36835-107">La proprietà [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) sembra essere la proprietà da utilizzare per leggere e modificare lo stato di blocco di un account utente, ma il provider ADSI WinNT presenta restrizioni che limitano l'utilizzo della proprietà **IsAccountLocked** .</span><span class="sxs-lookup"><span data-stu-id="36835-107">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the WinNT ADSI provider has restrictions that limit the use of the **IsAccountLocked** property.</span></span>

## <a name="resetting-the-account-lockout-status"></a><span data-ttu-id="36835-108">Reimpostazione dello stato di blocco dell'account</span><span class="sxs-lookup"><span data-stu-id="36835-108">Resetting the Account Lockout Status</span></span>

<span data-ttu-id="36835-109">Quando si usa il provider WinNT, la proprietà [**IsAccountLocked**](iadsuser-property-methods.md) può essere impostata solo su **false**, per sbloccare l'account.</span><span class="sxs-lookup"><span data-stu-id="36835-109">When using the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can only be set to **FALSE**, which unlocks the account.</span></span> <span data-ttu-id="36835-110">Il tentativo di impostare la proprietà **IsAccountLocked** su **true** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="36835-110">Attempting to set the **IsAccountLocked** property to **TRUE** will fail.</span></span> <span data-ttu-id="36835-111">Un account può essere bloccato solo dal sistema.</span><span class="sxs-lookup"><span data-stu-id="36835-111">Only the system can lock an account.</span></span>

<span data-ttu-id="36835-112">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare Visual Basic con ADSI per sbloccare un account utente.</span><span class="sxs-lookup"><span data-stu-id="36835-112">The following code example demonstrates how to use Visual Basic with ADSI to unlock a user account.</span></span>


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



<span data-ttu-id="36835-113">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare C++ con ADSI per sbloccare un account utente.</span><span class="sxs-lookup"><span data-stu-id="36835-113">The following code example demonstrates how to use C++ with ADSI to unlock a user account.</span></span>


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a><span data-ttu-id="36835-114">Lettura dello stato di blocco dell'account</span><span class="sxs-lookup"><span data-stu-id="36835-114">Reading the Account Lockout Status</span></span>

<span data-ttu-id="36835-115">Con il provider WinNT, è possibile usare la proprietà [**IsAccountLocked**](iadsuser-property-methods.md) per determinare se un account è bloccato. Se un account è bloccato, la proprietà **IsAccountLocked** conterrà **true**.</span><span class="sxs-lookup"><span data-stu-id="36835-115">With the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can be used to determine if an account is locked out. If an account is locked out, the **IsAccountLocked** property will contain **TRUE**.</span></span> <span data-ttu-id="36835-116">Se un account non è bloccato, la proprietà **IsAccountLocked** conterrà **false**.</span><span class="sxs-lookup"><span data-stu-id="36835-116">If an account is not locked out, the **IsAccountLocked** property will contain **FALSE**.</span></span>

<span data-ttu-id="36835-117">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare Visual Basic con ADSI per determinare se un account è bloccato.</span><span class="sxs-lookup"><span data-stu-id="36835-117">The following code example demonstrates how to use Visual Basic with ADSI to determine if an account is locked out.</span></span>


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



<span data-ttu-id="36835-118">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare C++ con ADSI per determinare se un account è bloccato.</span><span class="sxs-lookup"><span data-stu-id="36835-118">The following code example demonstrates how to use C++ with ADSI to determine if an account is locked out.</span></span>


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 