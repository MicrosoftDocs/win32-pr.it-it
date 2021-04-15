---
description: Recupera l'area del documento che corrisponde alle modifiche apportate nell'albero del nodo di contesto dell'oggetto IInkAnalyzer come risultato dell'analisi dell'input penna.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Metodo IAnalysisStatus:: GetAppliedChangesRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526545"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a><span data-ttu-id="cb58c-103">Metodo IAnalysisStatus:: GetAppliedChangesRegion</span><span class="sxs-lookup"><span data-stu-id="cb58c-103">IAnalysisStatus::GetAppliedChangesRegion method</span></span>

<span data-ttu-id="cb58c-104">Recupera l'area del documento che corrisponde alle modifiche apportate nell'albero del nodo di contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) come risultato dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="cb58c-104">Retrieves the region of the document that corresponds to changes that were made in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree as a result of ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb58c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb58c-105">Syntax</span></span>


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a><span data-ttu-id="cb58c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb58c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb58c-107">*pAppliedChangesRegion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb58c-107">*pAppliedChangesRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb58c-108">Puntatore al [**IAnalysisRegion**](ianalysisregion.md) del documento in cui sono state apportate modifiche.</span><span class="sxs-lookup"><span data-stu-id="cb58c-108">A pointer to the [**IAnalysisRegion**](ianalysisregion.md) of the document where changes were made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb58c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb58c-109">Return value</span></span>

<span data-ttu-id="cb58c-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cb58c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb58c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb58c-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cb58c-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pAppliedChangesRegion* quando non è più necessario usare l'area di analisi.</span><span class="sxs-lookup"><span data-stu-id="cb58c-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAppliedChangesRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="cb58c-113">Questo metodo viene usato più di frequente quando l'applicazione riceve informazioni a scopo di debug e deve invalidare l'area in cui potrebbero verificarsi le modifiche in modo da disegnare le informazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="cb58c-113">This method is most frequently used when the application receives information for debugging purposes and needs to invalidate the area where changes might occur so that the debugging information is painted.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb58c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb58c-114">Requirements</span></span>



| <span data-ttu-id="cb58c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb58c-115">Requirement</span></span> | <span data-ttu-id="cb58c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cb58c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb58c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb58c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb58c-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cb58c-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cb58c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb58c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb58c-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cb58c-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cb58c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb58c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb58c-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cb58c-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb58c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cb58c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb58c-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb58c-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cb58c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb58c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb58c-126">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="cb58c-126">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="cb58c-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="cb58c-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="cb58c-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="cb58c-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

