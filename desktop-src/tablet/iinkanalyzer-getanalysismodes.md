---
description: Recupera i flag che controllano il modo in cui IInkAnalyzer esegue l'analisi dell'input penna.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'Metodo IInkAnalyzer:: GetAnalysisModes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307385"
---
# <a name="iinkanalyzergetanalysismodes-method"></a><span data-ttu-id="cbfe6-103">Metodo IInkAnalyzer:: GetAnalysisModes</span><span class="sxs-lookup"><span data-stu-id="cbfe6-103">IInkAnalyzer::GetAnalysisModes method</span></span>

<span data-ttu-id="cbfe6-104">Recupera i flag che controllano il modo in cui [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="cbfe6-104">Retrieves flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfe6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbfe6-105">Syntax</span></span>


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="cbfe6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbfe6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbfe6-107">*pAnalysisMode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cbfe6-107">*pAnalysisMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbfe6-108">Combinazione bit per bit dei valori dell'enumerazione [**AnalysisModes**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfe6-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbfe6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbfe6-109">Return value</span></span>

<span data-ttu-id="cbfe6-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cbfe6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfe6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbfe6-111">Requirements</span></span>



| <span data-ttu-id="cbfe6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbfe6-112">Requirement</span></span> | <span data-ttu-id="cbfe6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cbfe6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfe6-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbfe6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cbfe6-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cbfe6-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cbfe6-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbfe6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cbfe6-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cbfe6-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cbfe6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbfe6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbfe6-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cbfe6-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cbfe6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cbfe6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbfe6-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbfe6-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cbfe6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbfe6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfe6-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="cbfe6-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cbfe6-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="cbfe6-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="cbfe6-125">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="cbfe6-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="cbfe6-126">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="cbfe6-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="cbfe6-127">**Metodo IInkAnalyzer:: SetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="cbfe6-127">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="cbfe6-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="cbfe6-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




