---
title: Metodo Get
description: Il metodo IADs Get viene utilizzato per recuperare singoli attributi denominati da un oggetto directory.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Ottenere ADSI, usando IADs Get
- ADSI ADSI, utilizzo di, utilizzo del metodo IADs Get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297644"
---
# <a name="the-get-method"></a>Metodo Get

Il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) viene usato per recuperare singoli attributi denominati da un oggetto directory.

Nell'esempio di codice seguente viene usato il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) per recuperare un attributo denominato da un oggetto.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Nei linguaggi di automazione è inoltre possibile accedere direttamente agli attributi denominati utilizzando la notazione del punto. Ad esempio, **Object. Get ("Distinguishname")** è identico a **Object. Distinguishname**.

L'esempio di codice seguente è identico all'esempio precedente, con la differenza che è possibile accedere all'attributo **Distinguishname** usando la notazione del punto.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Se per l'oggetto non è impostato alcun valore, il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) restituirà l'errore "proprietà non trovata nella cache".

 

 




