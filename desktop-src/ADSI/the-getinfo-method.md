---
title: Metodo GetInfo
description: Il metodo IADs GetInfo carica tutti i valori di attributo per un oggetto ADSI nella cache locale dal servizio directory sottostante.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- GetInfo ADSI, uso di IADs GetInfo
- ADSI ADSI, utilizzo di, utilizzo del metodo GetInfo IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707372"
---
# <a name="the-getinfo-method"></a>Metodo GetInfo

Il metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) carica tutti i valori di attributo per un oggetto ADSI nella cache locale dal servizio directory sottostante. Il metodo [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) viene usato per caricare valori di attributo specifici nella cache locale. Per ulteriori informazioni sull'utilizzo del metodo **IADs:: GetInfoEx** , vedere [ottimizzazione con GetInfoEx](optimization-using-getinfoex.md).

ADSI effettuerà una chiamata [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implicita quando il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) viene chiamato per un attributo specifico e non viene trovato alcun valore nella cache locale. Quando viene chiamato **IADs:: GetInfo** , una chiamata implicita non viene ripetuta. Se un valore esiste già nella cache delle proprietà, tuttavia, la chiamata al metodo **IADs:: Get** o **IADs:: GetEx** senza prima chiamare **IADs:: GetInfo** recupererà il valore memorizzato nella cache anziché il valore più attuale dalla directory sottostante. Questo può causare la sovrascrittura dei valori degli attributi aggiornati se la cache locale è stata modificata, ma non è stato eseguito il commit dei valori nel servizio directory sottostante con una chiamata al metodo [**IADs:: seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Per evitare problemi di memorizzazione nella cache, è necessario eseguire il commit delle modifiche del valore dell'attributo chiamando **IADs:: seinfo** prima di chiamare **IADs:: GetInfo**.


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



Alcuni servizi directory non restituiscono tutti i valori di attributo per un oggetto in risposta a una chiamata [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) . In questi casi, usare il metodo [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) per caricare questi valori nella cache locale.

 

 




