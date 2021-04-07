---
title: Metodo PutEx
description: Il metodo IADs PutEx usa il nome di una proprietà per salvare una proprietà con uno o più valori nella cache delle proprietà.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI, informazioni
- ADSI ADSI, esempio di codice Visual Basic, utilizzo del metodo PutEx
- Proprietà ADSI, salvataggio di una proprietà singola o multivalore nella cache delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855241"
---
# <a name="the-putex-method"></a>Metodo PutEx

Il metodo [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa il nome di una proprietà per salvare una proprietà con uno o più valori nella cache delle proprietà. Questa operazione sovrascrive tutti i valori attualmente presenti nella cache delle proprietà. I valori nella cache non vengono scritti nel servizio directory sottostante fino a quando non si verifica [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Il primo argomento di **PutEx** indica se si desidera sostituire o aggiungere i valori esistenti per la proprietà. Nell'esempio seguente, tutti i valori esistenti dell'attributo **Description** vengono cancellati nella cache quando viene chiamato **PutEx** e cancellati nel server quando viene chiamato il metodo **seinfo** .


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



 

 




