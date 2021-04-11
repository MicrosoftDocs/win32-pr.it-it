---
description: Crea un nuovo nodo di riconoscimento personalizzato per IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'Metodo IInkAnalyzer:: CreateCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226159"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a><span data-ttu-id="4f16a-103">Metodo IInkAnalyzer:: CreateCustomRecognizer</span><span class="sxs-lookup"><span data-stu-id="4f16a-103">IInkAnalyzer::CreateCustomRecognizer method</span></span>

<span data-ttu-id="4f16a-104">Crea un nuovo nodo di riconoscimento personalizzato per [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="4f16a-104">Creates a new custom recognizer node for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f16a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f16a-105">Syntax</span></span>


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="4f16a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f16a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f16a-107">*pInkAnalysisRecognizerId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f16a-107">*pInkAnalysisRecognizerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f16a-108">Identificatore univoco globale (GUID) dell'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) per il quale creare un nodo.</span><span class="sxs-lookup"><span data-stu-id="4f16a-108">The globally unique identifier (GUID) of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) for which to create a node.</span></span>

</dd> <dt>

<span data-ttu-id="4f16a-109">*ppContextNode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f16a-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f16a-110">Puntatore all'oggetto [**IContextNode**](icontextnode.md) che rappresenta il nuovo nodo di riconoscimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4f16a-110">A pointer to the [**IContextNode**](icontextnode.md) object representing the new custom recognizer node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f16a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f16a-111">Return value</span></span>

<span data-ttu-id="4f16a-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4f16a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f16a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f16a-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4f16a-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su ppContextNode quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4f16a-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on ppContextNode when you no longer need to use the object.</span></span>

 

<span data-ttu-id="4f16a-115">Questo metodo crea un nuovo [**IContextNode**](icontextnode.md) con un tipo di CustomRecognizer (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="4f16a-115">This method creates a new [**IContextNode**](icontextnode.md) with a type of CustomRecognizer (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="4f16a-116">Aggiunge quindi il nuovo nodo di riconoscimento personalizzato alla raccolta dei sottonodi del nodo radice dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il metodo [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="4f16a-116">It then adds the new custom recognizer node to the subnodes collection of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f16a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f16a-117">Requirements</span></span>



| <span data-ttu-id="4f16a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f16a-118">Requirement</span></span> | <span data-ttu-id="4f16a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4f16a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f16a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f16a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4f16a-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4f16a-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f16a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f16a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4f16a-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f16a-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4f16a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f16a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f16a-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4f16a-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4f16a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4f16a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f16a-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f16a-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4f16a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f16a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f16a-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4f16a-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4f16a-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4f16a-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4f16a-131">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="4f16a-131">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="4f16a-132">**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**</span><span class="sxs-lookup"><span data-stu-id="4f16a-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="4f16a-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4f16a-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

