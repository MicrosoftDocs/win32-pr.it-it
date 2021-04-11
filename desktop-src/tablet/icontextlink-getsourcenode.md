---
description: Recupera l'oggetto IContextNode che rappresenta l'origine per questo IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'Metodo IContextLink:: GetSourceNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226166"
---
# <a name="icontextlinkgetsourcenode-method"></a><span data-ttu-id="bda5d-103">Metodo IContextLink:: GetSourceNode</span><span class="sxs-lookup"><span data-stu-id="bda5d-103">IContextLink::GetSourceNode method</span></span>

<span data-ttu-id="bda5d-104">Recupera l'oggetto [**IContextNode**](icontextnode.md) che rappresenta l'origine per questo [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="bda5d-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bda5d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bda5d-105">Syntax</span></span>


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="bda5d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bda5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda5d-107">*ppSrcContextNodeId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bda5d-107">*ppSrcContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bda5d-108">Puntatore all'oggetto [**IContextNode**](icontextnode.md) che rappresenta l'origine per questo [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="bda5d-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda5d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bda5d-109">Return value</span></span>

<span data-ttu-id="bda5d-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bda5d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bda5d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bda5d-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="bda5d-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppSrcContextNodeId* quando non è più necessario usare il nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="bda5d-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSrcContextNodeId* when you no longer need to use the source node.</span></span>

 

<span data-ttu-id="bda5d-113">Se l'oggetto [**IContextLink**](icontextlink.md) è collegato tra un nodo che contiene la scrittura e un nodo che contiene il disegno, il nodo di origine è in genere il nodo che contiene il disegno.</span><span class="sxs-lookup"><span data-stu-id="bda5d-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the source node is generally the node that contains drawing.</span></span>

<span data-ttu-id="bda5d-114">Se l'oggetto [**IContextLink**](icontextlink.md) dispone di un tipo di collegamento di racchiude (vedere [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), il nodo di origine è il nodo che racchiude il nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bda5d-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the source node is the node that encloses the destination node.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda5d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda5d-115">Requirements</span></span>



| <span data-ttu-id="bda5d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda5d-116">Requirement</span></span> | <span data-ttu-id="bda5d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bda5d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda5d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda5d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bda5d-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bda5d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bda5d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda5d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bda5d-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bda5d-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bda5d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bda5d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda5d-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bda5d-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bda5d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bda5d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bda5d-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bda5d-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bda5d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bda5d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda5d-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="bda5d-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="bda5d-128">**IContextLink::GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="bda5d-128">**IContextLink::GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)
</dt> <dt>

[<span data-ttu-id="bda5d-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="bda5d-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="bda5d-130">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="bda5d-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

