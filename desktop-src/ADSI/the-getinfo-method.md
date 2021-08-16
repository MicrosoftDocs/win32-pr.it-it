---
title: Metodo GetInfo
description: Il metodo GetInfo IADs carica tutti i valori di attributo per un oggetto ADSI nella cache locale dal servizio directory sottostante.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- GetInfo ADSI , con IAD GetInfo
- ADSI ADSI ,using,using the IADs GetInfo method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534de8bd667ed33d562ac55b6a70452b6496d0a3d708c55a2cb0fee1a86a8a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838455"
---
# <a name="the-getinfo-method"></a>Metodo GetInfo

Il [**metodo IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) carica tutti i valori di attributo per un oggetto ADSI nella cache locale dal servizio directory sottostante. Il [**metodo IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) viene usato per caricare valori di attributo specifici nella cache locale. Per altre informazioni sull'uso **del metodo IADs::GetInfoEx,** vedere [Ottimizzazione tramite GetInfoEx.](optimization-using-getinfoex.md)

ADSI effettua una chiamata [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implicita quando viene chiamato il metodo [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) per un attributo specifico e non viene trovato alcun valore nella cache locale. Quando **viene chiamato IADs::GetInfo,** una chiamata implicita non viene ripetuta. Se esiste già un valore nella cache delle proprietà, tuttavia, la chiamata al metodo **IADs::Get** o **IADs::GetEx** senza prima chiamare **IADs::GetInfo** recupererà il valore memorizzato nella cache anziché il valore più corrente dalla directory sottostante. Ciò può causare la sovrascrittura dei valori degli attributi aggiornati se la cache locale è stata modificata ma non è stato eseguito il commit dei valori nel servizio directory sottostante con una chiamata al metodo [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Per evitare problemi di memorizzazione nella cache, eseguire il commit delle modifiche al valore dell'attributo chiamando **IADs::SetInfo** prima di **chiamare IADs::GetInfo**.


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



Alcuni servizi directory non restituiscono tutti i valori di attributo per un oggetto in risposta a una chiamata [**IADs::GetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) In questi casi, usare [**il metodo IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) per caricare questi valori nella cache locale.

 

 




