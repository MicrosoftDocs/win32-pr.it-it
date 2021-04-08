---
title: Funzionalità del linguaggio FAD in MIDL
description: Attributi Object Description Language (FAD), parole chiave, istruzioni e direttive che fanno parte di MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL e FAD MIDL, funzionalità del linguaggio
- FAD MIDL, in MIDL
- MIDL di FAD, attributi
- FAD MIDL, parole chiave
- MIDL (FAD), istruzioni
- MIDL (FAD), direttive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856730"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="bb2d8-109">Funzionalità del linguaggio FAD in MIDL</span><span class="sxs-lookup"><span data-stu-id="bb2d8-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="bb2d8-110">Lo strumento Mktyplib.exe è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bb2d8-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="bb2d8-111">Usare invece il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="bb2d8-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="bb2d8-112">Gli argomenti seguenti elencano gli attributi Object Description Language (FAD), le parole chiave, le istruzioni e le direttive che fanno ora parte del Microsoft Interface Definition Language (MIDL):</span><span class="sxs-lookup"><span data-stu-id="bb2d8-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="bb2d8-113">Attributi di FAD</span><span class="sxs-lookup"><span data-stu-id="bb2d8-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="bb2d8-114">Parole chiave, istruzioni e direttive di FAD</span><span class="sxs-lookup"><span data-stu-id="bb2d8-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="bb2d8-115">Attributi di FAD</span><span class="sxs-lookup"><span data-stu-id="bb2d8-115">ODL Attributes</span></span>



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="bb2d8-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-116">\[[**appobject**](appobject.md)\]</span></span>         | <span data-ttu-id="bb2d8-117">\[[**associabile**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-117">\[[**bindable**](bindable.md)\]</span></span>       |
| <span data-ttu-id="bb2d8-118">\[[**controllo**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-118">\[[**control**](control.md)\]</span></span>             | <span data-ttu-id="bb2d8-119">\[[**predefinita**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-119">\[[**default**](default.md)\]</span></span>         |
| <span data-ttu-id="bb2d8-120">\[[**DefaultValue**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>   | <span data-ttu-id="bb2d8-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-121">\[[**displaybind**](displaybind.md)\]</span></span> |
| <span data-ttu-id="bb2d8-122">\[[**DllName**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-122">\[[**dllname**](dllname-str-.md)\]</span></span>        | <span data-ttu-id="bb2d8-123">\[[**Dual**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-123">\[[**dual**](dual.md)\]</span></span>               |
| <span data-ttu-id="bb2d8-124">\[[**voce**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-124">\[[**entry**](entry.md)\]</span></span>                 | <span data-ttu-id="bb2d8-125">\[[**HelpContext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-125">\[[**helpcontext**](helpcontext.md)\]</span></span> |
| <span data-ttu-id="bb2d8-126">\[[**helpstring**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-126">\[[**helpstring**](helpstring.md)\]</span></span>       | <span data-ttu-id="bb2d8-127">\[[**HelpFile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-127">\[[**helpfile**](helpfile.md)\]</span></span>       |
| <span data-ttu-id="bb2d8-128">\[[**nascosto**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-128">\[[**hidden**](hidden.md)\]</span></span>               | <span data-ttu-id="bb2d8-129">\[[**ID**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-129">\[[**id**](id.md)\]</span></span>                   |
| <span data-ttu-id="bb2d8-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-130">\[[**immediatebind**](immediatebind.md)\]</span></span> | <span data-ttu-id="bb2d8-131">\[[**in**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-131">\[[**in**](in.md)\]</span></span>                   |
| <span data-ttu-id="bb2d8-132">\[[**LCID**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-132">\[[**lcid**](lcid.md)\]</span></span>                   | <span data-ttu-id="bb2d8-133">\[[**licenza**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-133">\[[**licensed**](licensed.md)\]</span></span>       |
| <span data-ttu-id="bb2d8-134">\[[**PerformanceCategory**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-134">\[[**nonextensible**](nonextensible.md)\]</span></span> | <span data-ttu-id="bb2d8-135">\[[**ODL**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-135">\[[**odl**](odl.md)\]</span></span>                 |
| <span data-ttu-id="bb2d8-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-136">\[[**oleautomation**](oleautomation.md)\]</span></span> | <span data-ttu-id="bb2d8-137">\[[**opzionale**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-137">\[[**optional**](optional.md)\]</span></span>       |
| <span data-ttu-id="bb2d8-138">\[[**out**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-138">\[[**out**](out-idl.md)\]</span></span>                 | <span data-ttu-id="bb2d8-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-139">\[[**propget**](propget.md)\]</span></span>         |
| <span data-ttu-id="bb2d8-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-140">\[[**propput**](propput.md)\]</span></span>             | <span data-ttu-id="bb2d8-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-141">\[[**propputref**](propputref.md)\]</span></span>   |
| <span data-ttu-id="bb2d8-142">\[[**pubblico**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-142">\[[**public**](public.md)\]</span></span>               | <span data-ttu-id="bb2d8-143">\[[ **ReadOnly**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-143">\[ [**readonly**](readonly.md)\]</span></span>      |
| <span data-ttu-id="bb2d8-144">\[[**requestedit**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-144">\[[**requestedit**](requestedit.md)\]</span></span>     | <span data-ttu-id="bb2d8-145">\[[**limitato**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-145">\[[**restricted**](restricted.md)\]</span></span>   |
| <span data-ttu-id="bb2d8-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-146">\[[**retval**](retval.md)\]</span></span>               | <span data-ttu-id="bb2d8-147">\[[**origine**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-147">\[[**source**](source.md)\]</span></span>           |
| <span data-ttu-id="bb2d8-148">\[[**UUID**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-148">\[[**uuid**](uuid.md)\]</span></span>                   | <span data-ttu-id="bb2d8-149">[**vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-149">[**vararg**](vararg.md)\]</span></span>             |
| <span data-ttu-id="bb2d8-150">\[[**Versione**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-150">\[[**version**](version.md)\]</span></span>             | <span data-ttu-id="bb2d8-151">Â</span><span class="sxs-lookup"><span data-stu-id="bb2d8-151">Â</span></span>                                      |



 

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="bb2d8-152">Parole chiave, istruzioni e direttive di FAD</span><span class="sxs-lookup"><span data-stu-id="bb2d8-152">ODL Keywords, Statements, and Directives</span></span>



|                                        |
|----------------------------------------|
| [<span data-ttu-id="bb2d8-153">**coclass**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-153">**coclass**</span></span>](coclass.md)             |
| [<span data-ttu-id="bb2d8-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-154">**dispinterface**</span></span>](dispinterface.md) |
| [<span data-ttu-id="bb2d8-155">**enum**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-155">**enum**</span></span>](enum.md)                   |
| <span data-ttu-id="bb2d8-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="bb2d8-156">\[[**importlib**](importlib.md)\]</span></span>     |
| [<span data-ttu-id="bb2d8-157">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-157">**interface**</span></span>](interface.md)         |
| [<span data-ttu-id="bb2d8-158">**libreria**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-158">**library**</span></span>](library.md)             |
| [<span data-ttu-id="bb2d8-159">**modulo**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-159">**module**</span></span>](module.md)               |
| [<span data-ttu-id="bb2d8-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-160">**struct**</span></span>](struct.md)               |
| [<span data-ttu-id="bb2d8-161">**typedef**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-161">**typedef**</span></span>](typedef.md)             |
| [<span data-ttu-id="bb2d8-162">**Unione**</span><span class="sxs-lookup"><span data-stu-id="bb2d8-162">**union**</span></span>](union.md)                 |



 

<span data-ttu-id="bb2d8-163">Per informazioni su come effettuare il marshalling di tipi di automazione OLE, ad esempio **BSTR**, **Variant** e **SAFEARRAY**, vedere [marshalling di tipi di dati OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="bb2d8-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




