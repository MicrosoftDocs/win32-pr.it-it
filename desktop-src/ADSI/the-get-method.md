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
# <a name="the-get-method"></a><span data-ttu-id="e9d89-105">Metodo Get</span><span class="sxs-lookup"><span data-stu-id="e9d89-105">The Get Method</span></span>

<span data-ttu-id="e9d89-106">Il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) viene usato per recuperare singoli attributi denominati da un oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="e9d89-106">The [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve individual named attributes from a directory object.</span></span>

<span data-ttu-id="e9d89-107">Nell'esempio di codice seguente viene usato il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) per recuperare un attributo denominato da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9d89-107">The following code example uses the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method to retrieve a named attribute from an object.</span></span>


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



<span data-ttu-id="e9d89-108">Nei linguaggi di automazione è inoltre possibile accedere direttamente agli attributi denominati utilizzando la notazione del punto.</span><span class="sxs-lookup"><span data-stu-id="e9d89-108">In Automation languages, named attributes can also be accessed directly using the dot notation.</span></span> <span data-ttu-id="e9d89-109">Ad esempio, **Object. Get ("Distinguishname")** è identico a **Object. Distinguishname**.</span><span class="sxs-lookup"><span data-stu-id="e9d89-109">For example, **object.Get("distinguishedName")** is identical to **object.distinguishedName**.</span></span>

<span data-ttu-id="e9d89-110">L'esempio di codice seguente è identico all'esempio precedente, con la differenza che è possibile accedere all'attributo **Distinguishname** usando la notazione del punto.</span><span class="sxs-lookup"><span data-stu-id="e9d89-110">The following code example is identical to the previous example except that the **distinguishedName** attribute is accessed using the dot notation.</span></span>


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



<span data-ttu-id="e9d89-111">Se per l'oggetto non è impostato alcun valore, il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) restituirà l'errore "proprietà non trovata nella cache".</span><span class="sxs-lookup"><span data-stu-id="e9d89-111">If a value is not set on the object, the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method will return the error "Property not found in cache".</span></span>

 

 




