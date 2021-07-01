---
title: Funzionalità del linguaggio ODL in MIDL
description: Object Description Language (ODL), parole chiave, istruzioni e direttive che fanno parte di MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL e ODL MIDL , funzionalità del linguaggio
- ODL MIDL , in MIDL
- ODL MIDL , attributi
- ODL MIDL, parole chiave
- Istruzioni MIDL ODL ,
- ODL MIDL , direttive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db346a664ed7b8f7beeacfe73cc928a924befe10
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119786"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="729ea-109">Funzionalità del linguaggio ODL in MIDL</span><span class="sxs-lookup"><span data-stu-id="729ea-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="729ea-110">Lo Mktyplib.exe è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="729ea-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="729ea-111">Usare invece il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="729ea-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="729ea-112">Negli argomenti seguenti sono elencati gli Object Description Language (ODL), le parole chiave, le istruzioni e le direttive che fanno ora parte di Microsoft Interface Definition Language (MIDL):</span><span class="sxs-lookup"><span data-stu-id="729ea-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="729ea-113">Attributi ODL</span><span class="sxs-lookup"><span data-stu-id="729ea-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="729ea-114">Parole chiave, istruzioni e direttive ODL</span><span class="sxs-lookup"><span data-stu-id="729ea-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="729ea-115">Attributi ODL</span><span class="sxs-lookup"><span data-stu-id="729ea-115">ODL Attributes</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="729ea-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-116">\[[**appobject**](appobject.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-117">\[[**Associabile**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-117">\[[**bindable**](bindable.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-118">\[[**Controllo**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-118">\[[**control**](control.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-119">\[[**Predefinito**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-119">\[[**default**](default.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-120">\[[**Defaultvalue**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-121">\[[**displaybind**](displaybind.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-122">\[[**Dllname**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-122">\[[**dllname**](dllname-str-.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-123">\[[**Dual**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-123">\[[**dual**](dual.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-124">\[[**Voce**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-124">\[[**entry**](entry.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-125">\[[**Helpcontext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-125">\[[**helpcontext**](helpcontext.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-126">\[[**Helpstring**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-126">\[[**helpstring**](helpstring.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-127">\[[**Helpfile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-127">\[[**helpfile**](helpfile.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-128">\[[**Nascosto**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-128">\[[**hidden**](hidden.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-129">\[[**Id**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-129">\[[**id**](id.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-130">\[[**immediatebind**](immediatebind.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-131">\[[**Pollici**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-131">\[[**in**](in.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-132">\[[**Lcid**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-132">\[[**lcid**](lcid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-133">\[[**Licenza**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-133">\[[**licensed**](licensed.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-134">\[[**non estensibile**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-134">\[[**nonextensible**](nonextensible.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-135">\[[**odl**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-135">\[[**odl**](odl.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-136">\[[**oleautomation**](oleautomation.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-137">\[[**Opzionale**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-137">\[[**optional**](optional.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-138">\[[**Cambio**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-138">\[[**out**](out-idl.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-139">\[[**propget**](propget.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-140">\[[**propput**](propput.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-141">\[[**propputref**](propputref.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-142">\[[**Pubblico**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-142">\[[**public**](public.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-143">\[[ **readonly**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-143">\[ [**readonly**](readonly.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-144">\[[**requestedit**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-144">\[[**requestedit**](requestedit.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-145">\[[**Limitato**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-145">\[[**restricted**](restricted.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-146">\[[**Retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-146">\[[**retval**](retval.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-147">\[[**fonte**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-147">\[[**source**](source.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-148">\[[**Uuid**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-148">\[[**uuid**](uuid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-149">[**vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-149">[**vararg**](vararg.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="729ea-150">\[[**Versione**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-150">\[[**version**](version.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="729ea-151">Â</span><span class="sxs-lookup"><span data-stu-id="729ea-151">Â</span></span>
    :::column-end:::
:::row-end:::

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="729ea-152">Parole chiave, istruzioni e direttive ODL</span><span class="sxs-lookup"><span data-stu-id="729ea-152">ODL Keywords, Statements, and Directives</span></span>

[<span data-ttu-id="729ea-153">**coclass**</span><span class="sxs-lookup"><span data-stu-id="729ea-153">**coclass**</span></span>](coclass.md)

[<span data-ttu-id="729ea-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="729ea-154">**dispinterface**</span></span>](dispinterface.md)

[<span data-ttu-id="729ea-155">**Enum**</span><span class="sxs-lookup"><span data-stu-id="729ea-155">**enum**</span></span>](enum.md)

<span data-ttu-id="729ea-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="729ea-156">\[[**importlib**](importlib.md)\]</span></span>

[<span data-ttu-id="729ea-157">**Interfaccia**</span><span class="sxs-lookup"><span data-stu-id="729ea-157">**interface**</span></span>](interface.md)

[<span data-ttu-id="729ea-158">**library**</span><span class="sxs-lookup"><span data-stu-id="729ea-158">**library**</span></span>](library.md)

[<span data-ttu-id="729ea-159">**Modulo**</span><span class="sxs-lookup"><span data-stu-id="729ea-159">**module**</span></span>](module.md)

[<span data-ttu-id="729ea-160">**Struct**</span><span class="sxs-lookup"><span data-stu-id="729ea-160">**struct**</span></span>](struct.md)

[<span data-ttu-id="729ea-161">**Typedef**</span><span class="sxs-lookup"><span data-stu-id="729ea-161">**typedef**</span></span>](typedef.md)

[<span data-ttu-id="729ea-162">**Unione**</span><span class="sxs-lookup"><span data-stu-id="729ea-162">**union**</span></span>](union.md)

<span data-ttu-id="729ea-163">Per informazioni su come effettuare il marshalling di tipi di automazione OLE, ad esempio **BSTR,** **VARIANT** e **SAFEARRAY,** vedere [Marshalling OLE Data Types](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="729ea-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




