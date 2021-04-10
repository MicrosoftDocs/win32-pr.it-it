---
description: Salva tutti i risultati dell'analisi per un IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'Metodo IInkAnalyzer:: SaveResults (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343681"
---
# <a name="iinkanalyzersaveresults-method"></a><span data-ttu-id="9aa65-103">Metodo IInkAnalyzer:: SaveResults</span><span class="sxs-lookup"><span data-stu-id="9aa65-103">IInkAnalyzer::SaveResults method</span></span>

<span data-ttu-id="9aa65-104">Salva tutti i risultati dell'analisi per un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9aa65-104">Saves all analysis results for an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa65-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9aa65-105">Syntax</span></span>


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="9aa65-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9aa65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa65-107">*pulSerializedDataSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9aa65-107">*pulSerializedDataSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa65-108">Numero di byte in *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="9aa65-108">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="9aa65-109">*ppbSerializedData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9aa65-109">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa65-110">Matrice contenente i risultati dell'analisi salvata.</span><span class="sxs-lookup"><span data-stu-id="9aa65-110">An array containing the saved analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa65-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9aa65-111">Return value</span></span>

<span data-ttu-id="9aa65-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9aa65-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa65-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9aa65-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9aa65-114">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbSerializedData* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="9aa65-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="9aa65-115">Questo metodo consente di salvare tutti i risultati di analisi correnti, che includono l'hint di analisi corrente e i nodi di riconoscimento personalizzati (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="9aa65-115">This method saves all the current analysis results, which include current analysis hint and custom recognizer nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="9aa65-116">Questo metodo non salva i dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="9aa65-116">This method does not save any stroke data.</span></span> <span data-ttu-id="9aa65-117">È responsabilità dell'applicazione sincronizzare eventuali risultati di analisi e tratti corrispondenti se rende permanente i dati.</span><span class="sxs-lookup"><span data-stu-id="9aa65-117">It is the responsibility of your application to synchronize any analysis results and corresponding strokes if it persists data.</span></span>

<span data-ttu-id="9aa65-118">Questo metodo restituisce un codice di errore quando un oggetto [**IContextNode**](icontextnode.md) da salvare è parzialmente popolato (vedere [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="9aa65-118">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa65-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9aa65-119">Requirements</span></span>



| <span data-ttu-id="9aa65-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa65-120">Requirement</span></span> | <span data-ttu-id="9aa65-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9aa65-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa65-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9aa65-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa65-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9aa65-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9aa65-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9aa65-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa65-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9aa65-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9aa65-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9aa65-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aa65-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9aa65-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9aa65-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9aa65-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aa65-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aa65-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9aa65-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9aa65-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa65-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9aa65-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9aa65-132">**Metodo IInkAnalyzer:: LoadResults**</span><span class="sxs-lookup"><span data-stu-id="9aa65-132">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="9aa65-133">**Metodo IInkAnalyzer:: SaveResultsForNodes**</span><span class="sxs-lookup"><span data-stu-id="9aa65-133">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="9aa65-134">**Metodo IInkAnalyzer:: SaveResultsForStrokes**</span><span class="sxs-lookup"><span data-stu-id="9aa65-134">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="9aa65-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9aa65-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9aa65-136">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="9aa65-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

