---
title: source (attributo)
description: L'attributo \ source \ indica che un membro di una coclasse, di una proprietà o di un metodo è un'origine di eventi. Per un membro di una coclasse, questo attributo indica che il membro viene chiamato anziché implementato.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- attributo di origine MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956372"
---
# <a name="source-attribute"></a><span data-ttu-id="80a22-105">source (attributo)</span><span class="sxs-lookup"><span data-stu-id="80a22-105">source attribute</span></span>

<span data-ttu-id="80a22-106">L'attributo di **\[ origine \]** indica che un membro di una [**coclasse**](coclass.md), di una proprietà o di un metodo è un'origine di eventi.</span><span class="sxs-lookup"><span data-stu-id="80a22-106">The **\[source\]** attribute indicates that a member of a [**coclass**](coclass.md), property, or method is a source of events.</span></span> <span data-ttu-id="80a22-107">Per un membro di una **coclasse**, questo attributo indica che il membro viene chiamato anziché implementato.</span><span class="sxs-lookup"><span data-stu-id="80a22-107">For a member of a **coclass**, this attribute means that the member is called rather than implemented.</span></span>

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="80a22-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="80a22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a22-109">*coclass-attributi*</span><span class="sxs-lookup"><span data-stu-id="80a22-109">*coclass-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-110">Zero o più attributi che verranno applicati alla [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="80a22-110">Zero or more attributes that will be applied to the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="80a22-111">*coclass-nome*</span><span class="sxs-lookup"><span data-stu-id="80a22-111">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-112">Identificatore del nome della [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="80a22-112">The name identifier of the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="80a22-113">*facoltativo-attributi*</span><span class="sxs-lookup"><span data-stu-id="80a22-113">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-114">Zero o più attributi MIDL.</span><span class="sxs-lookup"><span data-stu-id="80a22-114">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="80a22-115">*tipo di istruzione*</span><span class="sxs-lookup"><span data-stu-id="80a22-115">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-116">Può essere [**Interface**](interface.md) o [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="80a22-116">Can be [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="80a22-117">*nome istruzione*</span><span class="sxs-lookup"><span data-stu-id="80a22-117">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-118">Nome dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="80a22-118">The name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="80a22-119">*tipo oggetto*</span><span class="sxs-lookup"><span data-stu-id="80a22-119">*object-type*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-120">Tipo dell'oggetto restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="80a22-120">The type of the object that the method returns.</span></span> <span data-ttu-id="80a22-121">Questo oggetto è un'origine di eventi.</span><span class="sxs-lookup"><span data-stu-id="80a22-121">This object is a source of events.</span></span>

</dd> <dt>

<span data-ttu-id="80a22-122">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="80a22-122">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-123">Nome di un metodo in un'interfaccia o in un' [**interfaccia**](interface.md) [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="80a22-123">The name of a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="80a22-124">*facoltativo-parameter-list*</span><span class="sxs-lookup"><span data-stu-id="80a22-124">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="80a22-125">Zero o più parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="80a22-125">Zero or more method parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80a22-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="80a22-126">Remarks</span></span>

<span data-ttu-id="80a22-127">In una proprietà o un metodo l'attributo di **\[ origine \]** indica che il membro restituisce un oggetto o una variante che è un'origine di eventi.</span><span class="sxs-lookup"><span data-stu-id="80a22-127">On a property or method, the **\[source\]** attribute indicates that the member returns an object or VARIANT that is a source of events.</span></span> <span data-ttu-id="80a22-128">L'oggetto implementa **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="80a22-128">The object implements **IConnectionPointContainer**.</span></span>

### <a name="flags"></a><span data-ttu-id="80a22-129">Flags</span><span class="sxs-lookup"><span data-stu-id="80a22-129">Flags</span></span>

<span data-ttu-id="80a22-130">IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ source, FUNCFLAG \_ source</span><span class="sxs-lookup"><span data-stu-id="80a22-130">IMPLTYPEFLAG\_FSOURCE, VARFLAG\_SOURCE, FUNCFLAG\_SOURCE</span></span>

## <a name="examples"></a><span data-ttu-id="80a22-131">Esempi</span><span class="sxs-lookup"><span data-stu-id="80a22-131">Examples</span></span>

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a><span data-ttu-id="80a22-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="80a22-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a22-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="80a22-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="80a22-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="80a22-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="80a22-135">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="80a22-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="80a22-136">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="80a22-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="80a22-137">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="80a22-137">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="80a22-138">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="80a22-138">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="80a22-139">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="80a22-139">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 