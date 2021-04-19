---
description: Aggiunge i dati del tratto per un singolo tratto a un nodo di riconoscimento personalizzato.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307397"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a><span data-ttu-id="3733a-103">Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer</span><span class="sxs-lookup"><span data-stu-id="3733a-103">IInkAnalyzer::AddStrokeToCustomRecognizer method</span></span>

<span data-ttu-id="3733a-104">Aggiunge i dati del tratto per un singolo tratto a un nodo di riconoscimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3733a-104">Adds stroke data for a single stroke to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="3733a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3733a-105">Syntax</span></span>


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="3733a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3733a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3733a-107">*ulStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3733a-107">*ulStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3733a-108">Identificatore del tratto da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3733a-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="3733a-109">*ulStrokePacketDataCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3733a-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3733a-110">Numero di pacchetti nell'oggetto Stroke.</span><span class="sxs-lookup"><span data-stu-id="3733a-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="3733a-111">*plStrokePacketData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3733a-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3733a-112">Matrice contenente i dati del pacchetto per il tratto.</span><span class="sxs-lookup"><span data-stu-id="3733a-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="3733a-113">*ulStrokePacketDescriptionCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3733a-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3733a-114">Numero di proprietà dei pacchetti in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3733a-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="3733a-115">*pStrokePacketDescriptionGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3733a-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3733a-116">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3733a-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="3733a-117">*pCustomRecognizer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3733a-117">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3733a-118">[**IContextNode**](icontextnode.md) di tipo **CustomRecognizer** a cui aggiungere il tratto.</span><span class="sxs-lookup"><span data-stu-id="3733a-118">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="3733a-119">*ppContextNodeStrokeAddedTo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3733a-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3733a-120">[**IContextNode**](icontextnode.md) a cui l'analizzatore di input penna ha aggiunto il tratto.</span><span class="sxs-lookup"><span data-stu-id="3733a-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3733a-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3733a-121">Return value</span></span>

<span data-ttu-id="3733a-122">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3733a-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3733a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3733a-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3733a-124">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3733a-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="3733a-125">Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="3733a-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="3733a-126">[**IInkAnalyzer**](iinkanalyzer.md) aggiunge il tratto a un [**IContextNode**](icontextnode.md) di tipo **CustomRecognizer** (vedere tipi di [nodo di contesto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="3733a-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="3733a-127">Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).</span><span class="sxs-lookup"><span data-stu-id="3733a-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="3733a-128">[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto e aggiunge il tratto al primo nodo **UnclassifiedInk** nel nodo **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="3733a-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="3733a-129">Se non esiste alcun nodo **UnclassifiedInk** , viene creato.</span><span class="sxs-lookup"><span data-stu-id="3733a-129">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="3733a-130">Se il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associato al nodo **CustomRecognizer** non supporta l'identificatore delle impostazioni cultura, il **IInkAnalyzer** continua ad analizzare e genera un avviso [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="3733a-130">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="3733a-131">Questo avviso ha un valore [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="3733a-131">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="3733a-132">*plStrokePacketData* contiene i dati dei pacchetti per tutti i punti del tratto.</span><span class="sxs-lookup"><span data-stu-id="3733a-132">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="3733a-133">*pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="3733a-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="3733a-134">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3733a-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="3733a-135">Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione del tratto aggiunto.</span><span class="sxs-lookup"><span data-stu-id="3733a-135">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="3733a-136">[**IInkAnalyzer**](iinkanalyzer.md) restituisce un valore **HRESULT** di **E \_ INVALIDARG** nelle circostanze seguenti.</span><span class="sxs-lookup"><span data-stu-id="3733a-136">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="3733a-137">[**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore del tratto da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3733a-137">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as the stroke to be added.</span></span>
-   <span data-ttu-id="3733a-138">Il parametro *pCustomRecognizer* contiene un nodo di riconoscimento personalizzato associato a un oggetto [**IInkAnalyzer**](iinkanalyzer.md) diverso.</span><span class="sxs-lookup"><span data-stu-id="3733a-138">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="3733a-139">Il parametro *pCustomRecognizer* contiene un [**IContextNode**](icontextnode.md) che non è di tipo **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="3733a-139">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3733a-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3733a-140">Requirements</span></span>



| <span data-ttu-id="3733a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3733a-141">Requirement</span></span> | <span data-ttu-id="3733a-142">Valore</span><span class="sxs-lookup"><span data-stu-id="3733a-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3733a-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3733a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3733a-144">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3733a-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3733a-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3733a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3733a-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3733a-146">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3733a-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3733a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3733a-148"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3733a-148"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3733a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3733a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3733a-150"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3733a-150"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3733a-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3733a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3733a-152">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3733a-152">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3733a-153">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="3733a-153">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="3733a-154">**Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="3733a-154">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="3733a-155">**Metodo IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="3733a-155">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="3733a-156">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="3733a-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

