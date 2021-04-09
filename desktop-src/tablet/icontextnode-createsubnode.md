---
description: Crea un nuovo oggetto IContextNode figlio.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Metodo IContextNode:: CreateSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879365"
---
# <a name="icontextnodecreatesubnode-method"></a><span data-ttu-id="87ca7-103">Metodo IContextNode:: CreateSubNode</span><span class="sxs-lookup"><span data-stu-id="87ca7-103">IContextNode::CreateSubNode method</span></span>

<span data-ttu-id="87ca7-104">Crea un nuovo oggetto [**IContextNode**](icontextnode.md) figlio.</span><span class="sxs-lookup"><span data-stu-id="87ca7-104">Creates a new child [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ca7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87ca7-105">Syntax</span></span>


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="87ca7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87ca7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ca7-107">*pNodeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87ca7-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ca7-108">**GUID** che rappresenta il tipo di [**IContextNode**](icontextnode.md) da creare.</span><span class="sxs-lookup"><span data-stu-id="87ca7-108">A **GUID** that represents the type of [**IContextNode**](icontextnode.md) to create.</span></span>

</dd> <dt>

<span data-ttu-id="87ca7-109">*ppContextNodeCreated* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="87ca7-109">*ppContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87ca7-110">Puntatore al nuovo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="87ca7-110">A pointer to the new [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ca7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87ca7-111">Return value</span></span>

<span data-ttu-id="87ca7-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="87ca7-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87ca7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="87ca7-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="87ca7-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextNodeCreated* quando non è più necessario usare il nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="87ca7-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="87ca7-115">Il nuovo [**IContextNode**](icontextnode.md) viene aggiunto alla raccolta di nodi figlio del nodo di contesto (vedere [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="87ca7-115">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="87ca7-116">Quando sono presenti nodi figlio esistenti, il **IContextNode** appena creato viene aggiunto come ultimo nodo figlio.</span><span class="sxs-lookup"><span data-stu-id="87ca7-116">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="87ca7-117">Per un elenco dei tipi di nodo di contesto, vedere [tipi di nodo di contesto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="87ca7-117">For a list of context node types, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87ca7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87ca7-118">Requirements</span></span>



| <span data-ttu-id="87ca7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ca7-119">Requirement</span></span> | <span data-ttu-id="87ca7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="87ca7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ca7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ca7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87ca7-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="87ca7-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="87ca7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ca7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87ca7-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="87ca7-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="87ca7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87ca7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ca7-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="87ca7-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="87ca7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="87ca7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87ca7-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87ca7-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="87ca7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87ca7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ca7-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="87ca7-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="87ca7-131">**IContextNode::D eleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="87ca7-131">**IContextNode::DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)
</dt> <dt>

[<span data-ttu-id="87ca7-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="87ca7-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

