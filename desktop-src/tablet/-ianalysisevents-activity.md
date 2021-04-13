---
description: 'Si verifica quando viene chiamato il metodo IInkAnalyzer:: Analyze o IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: 'Evento _IAnalysisEvents:: Activity (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351816"
---
# <a name="_ianalysiseventsactivity-event"></a><span data-ttu-id="5cfef-103">\_Evento IAnalysisEvents:: Activity</span><span class="sxs-lookup"><span data-stu-id="5cfef-103">\_IAnalysisEvents::Activity event</span></span>

<span data-ttu-id="5cfef-104">Si verifica quando viene chiamato il metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="5cfef-104">Occurs when the [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) method or [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cfef-105">Syntax</span></span>


```C++
HRESULT Activity();
```



## <a name="parameters"></a><span data-ttu-id="5cfef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cfef-106">Parameters</span></span>

<span data-ttu-id="5cfef-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="5cfef-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5cfef-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cfef-108">Return value</span></span>

<span data-ttu-id="5cfef-109">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5cfef-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cfef-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cfef-110">Remarks</span></span>

<span data-ttu-id="5cfef-111">Questo evento indica che [**IInkAnalyzer**](iinkanalyzer.md) sta eseguendo l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="5cfef-111">This event indicates that the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span> <span data-ttu-id="5cfef-112">Questo evento non indica lo stato di avanzamento dell'operazione di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="5cfef-112">This event does not indicate the progress of the ink analysis operation.</span></span>

<span data-ttu-id="5cfef-113">Per eseguire una delle operazioni seguenti, implementare un gestore eventi **\_ IAnalysisEvents:: Activity** :</span><span class="sxs-lookup"><span data-stu-id="5cfef-113">To do any of the following, implement an **\_IAnalysisEvents::Activity** event handler:</span></span>

-   <span data-ttu-id="5cfef-114">Indica all'utente che l'analizzatore di input penna sta eseguendo l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="5cfef-114">Indicate to the user that the ink analyzer is performing ink analysis.</span></span>
-   <span data-ttu-id="5cfef-115">Elaborare l'input dell'utente durante l'analisi sincrona.</span><span class="sxs-lookup"><span data-stu-id="5cfef-115">Process user input during synchronous analysis.</span></span>
-   <span data-ttu-id="5cfef-116">Ricevere una notifica delle richieste di sistema, ad esempio il ridisegno della finestra dell'applicazione, durante l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="5cfef-116">Receive notification of system requests, such as repainting of the application's window, during ink analysis.</span></span>

<span data-ttu-id="5cfef-117">[**IInkAnalyzer**](iinkanalyzer.md) genera spesso questo evento durante la fase di analisi del layout e la fase di classificazione di scrittura e disegno dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="5cfef-117">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event frequently during the layout analysis phase and the writing and drawing classification phase of ink analysis.</span></span> <span data-ttu-id="5cfef-118">**IInkAnalyzer** genera questo evento durante la fase di riconoscimento della grafia prima e dopo l'accesso a un riconoscimento input penna.</span><span class="sxs-lookup"><span data-stu-id="5cfef-118">The **IInkAnalyzer** raises this event during the handwriting recognition phase before and after accessing an ink recognizer.</span></span>

<span data-ttu-id="5cfef-119">Il numero di eventi di attività generati da un [**IInkAnalyzer**](iinkanalyzer.md) è influenzato da:</span><span class="sxs-lookup"><span data-stu-id="5cfef-119">The number of activity events an [**IInkAnalyzer**](iinkanalyzer.md) generates is affected by:</span></span>

-   <span data-ttu-id="5cfef-120">Riconoscimento dell'input penna applicato da [**IInkAnalyzer**](iinkanalyzer.md) al riconoscimento dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="5cfef-120">The ink recognizer that the [**IInkAnalyzer**](iinkanalyzer.md) applies to ink recognition.</span></span>
-   <span data-ttu-id="5cfef-121">Il numero e la lunghezza dei tratti analizzati da [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="5cfef-121">The number and length of strokes that the [**IInkAnalyzer**](iinkanalyzer.md) is analyzing.</span></span>
-   <span data-ttu-id="5cfef-122">Numero di tratti classificati come scritti.</span><span class="sxs-lookup"><span data-stu-id="5cfef-122">The number of strokes that are classified as writing.</span></span>

<span data-ttu-id="5cfef-123">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5cfef-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cfef-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cfef-124">Requirements</span></span>



| <span data-ttu-id="5cfef-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cfef-125">Requirement</span></span> | <span data-ttu-id="5cfef-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5cfef-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfef-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cfef-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5cfef-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5cfef-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5cfef-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cfef-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5cfef-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5cfef-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5cfef-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cfef-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cfef-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5cfef-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5cfef-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5cfef-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cfef-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cfef-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5cfef-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cfef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfef-136">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="5cfef-136">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="5cfef-137">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="5cfef-137">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="5cfef-138">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5cfef-138">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5cfef-139">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="5cfef-139">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="5cfef-140">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="5cfef-140">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="5cfef-141">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="5cfef-141">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5cfef-142">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="5cfef-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




