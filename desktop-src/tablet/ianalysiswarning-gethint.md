---
description: Recupera l'hint di analisi che ha generato l'avviso.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Metodo IAnalysisWarning:: GetHint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307455"
---
# <a name="ianalysiswarninggethint-method"></a><span data-ttu-id="bfe38-103">Metodo IAnalysisWarning:: GetHint</span><span class="sxs-lookup"><span data-stu-id="bfe38-103">IAnalysisWarning::GetHint method</span></span>

<span data-ttu-id="bfe38-104">Recupera l'hint di analisi che ha generato l'avviso.</span><span class="sxs-lookup"><span data-stu-id="bfe38-104">Retrieves the analysis hint that caused this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfe38-105">Syntax</span></span>


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="bfe38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfe38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe38-107">*pAnalysisHint* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bfe38-107">*pAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfe38-108">Nodo di contesto dell'hint di analisi che ha causato questo avviso o **null** se un hint di analisi non ha causato questo avviso.</span><span class="sxs-lookup"><span data-stu-id="bfe38-108">The analysis hint context node that caused this warning, or **NULL** if an analysis hint did not cause this warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe38-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfe38-109">Return value</span></span>

<span data-ttu-id="bfe38-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bfe38-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bfe38-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfe38-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="bfe38-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pAnalysisHint* quando non è più necessario usare il nodo di contesto dell'hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="bfe38-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAnalysisHint* when you no longer need to use the analysis hint context node.</span></span>

 

<span data-ttu-id="bfe38-113">Un esempio di hint di analisi che genera un [**IAnalysisWarning**](ianalysiswarning.md) è un hint di analisi che contiene un controllo del controllo ortografico digitato in modo errato.</span><span class="sxs-lookup"><span data-stu-id="bfe38-113">An example of an analysis hint that generates an [**IAnalysisWarning**](ianalysiswarning.md) is an analysis hint that contains an incorrectly spelled factoid.</span></span> <span data-ttu-id="bfe38-114">In questo caso, l'analisi dell'input penna restituisce un [**IAnalysisStatus**](ianalysisstatus.md) contenente un **IAnalysisWarning** che fa riferimento al nodo di contesto dell'hint di analisi con il controllo ortografico errato.</span><span class="sxs-lookup"><span data-stu-id="bfe38-114">In this case, ink analysis returns an [**IAnalysisStatus**](ianalysisstatus.md) that contains an **IAnalysisWarning** that references the analysis hint context node with the misspelled factoid.</span></span> <span data-ttu-id="bfe38-115">Inoltre, in questo caso, il metodo [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md) dell'avviso di analisi restituisce un valore [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ FactoidNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="bfe38-115">Also, in this case, the analysis warning's [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) method returns an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_FactoidNotSupported**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe38-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfe38-116">Requirements</span></span>



| <span data-ttu-id="bfe38-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe38-117">Requirement</span></span> | <span data-ttu-id="bfe38-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bfe38-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe38-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfe38-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe38-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bfe38-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bfe38-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfe38-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe38-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bfe38-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bfe38-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfe38-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe38-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bfe38-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bfe38-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bfe38-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfe38-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfe38-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bfe38-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfe38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe38-128">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="bfe38-128">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="bfe38-129">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="bfe38-129">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="bfe38-130">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="bfe38-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="bfe38-131">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="bfe38-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="bfe38-132">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="bfe38-132">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="bfe38-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="bfe38-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

