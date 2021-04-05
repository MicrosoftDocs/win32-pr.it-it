---
title: Supporto per l'associazione tardiva
description: Quando è presente il supporto per l'associazione tardiva, ogni chiamata di funzione deve passare attraverso l'interfaccia ADSI IDispatch, prima che venga reindirizzata all'estensione appropriata.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, supporto per l'associazione tardiva
- ADSI ADSI, esempio di codice Visual Basic, supporto per l'associazione tardiva
- Binding AD, supporto dell'associazione tardiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730311"
---
# <a name="late-binding-support"></a>Supporto per l'associazione tardiva

Quando è presente il supporto per l'associazione tardiva, ogni chiamata di funzione deve passare attraverso l'interfaccia ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , prima che venga reindirizzata all'estensione appropriata.

Osservare l'esempio di codice seguente.


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



Non sono presenti chiamate esplicite al metodo **QueryInterface** per ottenere le estensioni. Le estensioni devono reindirizzare le chiamate [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) all'interfaccia ADSI **IDispatch** . ADSI prende la decisione e risolve tutti i conflitti che si verificano, quindi reindirizza nuovamente all'estensione appropriata usando un'interfaccia denominata [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Pertanto, qualsiasi estensione che supporta l'associazione tardiva deve implementare **IADsExtension**.

 

 