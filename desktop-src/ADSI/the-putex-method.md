---
title: Metodo PutEx
description: Il metodo PutEx IADs usa il nome di una proprietà per salvare una proprietà con uno o più valori nella cache delle proprietà.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI , about
- Il codice ADSI ADSI Visual Basic ,usando il metodo PutEx
- proprietà ADSI, salvataggio di una proprietà singola o multivalore nella cache delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c07fad5d22110d345b71a763add5483d7f0be5f6ae2c36557eb7f1563561c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023169"
---
# <a name="the-putex-method"></a>Metodo PutEx

Il [**metodo IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa il nome di una proprietà per salvare una proprietà con uno o più valori nella cache delle proprietà. Questo sovrascrive qualsiasi valore attualmente presente nella cache delle proprietà. I valori nella cache non vengono scritti nel servizio directory sottostante fino a quando non si verifica [**un IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Il primo argomento di **PutEx** indica se si vuole sostituire o aggiungere valori esistenti per la proprietà. Nell'esempio seguente tutti i valori esistenti dell'attributo **description** vengono cancellati nella cache quando viene chiamato **PutEx** e cancellati nel server quando viene chiamato **SetInfo.**


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




