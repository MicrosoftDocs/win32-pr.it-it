---
title: attributo default
description: L'attributo \ default \ indica che l'interfaccia o l'interfaccia dispatch, definita all'interno di una coclasse, rappresenta l'interfaccia di programmabilità predefinita. Questo attributo deve essere utilizzato dai linguaggi macro.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- attributo predefinito MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472846"
---
# <a name="default-attribute"></a><span data-ttu-id="c6a77-105">attributo default</span><span class="sxs-lookup"><span data-stu-id="c6a77-105">default attribute</span></span>

<span data-ttu-id="c6a77-106">L'attributo **\[ \] default** indica che l' [**interfaccia**](interface.md) o l'interfaccia [**Dispatch**](dispinterface.md), definita all'interno di una [**coclasse**](coclass.md), rappresenta l'interfaccia di programmabilità predefinita.</span><span class="sxs-lookup"><span data-stu-id="c6a77-106">The **\[default\]** attribute Indicates that the [**interface**](interface.md) or [**dispinterface**](dispinterface.md), defined within a [**coclass**](coclass.md), represents the default programmability interface.</span></span> <span data-ttu-id="c6a77-107">Questo attributo deve essere utilizzato dai linguaggi macro.</span><span class="sxs-lookup"><span data-stu-id="c6a77-107">This attribute is intended for use by macro languages.</span></span>

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a><span data-ttu-id="c6a77-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6a77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a77-109">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="c6a77-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a77-110">Specifica un numero di identificazione univoco universale per la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="c6a77-110">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6a77-111">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="c6a77-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a77-112">Specifica attributi di [**coclasse**](coclass.md) aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="c6a77-112">Specifies additional [**coclass**](coclass.md) attributes.</span></span> <span data-ttu-id="c6a77-113">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="c6a77-113">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c6a77-114">*coclass-nome*</span><span class="sxs-lookup"><span data-stu-id="c6a77-114">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a77-115">Specifica il nome con cui altri componenti software possono fare riferimento a questa [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="c6a77-115">Specifies the name by which other software components can reference this [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6a77-116">*facoltativo-Interface-attribute*</span><span class="sxs-lookup"><span data-stu-id="c6a77-116">*optional-interface-attribute*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a77-117">L' **\[** attributo di [**origine**](source.md) **\]** , che specifica che un'interfaccia o un'interfaccia dispatch è in uscita, è l'unico altro attributo che può essere usato qui.</span><span class="sxs-lookup"><span data-stu-id="c6a77-117">The **\[**[**source**](source.md)**\]** attribute, which specifies that an interface or dispinterface is outgoing, is the only other attribute that can be used here.</span></span>

</dd> <dt>

<span data-ttu-id="c6a77-118">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="c6a77-118">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a77-119">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c6a77-119">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6a77-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6a77-120">Remarks</span></span>

<span data-ttu-id="c6a77-121">Una [**coclasse**](coclass.md) può avere al massimo due membri **\[ predefiniti \]** .</span><span class="sxs-lookup"><span data-stu-id="c6a77-121">A [**coclass**](coclass.md) may have at most two **\[default\]** members.</span></span> <span data-ttu-id="c6a77-122">Uno rappresenta l'interfaccia di uscita (di origine) o l'interfaccia dispatch e l'altra rappresenta l'interfaccia (sink) in ingresso o l'interfaccia dispatch.</span><span class="sxs-lookup"><span data-stu-id="c6a77-122">One represents the outgoing (source) interface or dispinterface, and the other represents the incoming (sink) interface or dispinterface.</span></span> <span data-ttu-id="c6a77-123">Se non viene specificato l'attributo **\[ default \]** per alcun membro della **coclasse** o del **tipo**, i primi membri in uscita e in ingresso che non dispongono dell' **\[** [**attributo Restricted**](restricted.md) **\]** vengono considerati come valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c6a77-123">If the **\[default\]** attribute is not specified for any member of the **coclass** or **cotype**, the first outgoing and incoming members that do not have the **\[**[**restricted**](restricted.md)**\]** attribute are treated as the defaults.</span></span>

### <a name="flags"></a><span data-ttu-id="c6a77-124">Flags</span><span class="sxs-lookup"><span data-stu-id="c6a77-124">Flags</span></span>

<span data-ttu-id="c6a77-125">\_FDEFAULT IMPLTYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="c6a77-125">IMPLTYPEFLAG\_FDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="c6a77-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="c6a77-126">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a><span data-ttu-id="c6a77-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c6a77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a77-128">**coclass**</span><span class="sxs-lookup"><span data-stu-id="c6a77-128">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="c6a77-129">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="c6a77-129">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="c6a77-130">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="c6a77-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c6a77-131">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="c6a77-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c6a77-132">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="c6a77-132">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c6a77-133">**limitato**</span><span class="sxs-lookup"><span data-stu-id="c6a77-133">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="c6a77-134">**origine**</span><span class="sxs-lookup"><span data-stu-id="c6a77-134">**source**</span></span>](source.md)
</dt> </dl>

 

 