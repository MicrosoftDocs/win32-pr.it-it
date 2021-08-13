---
title: Metodo GetEx
description: Alcuni attributi possono archiviare uno o più valori.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI , con IAD GetEx
- ADSI ADSI ,using,using the IADs GetEx method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e656bd6a48830feb725e927f08be1d573e7b0232cf02c16ee87bd7d6a5b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690150"
---
# <a name="the-getex-method"></a>Metodo GetEx

Alcuni attributi possono archiviare uno o più valori. Ad esempio, **l'altro attributoTelephone** di un oggetto utente in Active Directory è una proprietà che può avere zero, uno o molti valori. Gli attributi con più valori sono noti come "attributi multivalore". Se il [**metodo IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) viene usato per recuperare un attributo multivalore, i risultati devono essere elaborati in modo diverso rispetto a se l'attributo ha un singolo valore. I risultati forniti dal [**metodo IADs::GetEx,**](/windows/desktop/api/Iads/nf-iads-iads-getex) tuttavia, vengono elaborati nello stesso modo, indipendentemente dal fatto che l'attributo abbia uno o più valori. In entrambi i casi, **il metodo IADs::GetEx** restituisce i valori in una matrice.

Il [**metodo IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera le proprietà dalla cache delle proprietà. Se la proprietà specificata non viene trovata nella cache, **IADs::GetEx** esegue una chiamata [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implicita.

Il [**metodo IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituisce una matrice di varianti indipendentemente dal numero di valori restituiti dal server. Questo vale anche se l'attributo contiene un solo valore.


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



Il [**metodo IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) può essere usato anche per gli attributi a valore singolo. I risultati di un attributo a valore singolo vengono elaborati come i risultati per un attributo multivalore.


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



Se per l'attributo non è impostato alcun valore, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituisce l'errore "Proprietà non trovata nella cache".

 

 




