---
title: hidden (attributo)
description: L'attributo \ Hidden \ indica che l'elemento esiste ma non deve essere visualizzato in un browser orientato all'utente.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- attributo MIDL nascosto
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299640"
---
# <a name="hidden-attribute"></a><span data-ttu-id="624a7-104">hidden (attributo)</span><span class="sxs-lookup"><span data-stu-id="624a7-104">hidden attribute</span></span>

<span data-ttu-id="624a7-105">L'attributo **\[ Hidden \]** indica che l'elemento esiste ma non deve essere visualizzato in un browser orientato all'utente.</span><span class="sxs-lookup"><span data-stu-id="624a7-105">The **\[hidden\]** attribute indicates that the item exists but should not be displayed in a user-oriented browser.</span></span>

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="624a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="624a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="624a7-107">*altri attributi*</span><span class="sxs-lookup"><span data-stu-id="624a7-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="624a7-108">Zero o più attributi MIDL facoltativi.</span><span class="sxs-lookup"><span data-stu-id="624a7-108">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="624a7-109">*elemento*</span><span class="sxs-lookup"><span data-stu-id="624a7-109">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="624a7-110">Una delle direttive seguenti: [**coclasse**](coclass.md), interfaccia [**Dispatch**](dispinterface.md), [**interfaccia**](interface.md)o [**libreria**](library.md).</span><span class="sxs-lookup"><span data-stu-id="624a7-110">One of the following directives: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), or [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="624a7-111">*Nome elemento*</span><span class="sxs-lookup"><span data-stu-id="624a7-111">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="624a7-112">Nome che altri componenti software possono utilizzare per delineare l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="624a7-112">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="624a7-113">*definizioni*</span><span class="sxs-lookup"><span data-stu-id="624a7-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="624a7-114">Specifica le istruzioni che compongono la definizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="624a7-114">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="624a7-115">*tipo di funzione*</span><span class="sxs-lookup"><span data-stu-id="624a7-115">*function-type*</span></span> 
</dt> <dd>

<span data-ttu-id="624a7-116">Tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="624a7-116">Return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="624a7-117">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="624a7-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="624a7-118">Nome usato per richiamare la funzione.</span><span class="sxs-lookup"><span data-stu-id="624a7-118">Name used for invoking the function.</span></span>

</dd> <dt>

<span data-ttu-id="624a7-119">*facoltativo-parameter-list*</span><span class="sxs-lookup"><span data-stu-id="624a7-119">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="624a7-120">Zero o più parametri di funzione.</span><span class="sxs-lookup"><span data-stu-id="624a7-120">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="624a7-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="624a7-121">Remarks</span></span>

<span data-ttu-id="624a7-122">L'attributo **\[ Hidden \]** consente di rimuovere membri dall'interfaccia (mediante la schermatura da un ulteriore utilizzo) mantenendo la compatibilità con il codice esistente.</span><span class="sxs-lookup"><span data-stu-id="624a7-122">The **\[hidden\]** attribute allows you to remove members from your interface (by shielding them from further use) while maintaining compatibility with existing code.</span></span> <span data-ttu-id="624a7-123">È possibile usare l'attributo **\[ \] Hidden** per le proprietà, i metodi e le istruzioni [**coclass**](coclass.md), [**Dispatch**](dispinterface.md), [**Interface**](interface.md)e [**Library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="624a7-123">You can use the **\[hidden\]** attribute on properties, methods, and the [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), and [**library**](library.md) statements.</span></span>

<span data-ttu-id="624a7-124">Quando viene specificato per una libreria, l'attributo **\[ Hidden \]** impedisce la visualizzazione dell'intera libreria.</span><span class="sxs-lookup"><span data-stu-id="624a7-124">When specified for a library, the **\[hidden\]** attribute prevents the entire library from being displayed.</span></span> <span data-ttu-id="624a7-125">Questo utilizzo è pensato per i controlli.</span><span class="sxs-lookup"><span data-stu-id="624a7-125">This usage is intended for use with controls.</span></span> <span data-ttu-id="624a7-126">Gli host devono creare una nuova libreria dei tipi che esegue il wrapping del controllo con le proprietà estese.</span><span class="sxs-lookup"><span data-stu-id="624a7-126">Hosts need to create a new type library that wraps the control with extended properties.</span></span>

### <a name="flags"></a><span data-ttu-id="624a7-127">Flags</span><span class="sxs-lookup"><span data-stu-id="624a7-127">Flags</span></span>

<span data-ttu-id="624a7-128">VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TypeFlag \_ FHIDDEN</span><span class="sxs-lookup"><span data-stu-id="624a7-128">VARFLAG\_FHIDDEN, FUNCFLAG\_FHIDDEN, TYPEFLAG\_FHIDDEN</span></span>

## <a name="examples"></a><span data-ttu-id="624a7-129">Esempi</span><span class="sxs-lookup"><span data-stu-id="624a7-129">Examples</span></span>

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="624a7-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="624a7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624a7-131">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="624a7-131">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="624a7-132">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="624a7-132">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="624a7-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="624a7-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="624a7-134">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="624a7-134">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="624a7-135">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="624a7-135">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="624a7-136">**libreria**</span><span class="sxs-lookup"><span data-stu-id="624a7-136">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="624a7-137">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="624a7-137">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="624a7-138">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="624a7-138">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 