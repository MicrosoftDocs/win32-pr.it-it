---
title: attributo type_strict_context_handle
description: "\\_ \\_ Per impostare le restrizioni sugli handle di contesto, utilizzare l'handle di contesto Strict \\ Type \\_ \\ in un file ACF."
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- attributo type_strict_context_handle MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472790"
---
# <a name="type_strict_context_handle-attribute"></a><span data-ttu-id="e2bf0-104">Digitare \_ l' \_ attributo dell'handle di contesto Strict \_</span><span class="sxs-lookup"><span data-stu-id="e2bf0-104">type\_strict\_context\_handle attribute</span></span>

<span data-ttu-id="e2bf0-105">Usare l' **\[ \_ \_ \_ handle \] di contesto Strict di tipo** in un file ACF per impostare le restrizioni sugli handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-105">Use the **\[type\_strict\_context\_handle\]** in an ACF file to set restrictions on context handles.</span></span>

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="e2bf0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2bf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2bf0-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e2bf0-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e2bf0-108">Altri attributi di ACF che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="e2bf0-109">Gli attributi validi [**includono \_ handle automatico**](auto-handle.md), [**\_ handle implicito**](implicit-handle.md), [**\_ handle esplicito**](explicit-handle.md)e [**ottimizza**](optimize.md), [**codice**](code.md)o [**NoCode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="e2bf0-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="e2bf0-110">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e2bf0-111">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="e2bf0-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e2bf0-112">Nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="e2bf0-113">*Interface-Definition-Statements*</span><span class="sxs-lookup"><span data-stu-id="e2bf0-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="e2bf0-114">Una o più istruzioni MIDL che definiscono gli elementi dell' [**interfaccia**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="e2bf0-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2bf0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2bf0-115">Remarks</span></span>

<span data-ttu-id="e2bf0-116">Per usare questo attributo, il flag-target deve essere impostato su NT60 (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-116">In order to use this attribute, the -target flag must be set to NT60 (or higher) when running midl.exe.</span></span>

<span data-ttu-id="e2bf0-117">\[\_il tipo \_ strict \_ handle \] di contesto è un superset funzionale dell' \[ handle di \_ contesto Strict \_ \] .</span><span class="sxs-lookup"><span data-stu-id="e2bf0-117">\[type\_strict\_context\_handle\] is a functional superset of \[strict\_context\_handle\].</span></span> <span data-ttu-id="e2bf0-118">In \[ \_ un handle di contesto rigoroso \_ \] , l'ID del tipo dell'handle è sempre 0; nell' \[ handle di contesto Strict del tipo \_ \_ \_ \] , un ID di tipo univoco viene assegnato dal compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-118">In \[strict\_context\_handle\], the type ID of the handle is always 0; in \[type\_strict\_context\_handle\], a unique type ID is assigned by the MIDL compiler.</span></span>

<span data-ttu-id="e2bf0-119">È consigliabile usare un \[ handle di \_ \_ contesto Strict \_ del tipo anziché un \] \[ handle di contesto rigoroso \_ \_ \] .</span><span class="sxs-lookup"><span data-stu-id="e2bf0-119">It is recommended to use \[type\_strict\_context\_handle\] rather than \[strict\_context\_handle\].</span></span> <span data-ttu-id="e2bf0-120">Per impostazione predefinita, gli handle di contesto non sono associati a un tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-120">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="e2bf0-121">Quando nello stesso processo vengono usati più tipi di handle di contesto, è possibile che un client malintenzionato passi un handle di contesto al posto di un altro per produrre risultati non desiderati.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-121">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="e2bf0-122">L'utilizzo di \[ \_ un handle di contesto di tipo strict \_ consente alle \_ \] applicazioni di applicare la coerenza del tipo di handle del contesto ed evitare qualsiasi utilizzo del tipo di handle del contesto non corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e2bf0-122">The use of \[type\_strict\_context\_handle\] allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

<span data-ttu-id="e2bf0-123">Un handle di contesto attribuito con un \[ \_ handle di contesto Strict di tipo \_ \_ \] non può essere attribuito anche con un \[ handle di \_ contesto rigido \_ \] .</span><span class="sxs-lookup"><span data-stu-id="e2bf0-123">A context handle attributed with \[type\_strict\_context\_handle\] cannot also be attributed with \[strict\_context\_handle\].</span></span>

## <a name="see-also"></a><span data-ttu-id="e2bf0-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2bf0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2bf0-125">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="e2bf0-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-126">**codice**</span><span class="sxs-lookup"><span data-stu-id="e2bf0-126">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-127">Handle di contesto</span><span class="sxs-lookup"><span data-stu-id="e2bf0-127">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="e2bf0-128">**\_serializzazione handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="e2bf0-128">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-129">**gestore del contesto \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="e2bf0-129">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-130">**handle esplicito \_**</span><span class="sxs-lookup"><span data-stu-id="e2bf0-130">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-131">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="e2bf0-131">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-132">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="e2bf0-132">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-133">**ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="e2bf0-133">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="e2bf0-134">\_handle di contesto Strict \_</span><span class="sxs-lookup"><span data-stu-id="e2bf0-134">strict\_context\_handle</span></span>](strict-context-handle.md)
</dt> </dl>

 

 