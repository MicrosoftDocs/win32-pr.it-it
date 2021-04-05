---
title: attributo strict_context_handle
description: L'attributo \ Strict \_ Context \_ handle \ ACF imposta le restrizioni sugli handle di contesto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- attributo strict_context_handle MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956371"
---
# <a name="strict_context_handle-attribute"></a><span data-ttu-id="e70e4-104">\_attributo handle di contesto Strict \_</span><span class="sxs-lookup"><span data-stu-id="e70e4-104">strict\_context\_handle attribute</span></span>

<span data-ttu-id="e70e4-105">L'attributo di **\[ \_ \_ gestione \] del contesto rigido** ACF imposta le restrizioni sugli handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="e70e4-105">The **\[strict\_context\_handle\]** ACF attribute sets restrictions on context handles.</span></span>

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="e70e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e70e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70e4-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e70e4-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e70e4-108">Altri attributi di ACF che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="e70e4-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="e70e4-109">Gli attributi validi [**includono \_ handle automatico**](auto-handle.md), [**\_ handle implicito**](implicit-handle.md), [**\_ handle esplicito**](explicit-handle.md)e [**ottimizza**](optimize.md), [**codice**](code.md)o [**NoCode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="e70e4-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="e70e4-110">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="e70e4-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-111">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="e70e4-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e70e4-112">Nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e70e4-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-113">*Interface-Definition-Statements*</span><span class="sxs-lookup"><span data-stu-id="e70e4-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="e70e4-114">Una o più istruzioni MIDL che definiscono gli elementi dell' [**interfaccia**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="e70e4-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e70e4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e70e4-115">Remarks</span></span>

<span data-ttu-id="e70e4-116">In genere, quando una chiamata a un metodo di interfaccia genera un handle di contesto, tale handle diventa liberamente disponibile per qualsiasi altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e70e4-116">Normally, when a call to an interface method generates a context handle, that handle becomes freely available to any other interface.</span></span> <span data-ttu-id="e70e4-117">Quando si usa l'attributo **\[ strict \_ Context \_ handle \]** , si garantisce che i metodi di tale interfaccia accettino solo handle di contesto creati da un metodo dalla stessa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e70e4-117">When you use the **\[strict\_context\_handle\]** attribute you guarantee that the methods in that interface will only accept context handles that were created by a method from the same interface.</span></span> <span data-ttu-id="e70e4-118">Le interfacce compilate senza un **\[ \_ \_ handle \] di contesto rigido** non accettano handle di contesto creati in interfacce compilate con un **\[ \_ \_ \] handle di contesto rigido**</span><span class="sxs-lookup"><span data-stu-id="e70e4-118">Interfaces compiled without **\[strict\_context\_handle\]** cannot accept context handles created on interfaces compiled with **\[strict\_context\_handle\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e70e4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e70e4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70e4-120">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="e70e4-120">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="e70e4-121">**codice**</span><span class="sxs-lookup"><span data-stu-id="e70e4-121">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="e70e4-122">Handle di contesto</span><span class="sxs-lookup"><span data-stu-id="e70e4-122">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="e70e4-123">**\_serializzazione handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="e70e4-123">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="e70e4-124">**gestore del contesto \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="e70e4-124">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="e70e4-125">**handle esplicito \_**</span><span class="sxs-lookup"><span data-stu-id="e70e4-125">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="e70e4-126">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="e70e4-126">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="e70e4-127">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="e70e4-127">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="e70e4-128">**ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="e70e4-128">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="e70e4-129">tipo \_ strict \_ handle di contesto \_</span><span class="sxs-lookup"><span data-stu-id="e70e4-129">type\_strict\_context\_handle</span></span>](type-strict-context-handle.md)
</dt> </dl>

 

 