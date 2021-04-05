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
# <a name="late-binding-support"></a><span data-ttu-id="0d31e-106">Supporto per l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="0d31e-106">Late Binding Support</span></span>

<span data-ttu-id="0d31e-107">Quando è presente il supporto per l'associazione tardiva, ogni chiamata di funzione deve passare attraverso l'interfaccia ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , prima che venga reindirizzata all'estensione appropriata.</span><span class="sxs-lookup"><span data-stu-id="0d31e-107">When late binding support is in place, each function call must go through the ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface, before it is rerouted to the appropriate extension.</span></span>

<span data-ttu-id="0d31e-108">Osservare l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="0d31e-108">Consider the following code example.</span></span>


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



<span data-ttu-id="0d31e-109">Non sono presenti chiamate esplicite al metodo **QueryInterface** per ottenere le estensioni.</span><span class="sxs-lookup"><span data-stu-id="0d31e-109">There are no explicit calls to the **QueryInterface** method to get to the extensions.</span></span> <span data-ttu-id="0d31e-110">Le estensioni devono reindirizzare le chiamate [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) all'interfaccia ADSI **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="0d31e-110">The extensions must reroute their [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) calls to the ADSI **IDispatch** interface.</span></span> <span data-ttu-id="0d31e-111">ADSI prende la decisione e risolve tutti i conflitti che si verificano, quindi reindirizza nuovamente all'estensione appropriata usando un'interfaccia denominata [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="0d31e-111">ADSI makes the decision and resolves any conflicts that occur, then it re-routes back to the appropriate extension using an interface called [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span> <span data-ttu-id="0d31e-112">Pertanto, qualsiasi estensione che supporta l'associazione tardiva deve implementare **IADsExtension**.</span><span class="sxs-lookup"><span data-stu-id="0d31e-112">Therefore, any extension that supports late binding must implement **IADsExtension**.</span></span>

 

 