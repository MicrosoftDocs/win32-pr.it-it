---
description: Crea un oggetto IContextNodes.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'Metodo IInkAnalyzer:: CreateContextNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307394"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a><span data-ttu-id="0ec8c-103">Metodo IInkAnalyzer:: CreateContextNodes</span><span class="sxs-lookup"><span data-stu-id="0ec8c-103">IInkAnalyzer::CreateContextNodes method</span></span>

<span data-ttu-id="0ec8c-104">Crea un oggetto [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec8c-104">Creates an [**IContextNodes**](icontextnodes.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec8c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ec8c-105">Syntax</span></span>


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="0ec8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ec8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ec8c-107">*ppContextNodes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0ec8c-107">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec8c-108">Puntatore all'oggetto [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec8c-108">A pointer to the [**IContextNodes**](icontextnodes.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ec8c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ec8c-109">Return value</span></span>

<span data-ttu-id="0ec8c-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0ec8c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ec8c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ec8c-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0ec8c-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodes* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodes* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="0ec8c-113">Utilizzare questo metodo per creare una raccolta [**IContextNodes**](icontextnodes.md) vuota associata a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="0ec8c-113">Use this method to create an empty [**IContextNodes**](icontextnodes.md) collection that is associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="0ec8c-114">La nuova raccolta **IContextNodes** non fa parte dell'albero del contesto dell'oggetto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="0ec8c-114">The new **IContextNodes** collection is not part of the **IInkAnalyzer** object's context tree.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec8c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ec8c-115">Requirements</span></span>



| <span data-ttu-id="0ec8c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ec8c-116">Requirement</span></span> | <span data-ttu-id="0ec8c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0ec8c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec8c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ec8c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec8c-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0ec8c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0ec8c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ec8c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec8c-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0ec8c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0ec8c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ec8c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ec8c-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0ec8c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0ec8c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0ec8c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ec8c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ec8c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0ec8c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ec8c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec8c-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="0ec8c-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0ec8c-128">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="0ec8c-128">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="0ec8c-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="0ec8c-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

