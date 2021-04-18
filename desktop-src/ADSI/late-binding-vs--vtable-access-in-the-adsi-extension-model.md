---
title: Associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI
description: Una doppia interfaccia consente l'accesso diretto a vtable a tutte le relative funzioni, mentre un'interfaccia di dispatch non lo supporta.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI ADSI
- estensioni ADSI, associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI
- ADSI ADSI, esempio di codice Visual Basic, uso di IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300451"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a><span data-ttu-id="e03ba-106">Associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI</span><span class="sxs-lookup"><span data-stu-id="e03ba-106">Late Binding vs. Vtable Access in the ADSI Extension Model</span></span>

<span data-ttu-id="e03ba-107">Una doppia interfaccia consente l'accesso diretto a vtable a tutte le relative funzioni, mentre un'interfaccia di dispatch non lo supporta.</span><span class="sxs-lookup"><span data-stu-id="e03ba-107">A dual interface enables direct vtable access to all its functions while a dispatch interface does not.</span></span> <span data-ttu-id="e03ba-108">Un client C/C++ può eseguire una query per un puntatore a interfaccia duale e usare l'accesso diretto a vtable per richiamare le relative funzioni.</span><span class="sxs-lookup"><span data-stu-id="e03ba-108">A C/C++ client can query for a dual interface pointer and use direct vtable access to invoke its functions.</span></span> <span data-ttu-id="e03ba-109">Questo consente un accesso più rapido rispetto alla chiamata della funzione tramite le funzioni [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="e03ba-109">This provides faster access than invoking the function using the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions.</span></span> <span data-ttu-id="e03ba-110">Ciò è particolarmente vero nel modello di estensione, perché tutte le interfacce duali in un oggetto di estensione devono delegare le funzioni **GetIDsOfNames** e **Invoke** prima di tutto a Aggregator (ADSI).</span><span class="sxs-lookup"><span data-stu-id="e03ba-110">This is especially true in the extension model, because all dual interfaces in an extension object must delegate their **GetIDsOfNames** and **Invoke** functions back to the aggregator (ADSI) first.</span></span> <span data-ttu-id="e03ba-111">L'aggregatore deve quindi eseguire ulteriori passaggi interni per identificare l'oggetto di estensione, eventualmente incluso l'aggregatore stesso, fornisce il supporto per la funzione chiamata e reindirizza la chiamata all'oggetto appropriato.</span><span class="sxs-lookup"><span data-stu-id="e03ba-111">The aggregator then must perform extra internal steps to identify which extension object, possibly including the aggregator itself, provides support for the function called and redirect the call to the appropriate object.</span></span>

<span data-ttu-id="e03ba-112">Visual Basic richiama inoltre una funzione a doppia interfaccia utilizzando l'accesso diretto a un oggetto vtable, se dispone di un puntatore all'interfaccia e l'accesso ai dati del tipo dalla libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="e03ba-112">Visual Basic also invokes a dual-interface function using direct access to a vtable, if it has a pointer to the interface and access to type data from the type library.</span></span> <span data-ttu-id="e03ba-113">I client ADSI scritti in Visual Basic possono specificare un puntatore a un'interfaccia duale, ad esempio [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), in modo esplicito e quindi abilitare l'accesso vtable alle funzioni nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e03ba-113">ADSI clients written in Visual Basic can specify a pointer to a dual interface, for example, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitly, and thus enable vtable access to functions in the interface.</span></span>


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



<span data-ttu-id="e03ba-114">Poiché un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) non supporta l'accesso vtable, questo esempio non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="e03ba-114">Because an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface does not support vtable access, this example does not apply.</span></span> <span data-ttu-id="e03ba-115">Ovvero, una funzione Dispatch viene sempre richiamata tramite le funzioni [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="e03ba-115">That is, a dispatch function is always invoked through the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions only.</span></span>

<span data-ttu-id="e03ba-116">Anche le versioni correnti di VBScript e JScript non supportano l'accesso vtable.</span><span class="sxs-lookup"><span data-stu-id="e03ba-116">Current releases of VBScript and JScript also do not support vtable access.</span></span> <span data-ttu-id="e03ba-117">Pertanto, un'interfaccia duale in un ambiente VBScript o JScript viene eseguita come un'interfaccia dispatch.</span><span class="sxs-lookup"><span data-stu-id="e03ba-117">Therefore, a dual interface in a VBScript or JScript environment performs like a dispatch interface.</span></span>

 

 