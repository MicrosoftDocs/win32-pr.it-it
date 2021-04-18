---
title: Metodo GetEx
description: Alcuni attributi possono archiviare uno o più valori.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, uso di IADs GetEx
- ADSI ADSI, utilizzo di, utilizzo del metodo IADs GetEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297643"
---
# <a name="the-getex-method"></a>Metodo GetEx

Alcuni attributi possono archiviare uno o più valori. Ad esempio, l'attributo **OtherTelephone** di un oggetto utente in Active Directory è una proprietà che può avere zero, uno o più valori. Gli attributi con più valori sono noti come "attributi multivalore". Se il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) viene utilizzato per recuperare un attributo multivalore, i risultati devono essere elaborati in modo diverso rispetto a se l'attributo ha un singolo valore. I risultati forniti dal metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) , tuttavia, vengono elaborati nello stesso modo, indipendentemente dal fatto che l'attributo abbia un solo valore o più valori. In entrambi i casi, il metodo **IADs:: GetEx** restituisce i valori in una matrice.

Il metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera le proprietà dalla cache delle proprietà. Se la proprietà specificata non viene trovata nella cache, **IADs:: GetEx** esegue una chiamata implicita a [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .

Il metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituisce una matrice di varianti Variant indipendentemente dal numero di valori restituiti dal server. Questo vale anche se l'attributo contiene solo un valore.


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Il metodo [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) può essere usato anche per gli attributi a valore singolo. I risultati di un attributo a valore singolo vengono elaborati come i risultati di un attributo multivalore.


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Se non è impostato alcun valore per l'attributo, [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituisce l'errore "proprietà non trovata nella cache".

 

 




