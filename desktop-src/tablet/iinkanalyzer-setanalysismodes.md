---
description: Modifica i flag che controllano il modo in cui IInkAnalyzer esegue l'analisi dell'input penna.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'Metodo IInkAnalyzer:: SetAnalysisModes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 826d31fd5b61db2332ef953d55b2cf6c6331995b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526478"
---
# <a name="iinkanalyzersetanalysismodes-method"></a><span data-ttu-id="e15ac-103">Metodo IInkAnalyzer:: SetAnalysisModes</span><span class="sxs-lookup"><span data-stu-id="e15ac-103">IInkAnalyzer::SetAnalysisModes method</span></span>

<span data-ttu-id="e15ac-104">Modifica i flag che controllano il modo in cui [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="e15ac-104">Modifies flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e15ac-105">Syntax</span></span>


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="e15ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e15ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e15ac-107">*analysisMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e15ac-107">*analysisMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e15ac-108">Combinazione bit per bit dei valori dell'enumerazione [**AnalysisModes**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="e15ac-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e15ac-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e15ac-109">Return value</span></span>

<span data-ttu-id="e15ac-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e15ac-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e15ac-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e15ac-111">Requirements</span></span>



| <span data-ttu-id="e15ac-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e15ac-112">Requirement</span></span> | <span data-ttu-id="e15ac-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e15ac-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e15ac-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e15ac-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e15ac-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e15ac-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e15ac-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e15ac-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e15ac-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e15ac-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e15ac-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e15ac-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e15ac-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e15ac-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e15ac-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e15ac-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e15ac-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e15ac-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e15ac-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e15ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e15ac-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e15ac-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e15ac-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="e15ac-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="e15ac-125">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="e15ac-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="e15ac-126">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="e15ac-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="e15ac-127">**Metodo IInkAnalyzer:: GetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="e15ac-127">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="e15ac-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="e15ac-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




