---
description: Aggiorna i dati dei pacchetti per i tratti specificati.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Metodo IInkAnalyzer:: UpdateStrokesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307369"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a><span data-ttu-id="df382-103">Metodo IInkAnalyzer:: UpdateStrokesData</span><span class="sxs-lookup"><span data-stu-id="df382-103">IInkAnalyzer::UpdateStrokesData method</span></span>

<span data-ttu-id="df382-104">Aggiorna i dati dei pacchetti per i tratti specificati.</span><span class="sxs-lookup"><span data-stu-id="df382-104">Updates the packet data for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="df382-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df382-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="df382-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df382-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df382-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df382-108">Numero di tratti da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="df382-108">The number of strokes to update.</span></span>

</dd> <dt>

<span data-ttu-id="df382-109">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df382-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df382-110">Matrice contenente gli identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="df382-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="df382-111">*ulStrokePacketDescriptionCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df382-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df382-112">Numero di proprietà in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="df382-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="df382-113">*pStrokePacketDescriptionGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df382-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df382-114">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="df382-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="df382-115">*pulPacketDataCountPerStroke* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df382-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df382-116">Matrice contenente il numero di pacchetti in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="df382-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="df382-117">*plStrokePacketData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df382-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df382-118">Matrice contenente i dati dei pacchetti per i tratti.</span><span class="sxs-lookup"><span data-stu-id="df382-118">An array containing the packet data for the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df382-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df382-119">Return value</span></span>

<span data-ttu-id="df382-120">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="df382-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df382-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="df382-121">Remarks</span></span>

<span data-ttu-id="df382-122">il parametro *plStrokePacketData* contiene i dati dei pacchetti per tutti i tratti.</span><span class="sxs-lookup"><span data-stu-id="df382-122">the *plStrokePacketData* parameter contains packet data for all of the strokes.</span></span> <span data-ttu-id="df382-123">Il parametro *pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="df382-123">The *pStrokePacketDescriptionGuids* parameter contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="df382-124">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="df382-124">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="df382-125">Solo i tratti con le stesse descrizioni di pacchetti possono essere aggiornati in una singola chiamata al **Metodo IInkAnalyzer:: UpdateStrokesData**.</span><span class="sxs-lookup"><span data-stu-id="df382-125">Only strokes with the same packet descriptions can be updated in a single call to **IInkAnalyzer::UpdateStrokesData Method**.</span></span>

<span data-ttu-id="df382-126">Questo metodo non aggiorna l'area dirty dell'analizzatore di input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="df382-126">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="df382-127">Se un tratto specificato non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="df382-127">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="df382-128">Se nessuno dei tratti specificati identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="df382-128">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="df382-129">Questo metodo restituisce un codice di errore quando *plStrokeIds* è **null**.</span><span class="sxs-lookup"><span data-stu-id="df382-129">This method returns an error code when *plStrokeIds* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="df382-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df382-130">Requirements</span></span>



| <span data-ttu-id="df382-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="df382-131">Requirement</span></span> | <span data-ttu-id="df382-132">Valore</span><span class="sxs-lookup"><span data-stu-id="df382-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df382-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df382-133">Minimum supported client</span></span><br/> | <span data-ttu-id="df382-134">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="df382-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="df382-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df382-135">Minimum supported server</span></span><br/> | <span data-ttu-id="df382-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="df382-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="df382-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df382-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="df382-138"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="df382-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="df382-139">DLL</span><span class="sxs-lookup"><span data-stu-id="df382-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df382-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df382-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="df382-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df382-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df382-142">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="df382-142">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="df382-143">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="df382-143">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="df382-144">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="df382-144">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="df382-145">**Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="df382-145">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="df382-146">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="df382-146">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="df382-147">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="df382-147">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="df382-148">**Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="df382-148">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="df382-149">**Metodo IInkAnalyzer:: ClearStrokeData**</span><span class="sxs-lookup"><span data-stu-id="df382-149">**IInkAnalyzer::ClearStrokeData Method**</span></span>](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[<span data-ttu-id="df382-150">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="df382-150">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="df382-151">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="df382-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




