---
title: attributo idempotente
description: L'attributo \ idempotente \ specifica che un'operazione non modifica le informazioni sullo stato e restituisce gli stessi risultati ogni volta che viene eseguita. L'esecuzione della routine più di una volta ha lo stesso effetto dell'esecuzione di una sola volta.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- attributo MIDL di idempotente
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516219"
---
# <a name="idempotent-attribute"></a><span data-ttu-id="1806a-105">attributo idempotente</span><span class="sxs-lookup"><span data-stu-id="1806a-105">idempotent attribute</span></span>

<span data-ttu-id="1806a-106">L'attributo **\[ idempotente \]** specifica che un'operazione non modifica le informazioni di stato e restituisce gli stessi risultati ogni volta che viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="1806a-106">The **\[idempotent\]** attribute specifies that an operation does not modify state information and returns the same results each time it is performed.</span></span> <span data-ttu-id="1806a-107">L'esecuzione della routine più di una volta ha lo stesso effetto dell'esecuzione di una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1806a-107">Performing the routine more than once has the same effect as performing it once.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="1806a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1806a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1806a-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="1806a-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1806a-110">Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="1806a-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="1806a-111">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="1806a-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="1806a-112">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="1806a-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1806a-113">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1806a-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="1806a-114">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="1806a-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1806a-115">Specifica gli attributi aggiuntivi da applicare alla funzione.</span><span class="sxs-lookup"><span data-stu-id="1806a-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="1806a-116">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="1806a-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="1806a-117">*returnType*</span><span class="sxs-lookup"><span data-stu-id="1806a-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="1806a-118">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="1806a-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="1806a-119">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="1806a-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1806a-120">Specifica il nome della funzione a cui verrà applicato l'attributo **\[ idempotente \]** .</span><span class="sxs-lookup"><span data-stu-id="1806a-120">Specifies the name of the function to which the **\[idempotent\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="1806a-121">*params*</span><span class="sxs-lookup"><span data-stu-id="1806a-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="1806a-122">Elenco dei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="1806a-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1806a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="1806a-123">Remarks</span></span>

<span data-ttu-id="1806a-124">RPC supporta due tipi di semantica di chiamata remota: le chiamate alle operazioni con l'attributo **\[ idempotente \]** e le chiamate alle operazioni (operazioni *idempotente* ) senza l'attributo **\[ idempotente \]** (operazioni *non idempotente* ).</span><span class="sxs-lookup"><span data-stu-id="1806a-124">RPC supports two types of remote call semantics: calls to operations with the **\[idempotent\]** attribute and calls to operations (*idempotent* operations) without the **\[idempotent\]** attribute (*non-idempotent* operations).</span></span> <span data-ttu-id="1806a-125">Un'operazione idempotente può essere eseguita più di una volta senza effetti negativi.</span><span class="sxs-lookup"><span data-stu-id="1806a-125">An idempotent operation can be carried out more than once with no ill effect.</span></span> <span data-ttu-id="1806a-126">Viceversa, un'operazione non idempotente non può essere eseguita più di una volta perché restituirà risultati diversi ogni volta o perché modifica uno stato.</span><span class="sxs-lookup"><span data-stu-id="1806a-126">Conversely, a non-idempotent operation cannot be executed more than once because it will either return different results each time or because it modifies some state.</span></span>

<span data-ttu-id="1806a-127">Per assicurarsi che una routine venga eseguita di nuovo automaticamente se la chiamata non viene completata, utilizzare l'attributo **\[ idempotente \]** .</span><span class="sxs-lookup"><span data-stu-id="1806a-127">To ensure that a procedure is automatically re-executed if the call does not complete, use the **\[idempotent\]** attribute.</span></span> <span data-ttu-id="1806a-128">Se gli attributi **\[ \] idempotente**, **\[** [**broadcast**](broadcast.md) **\]** o **\[** [**Maybe**](maybe.md) **\]** non sono presenti, per impostazione predefinita la procedura utilizzerà la semantica non idempotente.</span><span class="sxs-lookup"><span data-stu-id="1806a-128">If the **\[idempotent\]**, **\[**[**broadcast**](broadcast.md)**\]**, or **\[**[**maybe**](maybe.md)**\]** attributes are not present, the procedure will use non-idempotent semantics by default.</span></span> <span data-ttu-id="1806a-129">In questo caso, l'operazione viene eseguita una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1806a-129">In this case, the operation is executed only once.</span></span>

## <a name="see-also"></a><span data-ttu-id="1806a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1806a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1806a-131">**trasmissione**</span><span class="sxs-lookup"><span data-stu-id="1806a-131">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="1806a-132">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="1806a-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="1806a-133">**Forse**</span><span class="sxs-lookup"><span data-stu-id="1806a-133">**maybe**</span></span>](maybe.md)
</dt> </dl>

 

 




