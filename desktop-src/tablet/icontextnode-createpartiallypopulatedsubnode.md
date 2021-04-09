---
description: Crea un oggetto IContextNode figlio contenente solo le informazioni sul tipo, l'identificatore e la posizione.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Metodo IContextNode:: CreatePartiallyPopulatedSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879366"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a><span data-ttu-id="78ef3-103">Metodo IContextNode:: CreatePartiallyPopulatedSubNode</span><span class="sxs-lookup"><span data-stu-id="78ef3-103">IContextNode::CreatePartiallyPopulatedSubNode method</span></span>

<span data-ttu-id="78ef3-104">Crea un oggetto [**IContextNode**](icontextnode.md) figlio contenente solo le informazioni sul tipo, l'identificatore e la posizione.</span><span class="sxs-lookup"><span data-stu-id="78ef3-104">Creates a child [**IContextNode**](icontextnode.md) object that contains only information about type, identifier, and location.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ef3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78ef3-105">Syntax</span></span>


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="78ef3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78ef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78ef3-107">*pNodeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78ef3-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ef3-108">Tipo di nodo di contesto da creare.</span><span class="sxs-lookup"><span data-stu-id="78ef3-108">The type of context node to create.</span></span>

</dd> <dt>

<span data-ttu-id="78ef3-109">*pNodeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78ef3-109">*pNodeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ef3-110">Identificatore del nuovo nodo.</span><span class="sxs-lookup"><span data-stu-id="78ef3-110">The identifier for the new node.</span></span>

</dd> <dt>

<span data-ttu-id="78ef3-111">*pNodeLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78ef3-111">*pNodeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ef3-112">Posizione del nuovo nodo.</span><span class="sxs-lookup"><span data-stu-id="78ef3-112">The location of the new node.</span></span>

</dd> <dt>

<span data-ttu-id="78ef3-113">*pPartiallyPopulatedContextNodeCreated* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="78ef3-113">*pPartiallyPopulatedContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78ef3-114">Puntatore alla nuova [**IContextNode**](icontextnode.md)popolata parzialmente.</span><span class="sxs-lookup"><span data-stu-id="78ef3-114">A pointer to the new, partially populated [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78ef3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78ef3-115">Return value</span></span>

<span data-ttu-id="78ef3-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="78ef3-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78ef3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="78ef3-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="78ef3-118">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pPartiallyPopulatedContextNodeCreated* quando non è più necessario usare il nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="78ef3-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pPartiallyPopulatedContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="78ef3-119">Il nuovo [**IContextNode**](icontextnode.md) viene aggiunto alla raccolta di nodi figlio del nodo di contesto (vedere [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="78ef3-119">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="78ef3-120">Quando sono presenti nodi figlio esistenti, il **IContextNode** appena creato viene aggiunto come ultimo nodo figlio.</span><span class="sxs-lookup"><span data-stu-id="78ef3-120">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="78ef3-121">Per ulteriori informazioni sul tipo, sull'identificatore e sulla posizione, vedere [**IContextNode:: GetType**](icontextnode-gettype.md), [**IContextNode:: GetId**](icontextnode-getid.md)e [**IContextNode:: getLocation**](icontextnode-getlocation.md).</span><span class="sxs-lookup"><span data-stu-id="78ef3-121">For more information about type, identifier, and location, see [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md), and [**IContextNode::GetLocation**](icontextnode-getlocation.md).</span></span>

<span data-ttu-id="78ef3-122">Questo metodo viene utilizzato per il proxy di dati come un modo per creare un oggetto [**IContextNode**](icontextnode.md) nell'albero del nodo di contesto prima che siano disponibili tutte le informazioni su di esso.</span><span class="sxs-lookup"><span data-stu-id="78ef3-122">This method is used for data proxy as a way to create an [**IContextNode**](icontextnode.md) object in the context node tree before all the information about it is available.</span></span> <span data-ttu-id="78ef3-123">Per altre informazioni, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="78ef3-123">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78ef3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78ef3-124">Requirements</span></span>



| <span data-ttu-id="78ef3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="78ef3-125">Requirement</span></span> | <span data-ttu-id="78ef3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="78ef3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78ef3-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78ef3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="78ef3-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="78ef3-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="78ef3-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78ef3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="78ef3-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78ef3-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="78ef3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78ef3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="78ef3-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="78ef3-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="78ef3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="78ef3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78ef3-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78ef3-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="78ef3-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78ef3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ef3-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="78ef3-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="78ef3-137">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="78ef3-137">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="78ef3-138">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="78ef3-138">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="78ef3-139">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="78ef3-139">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="78ef3-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="78ef3-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

