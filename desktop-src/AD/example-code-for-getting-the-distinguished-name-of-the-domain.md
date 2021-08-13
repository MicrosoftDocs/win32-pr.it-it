---
title: Codice di esempio per ottenere il nome distinto del dominio
description: In questo argomento è incluso un esempio di codice che ottiene il nome distinto del dominio di cui il computer locale è membro utilizzando l'associazione serverless.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory è un esempio di Active Directory, ottenendo il nome distinto del dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ebf027e6c95915e34b70f942fdbf342b3f49b9695d7885c442f015d2a74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693645"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Codice di esempio per ottenere il nome distinto del dominio

In questo argomento è incluso un esempio di codice che ottiene il nome distinto del dominio di cui il computer locale è membro utilizzando l'associazione serverless.

Nell'Visual Basic di codice seguente viene ottiene il nome distinto del dominio di cui il computer locale è membro utilizzando l'associazione serverless.


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



L'esempio di codice C# seguente ottiene il nome distinto del dominio di cui il computer locale è membro usando l'associazione serverless.


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



L'esempio di codice C/C++ seguente ottiene il nome distinto del dominio di cui il computer locale è membro usando l'associazione serverless.


```C++
IADs *pads;
hr = ADsGetObject(  L"LDAP://rootDSE",
                    IID_IADs, 
                    (void**)&pads);

if(SUCCEEDED(hr))
{
    VARIANT var;

    VariantInit(&var);
    
    hr = pads->Get(CComBSTR("defaultNamingContext"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_BSTR == var.vt)
        {
            wprintf(var.bstrVal);
        }
        
        VariantClear(&var);
    }
    
    pads->Release();
}
```



 

 




