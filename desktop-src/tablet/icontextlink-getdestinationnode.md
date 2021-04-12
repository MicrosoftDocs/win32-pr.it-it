---
description: Recupera l'oggetto IContextNode che rappresenta la destinazione per questo IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Metodo IContextLink:: GetDestinationNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343726"
---
# <a name="icontextlinkgetdestinationnode-method"></a><span data-ttu-id="ecaf2-103">Metodo IContextLink:: GetDestinationNode</span><span class="sxs-lookup"><span data-stu-id="ecaf2-103">IContextLink::GetDestinationNode method</span></span>

<span data-ttu-id="ecaf2-104">Recupera l'oggetto [**IContextNode**](icontextnode.md) che rappresenta la destinazione per questo [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf2-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecaf2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecaf2-105">Syntax</span></span>


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="ecaf2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecaf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecaf2-107">*ppDstContextNodeId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ecaf2-107">*ppDstContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecaf2-108">Puntatore all'oggetto [**IContextNode**](icontextnode.md) che rappresenta la destinazione per questo [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf2-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecaf2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecaf2-109">Return value</span></span>

<span data-ttu-id="ecaf2-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf2-110">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ecaf2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecaf2-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ecaf2-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppDstContextNodeId* quando non è più necessario usare il nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecaf2-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppDstContextNodeId* when you no longer need to use the destination node.</span></span>

 

<span data-ttu-id="ecaf2-113">Se l'oggetto [**IContextLink**](icontextlink.md) è collegato tra un nodo che contiene la scrittura e un nodo che contiene il disegno, il nodo di destinazione è in genere il nodo che contiene la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ecaf2-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the destination node is generally the node that contains writing.</span></span>

<span data-ttu-id="ecaf2-114">Se l'oggetto [**IContextLink**](icontextlink.md) dispone di un tipo di collegamento di racchiude (vedere [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), il nodo di destinazione è l'oggetto [**IContextNode**](icontextnode.md) che è incluso.</span><span class="sxs-lookup"><span data-stu-id="ecaf2-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the destination node is the [**IContextNode**](icontextnode.md) object that is enclosed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecaf2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecaf2-115">Requirements</span></span>



| <span data-ttu-id="ecaf2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecaf2-116">Requirement</span></span> | <span data-ttu-id="ecaf2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ecaf2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecaf2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecaf2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ecaf2-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ecaf2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ecaf2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecaf2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ecaf2-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ecaf2-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ecaf2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecaf2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecaf2-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ecaf2-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ecaf2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ecaf2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecaf2-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecaf2-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ecaf2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecaf2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecaf2-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="ecaf2-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="ecaf2-128">**IContextLink::GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="ecaf2-128">**IContextLink::GetSourceNode**</span></span>](icontextlink-getsourcenode.md)
</dt> <dt>

[<span data-ttu-id="ecaf2-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="ecaf2-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="ecaf2-130">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ecaf2-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

