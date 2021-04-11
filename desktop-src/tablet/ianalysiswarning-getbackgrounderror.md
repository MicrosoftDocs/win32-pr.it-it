---
description: Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Metodo IAnalysisWarning:: GetBackgroundError (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226171"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a><span data-ttu-id="046e0-103">Metodo IAnalysisWarning:: GetBackgroundError</span><span class="sxs-lookup"><span data-stu-id="046e0-103">IAnalysisWarning::GetBackgroundError method</span></span>

<span data-ttu-id="046e0-104">Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="046e0-104">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="046e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="046e0-105">Syntax</span></span>


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a><span data-ttu-id="046e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="046e0-106">Parameters</span></span>

<span data-ttu-id="046e0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="046e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="046e0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="046e0-108">Return value</span></span>

<span data-ttu-id="046e0-109">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="046e0-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="046e0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="046e0-110">Remarks</span></span>

<span data-ttu-id="046e0-111">Se si verifica un errore all'interno di un'operazione di analisi in background, [**IInkAnalyzer**](iinkanalyzer.md) non può restituire il codice di errore perché si sta verificando in un thread diverso.</span><span class="sxs-lookup"><span data-stu-id="046e0-111">If an error occurs within a background analysis operation, the [**IInkAnalyzer**](iinkanalyzer.md) cannot return the error code because it is occurring in a different thread.</span></span> <span data-ttu-id="046e0-112">Al contrario, il gestore dell'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) riceve un [**IAnalysisStatus**](ianalysisstatus.md) contenente un [**IAnalysisWarning**](ianalysiswarning.md) con [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ BackgroundException**.</span><span class="sxs-lookup"><span data-stu-id="046e0-112">Instead, the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event handler receives an [**IAnalysisStatus**](ianalysisstatus.md) that contains an [**IAnalysisWarning**](ianalysiswarning.md) with an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) of **AnalysisWarningCode\_BackgroundException**.</span></span> <span data-ttu-id="046e0-113">Questo **IAnalysisWarning** contiene il codice di errore per l'operazione di analisi in background.</span><span class="sxs-lookup"><span data-stu-id="046e0-113">This **IAnalysisWarning** contains the error code for the background analysis operation.</span></span> <span data-ttu-id="046e0-114">In generale, il gestore dell'evento **\_ IAnalysisEvents:: results** restituirà questo codice di errore in modo che possa essere gestito altrove nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="046e0-114">In general, your **\_IAnalysisEvents::Results** event handler will return this error code so that it can be handled elsewhere in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="046e0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="046e0-115">Requirements</span></span>



| <span data-ttu-id="046e0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="046e0-116">Requirement</span></span> | <span data-ttu-id="046e0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="046e0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="046e0-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="046e0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="046e0-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="046e0-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="046e0-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="046e0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="046e0-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="046e0-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="046e0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="046e0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="046e0-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="046e0-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="046e0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="046e0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="046e0-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="046e0-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="046e0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="046e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046e0-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="046e0-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="046e0-128">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="046e0-128">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="046e0-129">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="046e0-129">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="046e0-130">**\_IAnalysisEvents:: results**</span><span class="sxs-lookup"><span data-stu-id="046e0-130">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="046e0-131">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="046e0-131">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="046e0-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="046e0-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

