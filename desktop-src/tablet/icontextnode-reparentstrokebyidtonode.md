---
description: Sposta i dati del tratto da questo IContextNode al IContextNode specificato.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'Metodo IContextNode:: ReparentStrokeByIdToNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307418"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a><span data-ttu-id="69fd1-103">Metodo IContextNode:: ReparentStrokeByIdToNode</span><span class="sxs-lookup"><span data-stu-id="69fd1-103">IContextNode::ReparentStrokeByIdToNode method</span></span>

<span data-ttu-id="69fd1-104">Sposta i dati del tratto da questo [**IContextNode**](icontextnode.md) al **IContextNode** specificato.</span><span class="sxs-lookup"><span data-stu-id="69fd1-104">Moves stroke data from this [**IContextNode**](icontextnode.md) to the specified **IContextNode**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69fd1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69fd1-105">Syntax</span></span>


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a><span data-ttu-id="69fd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69fd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69fd1-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69fd1-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69fd1-108">Identificatore del tratto da spostare.</span><span class="sxs-lookup"><span data-stu-id="69fd1-108">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="69fd1-109">*pContextNodeDestination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69fd1-109">*pContextNodeDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69fd1-110">Oggetto [**IContextNode**](icontextnode.md) in cui spostare i dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="69fd1-110">The [**IContextNode**](icontextnode.md) object to which to move the stroke data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69fd1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69fd1-111">Return value</span></span>

<span data-ttu-id="69fd1-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="69fd1-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69fd1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="69fd1-113">Remarks</span></span>

<span data-ttu-id="69fd1-114">L'oggetto [**IContextNode**](icontextnode.md) specificato deve essere uno dei tipi seguenti dalle costanti dei [tipi di nodo di contesto](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** o **UnclassifiedInk**.</span><span class="sxs-lookup"><span data-stu-id="69fd1-114">The specified [**IContextNode**](icontextnode.md) object must be one of the following types from the [Context Node Types](context-node-types.md) constants: **InkWord**, **InkDrawing**, **InkBullet**, or **UnclassifiedInk**.</span></span> <span data-ttu-id="69fd1-115">Il tentativo di spostare un tratto in un altro tipo di oggetto **IContextNode** restituisce un valore restituito di **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="69fd1-115">Attempting to move a stroke to any other type of **IContextNode** object results in a return value of **E\_INVALIDARG**.</span></span>

<span data-ttu-id="69fd1-116">Questo metodo può essere chiamato da qualsiasi oggetto [**IContextNode**](icontextnode.md) , inclusi oggetti **IContextNode** foglia non input penna.</span><span class="sxs-lookup"><span data-stu-id="69fd1-116">This method can be called from any [**IContextNode**](icontextnode.md) object, including non-ink leaf **IContextNode** objects.</span></span> <span data-ttu-id="69fd1-117">È necessario fare riferimento al tratto specificato da uno dei discendenti di questo oggetto **IContextNode** oppure viene restituito **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="69fd1-117">The specified stroke must be referenced by one of the descendants of this **IContextNode** object or **E\_INVALIDARG** is returned.</span></span>

<span data-ttu-id="69fd1-118">Se il [**IContextNode**](icontextnode.md) o **IContextNode** in *pContextNodeDestination* è confermato, viene restituito **E \_ INVALIDARG** (vedere [**IContextNode:: deconfirmed**](icontextnode-isconfirmed.md)).</span><span class="sxs-lookup"><span data-stu-id="69fd1-118">If either this [**IContextNode**](icontextnode.md) or the **IContextNode** in *pContextNodeDestination* is confirmed, **E\_INVALIDARG** is returned (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).</span></span>

<span data-ttu-id="69fd1-119">L'analizzatore input penna non elimina i nodi di contesto vuoti dall'albero dei risultati in risposta a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="69fd1-119">The ink analyzer does not delete empty context nodes from its results tree in response to this method.</span></span>

-   <span data-ttu-id="69fd1-120">Un nodo foglia input penna che non fa riferimento a dati di tratto è un nodo vuoto.</span><span class="sxs-lookup"><span data-stu-id="69fd1-120">An ink leaf node that does not reference any stroke data is an empty node.</span></span>
-   <span data-ttu-id="69fd1-121">Un nodo contenitore che non fa riferimento A nodi figlio è un nodo vuoto.</span><span class="sxs-lookup"><span data-stu-id="69fd1-121">A container node that does not reference any child nodes is an empty node.</span></span>

<span data-ttu-id="69fd1-122">Un nodo vuoto genera errori se si trova nell'albero durante un'operazione di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="69fd1-122">An empty node generates errors if it is in the tree during an ink analysis operation.</span></span> <span data-ttu-id="69fd1-123">Per rimuovere un nodo dalla struttura ad albero dell'analizzatore di input penna, chiamare il metodo [**IContextNode::D eletesubnode**](icontextnode-deletesubnode.md) del nodo padre (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)).</span><span class="sxs-lookup"><span data-stu-id="69fd1-123">To remove a node from the ink analyzer's tree, call the parent node's [**IContextNode::DeleteSubNode**](icontextnode-deletesubnode.md) method (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="69fd1-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69fd1-124">Requirements</span></span>



| <span data-ttu-id="69fd1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="69fd1-125">Requirement</span></span> | <span data-ttu-id="69fd1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="69fd1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69fd1-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69fd1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="69fd1-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="69fd1-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69fd1-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69fd1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="69fd1-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69fd1-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="69fd1-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69fd1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="69fd1-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="69fd1-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69fd1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="69fd1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69fd1-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69fd1-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="69fd1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69fd1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69fd1-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="69fd1-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="69fd1-137">**IContextNode:: setratti**</span><span class="sxs-lookup"><span data-stu-id="69fd1-137">**IContextNode::SetStrokes**</span></span>](icontextnode-setstrokes.md)
</dt> <dt>

[<span data-ttu-id="69fd1-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="69fd1-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




