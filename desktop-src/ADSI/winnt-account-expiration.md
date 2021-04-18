---
title: Scadenza account (provider WinNT)
description: Quando si utilizza il provider WinNT, è possibile impostare la data di scadenza dell'account utilizzando la proprietà IADsUser. AccountExpirationDate.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- Scadenza account ADSI, provider WinNT
- ADSI del provider WinNT, esempi di gestione degli utenti, scadenza dell'account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4936004cbd68c853f5e6d5c76a405f2a8340d22a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322018"
---
# <a name="account-expiration-winnt-provider"></a><span data-ttu-id="08e7b-105">Scadenza account (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="08e7b-105">Account Expiration (WinNT Provider)</span></span>

<span data-ttu-id="08e7b-106">Quando si utilizza il provider WinNT, è possibile impostare la data di scadenza dell'account utilizzando la proprietà [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="08e7b-106">When using the WinNT provider, the account expiration date can be set using the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property.</span></span>

<span data-ttu-id="08e7b-107">Per impostare la data di scadenza dell'account, impostare la proprietà [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) sul valore di data desiderato.</span><span class="sxs-lookup"><span data-stu-id="08e7b-107">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="08e7b-108">Per impostare la data di scadenza dell'account in modo che non scada mai, impostare questa proprietà su "1 gennaio 1970".</span><span class="sxs-lookup"><span data-stu-id="08e7b-108">To set the account expiration date to never expire, set this property to "January 1, 1970".</span></span>

## <a name="example-1"></a><span data-ttu-id="08e7b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08e7b-109">Example 1</span></span>

<span data-ttu-id="08e7b-110">Nell'esempio di codice seguente viene illustrato come impostare la data di scadenza dell'account utilizzando Visual Basic con ADSI.</span><span class="sxs-lookup"><span data-stu-id="08e7b-110">The following code example shows how to set the account expiration date using Visual Basic with ADSI.</span></span>


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="08e7b-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="08e7b-111">Example 2</span></span>

<span data-ttu-id="08e7b-112">Nell'esempio di codice seguente viene illustrato come impostare la data di scadenza dell'account utilizzando C++ con ADSI.</span><span class="sxs-lookup"><span data-stu-id="08e7b-112">The following code example shows how to set the account expiration date using C++ with ADSI.</span></span>


```C++
void SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
   if(!pUser) return;

   HRESULT hr = S_OK;
   hr = pUser->put_AccountExpirationDate(date); // Set the account to expires on date.
   
   hr = pUser->SetInfo();
   hr = pUser->Release();
   return;
}
```



 

 




