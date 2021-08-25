---
title: Supporto dell'associazione tardiva
description: Quando è disponibile il supporto per l'associazione tardiva, ogni chiamata di funzione deve passare attraverso l'interfaccia IDispatch ADSI prima di essere reindirizzata all'estensione appropriata.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, supporto dell'associazione tardiva
- AdSI ADSI, codice di esempio Visual Basic, supporto dell'associazione tardiva
- associazione ad Active Directory, supporto dell'associazione tardiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff8a66764e49e912e7d4db61356c997516b8d2192046912e673640e9567e415
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821321"
---
# <a name="late-binding-support"></a>Supporto dell'associazione tardiva

Quando è disponibile il supporto per l'associazione tardiva, ogni chiamata di funzione deve passare attraverso l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ADSI prima di essere reindirizzata all'estensione appropriata.

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



Non sono presenti chiamate esplicite **al metodo QueryInterface** per ottenere le estensioni. Le estensioni devono reindirizzare [**le chiamate IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) all'interfaccia **IDispatch** ADSI. ADSI prende la decisione e risolve eventuali conflitti che si verificano, quindi esegue nuovamente il route all'estensione appropriata usando un'interfaccia denominata [**IADsExtension.**](/windows/desktop/api/Iads/nn-iads-iadsextension) Pertanto, qualsiasi estensione che supporta l'associazione tardiva deve implementare **IADsExtension.**

 

 