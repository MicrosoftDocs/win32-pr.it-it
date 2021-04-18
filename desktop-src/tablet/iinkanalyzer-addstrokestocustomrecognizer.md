---
description: Aggiunge dati Stroke per più tratti a un nodo di riconoscimento personalizzato.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307398"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a><span data-ttu-id="9e57f-103">Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer</span><span class="sxs-lookup"><span data-stu-id="9e57f-103">IInkAnalyzer::AddStrokesToCustomRecognizer method</span></span>

<span data-ttu-id="9e57f-104">Aggiunge dati Stroke per più tratti a un nodo di riconoscimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9e57f-104">Adds stroke data for multiple strokes to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e57f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e57f-105">Syntax</span></span>


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="9e57f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e57f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e57f-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-108">Numero di tratti da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9e57f-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="9e57f-109">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-110">Matrice contenente gli identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="9e57f-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9e57f-111">*ulStrokePacketDescriptionCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-112">Numero di proprietà in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9e57f-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="9e57f-113">*pStrokePacketDescriptionGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-114">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9e57f-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9e57f-115">*pulPacketDataCountPerStroke* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-116">Matrice contenente il numero di pacchetti in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="9e57f-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="9e57f-117">*plStrokePacketData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-118">Matrice contenente i dati dei pacchetti per i tratti.</span><span class="sxs-lookup"><span data-stu-id="9e57f-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="9e57f-119">*pCustomRecognizer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-119">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-120">[**IContextNode**](icontextnode.md) di tipo **CustomRecognizer** a cui aggiungere i tratti.</span><span class="sxs-lookup"><span data-stu-id="9e57f-120">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="9e57f-121">*ppContextNodeStrokeAddedTo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e57f-122">[**IContextNode**](icontextnode.md) a cui sono stati aggiunti i tratti dall'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="9e57f-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e57f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e57f-123">Return value</span></span>

<span data-ttu-id="9e57f-124">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9e57f-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e57f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e57f-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9e57f-126">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e57f-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="9e57f-127">Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="9e57f-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="9e57f-128">[**IInkAnalyzer**](iinkanalyzer.md) aggiunge i tratti a un [**IContextNode**](icontextnode.md) di tipo **CustomRecognizer** (vedere tipi di [nodo di contesto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="9e57f-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="9e57f-129">Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).</span><span class="sxs-lookup"><span data-stu-id="9e57f-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="9e57f-130">[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti e aggiunge i tratti al primo nodo **UnclassifiedInk** nel nodo **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="9e57f-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="9e57f-131">Se non esiste alcun nodo **UnclassifiedInk** , viene creato.</span><span class="sxs-lookup"><span data-stu-id="9e57f-131">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="9e57f-132">Se il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associato al nodo **CustomRecognizer** non supporta l'identificatore delle impostazioni cultura, il **IInkAnalyzer** continua ad analizzare e genera un avviso [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="9e57f-132">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="9e57f-133">Questo avviso ha un valore [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="9e57f-133">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="9e57f-134">*plStrokePacketData* contiene i dati dei pacchetti per tutti i tratti.</span><span class="sxs-lookup"><span data-stu-id="9e57f-134">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="9e57f-135">*pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="9e57f-135">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="9e57f-136">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9e57f-136">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="9e57f-137">Solo i tratti con le stesse descrizioni di pacchetti possono essere aggiunti in una singola chiamata al **Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="9e57f-137">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokesToCustomRecognizer Method**.</span></span>

 

<span data-ttu-id="9e57f-138">Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione dei tratti aggiunti.</span><span class="sxs-lookup"><span data-stu-id="9e57f-138">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="9e57f-139">[**IInkAnalyzer**](iinkanalyzer.md) restituisce un valore **HRESULT** di **E \_ INVALIDARG** nelle circostanze seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e57f-139">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="9e57f-140">[**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore di uno dei tratti da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9e57f-140">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added.</span></span>
-   <span data-ttu-id="9e57f-141">Il parametro *pCustomRecognizer* contiene un nodo di riconoscimento personalizzato associato a un oggetto [**IInkAnalyzer**](iinkanalyzer.md) diverso.</span><span class="sxs-lookup"><span data-stu-id="9e57f-141">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="9e57f-142">Il parametro *pCustomRecognizer* contiene un [**IContextNode**](icontextnode.md) che non è di tipo **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="9e57f-142">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e57f-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e57f-143">Requirements</span></span>



| <span data-ttu-id="9e57f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e57f-144">Requirement</span></span> | <span data-ttu-id="9e57f-145">Valore</span><span class="sxs-lookup"><span data-stu-id="9e57f-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e57f-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e57f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9e57f-147">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9e57f-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9e57f-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e57f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9e57f-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9e57f-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9e57f-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e57f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e57f-151"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9e57f-151"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9e57f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9e57f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e57f-153"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e57f-153"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9e57f-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e57f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e57f-155">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9e57f-155">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9e57f-156">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="9e57f-156">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="9e57f-157">**Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="9e57f-157">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="9e57f-158">**Metodo IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="9e57f-158">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="9e57f-159">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="9e57f-159">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

