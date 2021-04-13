---
description: Specifica il modo in cui IInkAnalyzer esegue l'analisi dell'input penna.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Enumerazione AnalysisModes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401518"
---
# <a name="analysismodes-enumeration"></a><span data-ttu-id="23192-103">Enumerazione AnalysisModes</span><span class="sxs-lookup"><span data-stu-id="23192-103">AnalysisModes enumeration</span></span>

<span data-ttu-id="23192-104">Specifica il modo in cui [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="23192-104">Specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="23192-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23192-105">Syntax</span></span>


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a><span data-ttu-id="23192-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="23192-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23192-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ None**</span><span class="sxs-lookup"><span data-stu-id="23192-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes\_None**</span></span>
</dt> <dd>

<span data-ttu-id="23192-108">Non è stata specificata alcuna modalità.</span><span class="sxs-lookup"><span data-stu-id="23192-108">No modes are specified.</span></span>

</dd> <dt>

<span data-ttu-id="23192-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**\_AutomaticReconciliation AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="23192-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes\_AutomaticReconciliation**</span></span>
</dt> <dd>

<span data-ttu-id="23192-110">Indica se il [**IInkAnalyzer**](iinkanalyzer.md) avvia automaticamente l'operazione di riconciliazione non appena i risultati intermedi o finali sono pronti.</span><span class="sxs-lookup"><span data-stu-id="23192-110">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically starts the reconciliation operation as soon as the intermediate or final results are ready.</span></span>

<span data-ttu-id="23192-111">Se questa modalità è abilitata, l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) non viene generato.</span><span class="sxs-lookup"><span data-stu-id="23192-111">If this mode is enabled, the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event is not raised.</span></span> <span data-ttu-id="23192-112">Se questa modalità è disabilitata, viene generato l'evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="23192-112">If this mode is disabled, the **\_IAnalysisEvents::ReadyToReconcile** event is raised.</span></span>

</dd> <dt>

<span data-ttu-id="23192-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**\_StrokeCacheAutoCleanup AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="23192-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes\_StrokeCacheAutoCleanup**</span></span>
</dt> <dd>

<span data-ttu-id="23192-114">Indica se [**IInkAnalyzer**](iinkanalyzer.md) cancella automaticamente i tratti non necessari dalla cache del tratto prima di eseguire l'analisi.</span><span class="sxs-lookup"><span data-stu-id="23192-114">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically clears unneeded strokes from the stroke cache before performing analysis.</span></span>

<span data-ttu-id="23192-115">Se questa modalità è abilitata, [**IInkAnalyzer**](iinkanalyzer.md) Cancella i dati del tratto prima di eseguire l'analisi.</span><span class="sxs-lookup"><span data-stu-id="23192-115">If this mode is enabled, the [**IInkAnalyzer**](iinkanalyzer.md) clears the stroke data before performing analysis.</span></span> <span data-ttu-id="23192-116">Il codice deve anche gestire l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="23192-116">Your code must also then handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span> <span data-ttu-id="23192-117">Se l'evento **\_ IAnalysisEvents:: UpdateStrokesCache** non è gestito, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="23192-117">If the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span> <span data-ttu-id="23192-118">Questa verifica viene eseguita sia in fase di analisi (o BackgroundAnalyze) che in fase di riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="23192-118">This check is done both at the Analyze (or BackgroundAnalyze) and Reconciliation phases.</span></span>

<span data-ttu-id="23192-119">Se questa modalità è disabilitata, [**IInkAnalyzer**](iinkanalyzer.md) non cancella i dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="23192-119">If this mode is disabled, the [**IInkAnalyzer**](iinkanalyzer.md) does not clear the stroke data.</span></span> <span data-ttu-id="23192-120">Per cancellare i dati del tratto, chiamare il [**Metodo IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md).</span><span class="sxs-lookup"><span data-stu-id="23192-120">To clear the stroke data, call [**IInkAnalyzer::ClearStrokeData Method**](iinkanalyzer-clearstrokedata.md).</span></span> <span data-ttu-id="23192-121">Se questa modalità è disabilitata, viene generato l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) in modo che **IInkAnalyzer** possa recuperare i dati del tratto più recenti per tutti i tratti per i quali la cache è stata cancellata.</span><span class="sxs-lookup"><span data-stu-id="23192-121">If this mode is disabled, the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event is raised so the **IInkAnalyzer** can retrieve the latest stroke data for any strokes that have had their cache cleared.</span></span> <span data-ttu-id="23192-122">Se la cache del tratto viene deselezionata, ma l'evento **\_ IAnalysisEvents:: UpdateStrokesCache** non viene gestito, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="23192-122">If the stroke cache is cleared, but the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span>

</dd> <dt>

<span data-ttu-id="23192-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**\_PersonalizationEnabled AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="23192-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes\_PersonalizationEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="23192-124">Personalizzazione del riconoscimento della grafia abilitata.</span><span class="sxs-lookup"><span data-stu-id="23192-124">Personalization of handwriting recognition is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="23192-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**\_Impostazione predefinita AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="23192-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="23192-126">Tutte le modalità sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="23192-126">All modes are enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23192-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="23192-127">Remarks</span></span>

<span data-ttu-id="23192-128">Questa enumerazione consente una combinazione bit per bit dei relativi valori dei membri.</span><span class="sxs-lookup"><span data-stu-id="23192-128">This enumeration allows a bitwise combination of its member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="23192-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23192-129">Requirements</span></span>



| <span data-ttu-id="23192-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="23192-130">Requirement</span></span> | <span data-ttu-id="23192-131">Valore</span><span class="sxs-lookup"><span data-stu-id="23192-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23192-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23192-132">Minimum supported client</span></span><br/> | <span data-ttu-id="23192-133">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="23192-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="23192-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23192-134">Minimum supported server</span></span><br/> | <span data-ttu-id="23192-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="23192-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="23192-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23192-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="23192-137"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="23192-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23192-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23192-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23192-139">**Metodo IInkAnalyzer:: GetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="23192-139">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="23192-140">**Metodo IInkAnalyzer:: SetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="23192-140">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="23192-141">**\_IAnalysisEvents:: IntermediateResults ()**</span><span class="sxs-lookup"><span data-stu-id="23192-141">**\_IAnalysisEvents::IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[<span data-ttu-id="23192-142">**\_IAnalysisEvents:: ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="23192-142">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="23192-143">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="23192-143">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="23192-144">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="23192-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




