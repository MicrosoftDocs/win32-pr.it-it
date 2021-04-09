---
description: Aggiunge i dati del tratto per un singolo tratto a IInkAnalyzer e assegna un identificatore di impostazioni cultura specifico al tratto.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'Metodo IInkAnalyzer:: AddStrokeForLanguage (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879346"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a><span data-ttu-id="6b05d-103">Metodo IInkAnalyzer:: AddStrokeForLanguage</span><span class="sxs-lookup"><span data-stu-id="6b05d-103">IInkAnalyzer::AddStrokeForLanguage method</span></span>

<span data-ttu-id="6b05d-104">Aggiunge i dati del tratto per un singolo tratto a [**IInkAnalyzer**](iinkanalyzer.md) e assegna un identificatore di impostazioni cultura specifico al tratto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns a specific culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b05d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b05d-105">Syntax</span></span>


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="6b05d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b05d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b05d-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b05d-108">Identificatore del tratto da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6b05d-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="6b05d-109">*lStrokeLCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b05d-110">Identificatore delle impostazioni cultura da assegnare al tratto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-110">The culture identifier to assign to the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="6b05d-111">*ulStrokePacketDataCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-111">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b05d-112">Numero di pacchetti nell'oggetto Stroke.</span><span class="sxs-lookup"><span data-stu-id="6b05d-112">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="6b05d-113">*plStrokePacketData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-113">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b05d-114">Matrice contenente i dati del pacchetto per il tratto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-114">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="6b05d-115">*ulStrokePacketDescriptionCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-115">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b05d-116">Numero di proprietà in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-116">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="6b05d-117">*pStrokePacketDescriptionGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-117">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b05d-118">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-118">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="6b05d-119">*ppContextNodeStrokeAddedTo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b05d-120">Puntatore il cui valore è impostato sul puntatore di [**IContextNode**](icontextnode.md) che contiene il tratto appena aggiunto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-120">A pointer whose value is set to the pointer of the [**IContextNode**](icontextnode.md) that contains the newly added stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b05d-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b05d-121">Return value</span></span>

<span data-ttu-id="6b05d-122">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6b05d-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b05d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b05d-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6b05d-124">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="6b05d-125">Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="6b05d-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="6b05d-126">[**IInkAnalyzer**](iinkanalyzer.md) aggiunge il tratto a un [**IContextNode**](icontextnode.md) di tipo UnclassifiedInk (vedere tipi di [nodo di contesto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="6b05d-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="6b05d-127">Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).</span><span class="sxs-lookup"><span data-stu-id="6b05d-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="6b05d-128">[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura *lStrokeLCID* al tratto e aggiunge il tratto al primo nodo di contesto UnclassifiedInk nel nodo radice dell'analizzatore di input penna che contiene i tratti con lo stesso identificatore di impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="6b05d-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns *lStrokeLCID* culture identifier to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="6b05d-129">Se l'analizzatore di input penna non dispone di un nodo con lo stesso identificatore di impostazioni cultura, viene creato un nuovo nodo di contesto UnclassifiedInk nel nodo radice e il tratto viene aggiunto al nuovo nodo di contesto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="6b05d-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="6b05d-130">*plStrokePacketData* contiene i dati dei pacchetti per tutti i punti del tratto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-130">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="6b05d-131">*pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto del tratto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="6b05d-132">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6b05d-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="6b05d-133">Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione del tratto aggiunto.</span><span class="sxs-lookup"><span data-stu-id="6b05d-133">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="6b05d-134">Se [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore del tratto, **IInkAnalyzer** restituisce un valore **HRESULT** di **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="6b05d-134">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b05d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b05d-135">Requirements</span></span>



| <span data-ttu-id="6b05d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b05d-136">Requirement</span></span> | <span data-ttu-id="6b05d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="6b05d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b05d-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b05d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6b05d-139">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6b05d-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6b05d-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b05d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6b05d-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6b05d-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6b05d-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b05d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b05d-143"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6b05d-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6b05d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6b05d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b05d-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b05d-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6b05d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b05d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b05d-147">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6b05d-147">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6b05d-148">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="6b05d-148">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="6b05d-149">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="6b05d-149">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="6b05d-150">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="6b05d-150">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="6b05d-151">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="6b05d-151">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="6b05d-152">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="6b05d-152">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="6b05d-153">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="6b05d-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

