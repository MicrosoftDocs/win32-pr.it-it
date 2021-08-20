---
title: Scadenza account (provider WinNT)
description: Quando si usa il provider WinNT, la data di scadenza dell'account può essere impostata usando la proprietà IADsUser.AccountExpirationDate.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- Scadenza account ADSI , provider WinNT
- Provider WinNT ADSI, esempi di gestione utenti, scadenza account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd23973a4de31fed629428be9f4df1b6cade34e77f78680a5f87c9d55c42234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838411"
---
# <a name="account-expiration-winnt-provider"></a>Scadenza account (provider WinNT)

Quando si usa il provider WinNT, la data di scadenza dell'account può essere impostata usando la [**proprietà IADsUser.AccountExpirationDate.**](iadsuser-property-methods.md)

Per impostare la data di scadenza dell'account, impostare la proprietà [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) sul valore di data desiderato. Per impostare la data di scadenza dell'account in modo che non scada mai, impostare questa proprietà su "1 gennaio 1970".

## <a name="example-1"></a>Esempio 1

Nell'esempio di codice seguente viene illustrato come impostare la data di scadenza dell'account Visual Basic con ADSI.


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a>Esempio 2

Nell'esempio di codice seguente viene illustrato come impostare la data di scadenza dell'account usando C++ con ADSI.


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



 

 




