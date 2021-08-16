---
title: Metodo Get
description: Il metodo Get IADs viene usato per recuperare singoli attributi denominati da un oggetto directory.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Get ADSI , using IADs Get
- ADSI ADSI ,using, usando il metodo Get IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386c3fe6e50a9f7357ec161b1e6bd8731cf8d0a74eed4b4a765adc3315c1045d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838631"
---
# <a name="the-get-method"></a>Metodo Get

Il [**metodo IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) viene usato per recuperare singoli attributi denominati da un oggetto directory.

Nell'esempio di codice seguente viene utilizzato il [**metodo IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) per recuperare un attributo denominato da un oggetto .


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



Nei linguaggi di automazione è anche possibile accedere direttamente agli attributi denominati usando la notazione del punto. Ad esempio, **object. Get("distinguishedName") è** identico a **object.distinguishedName**.

L'esempio di codice seguente è identico all'esempio precedente, ad eccezione del fatto che si accede **all'attributo distinguishedName** usando la notazione del punto.


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



Se un valore non è impostato sull'oggetto, il metodo [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) restituirà l'errore "Proprietà non trovata nella cache".

 

 




