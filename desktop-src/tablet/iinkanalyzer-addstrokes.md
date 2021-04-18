---
description: Aggiunge i dati del tratto per più tratti a IInkAnalyzer e assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'Metodo IInkAnalyzer:: AddStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307400"
---
# <a name="iinkanalyzeraddstrokes-method"></a><span data-ttu-id="62033-103">Metodo IInkAnalyzer:: AddStrokes</span><span class="sxs-lookup"><span data-stu-id="62033-103">IInkAnalyzer::AddStrokes method</span></span>

<span data-ttu-id="62033-104">Aggiunge i dati del tratto per più tratti a [**IInkAnalyzer**](iinkanalyzer.md) e assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti.</span><span class="sxs-lookup"><span data-stu-id="62033-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="62033-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62033-105">Syntax</span></span>


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="62033-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62033-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62033-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62033-108">Numero di tratti da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="62033-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="62033-109">*plStrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62033-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62033-110">Matrice contenente gli identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="62033-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="62033-111">*ulStrokePacketDescriptionCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62033-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62033-112">Numero di proprietà in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="62033-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="62033-113">*pStrokePacketDescriptionGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62033-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62033-114">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="62033-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="62033-115">*pulPacketDataCountPerStroke* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62033-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62033-116">Matrice contenente il numero di pacchetti in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="62033-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="62033-117">*plStrokePacketData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62033-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62033-118">Matrice contenente i dati dei pacchetti per i tratti.</span><span class="sxs-lookup"><span data-stu-id="62033-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="62033-119">*ppContextNodeStrokeAddedTo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="62033-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62033-120">[**IContextNode**](icontextnode.md) a cui sono stati aggiunti i tratti dall'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="62033-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62033-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62033-121">Return value</span></span>

<span data-ttu-id="62033-122">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="62033-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62033-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="62033-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="62033-124">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="62033-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="62033-125">Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="62033-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="62033-126">[**IInkAnalyzer**](iinkanalyzer.md) aggiunge i tratti a un [**IContextNode**](icontextnode.md) di tipo UnclassifiedInk (vedere tipi di [nodo di contesto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="62033-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="62033-127">Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).</span><span class="sxs-lookup"><span data-stu-id="62033-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="62033-128">[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti e aggiunge i tratti al primo nodo di contesto UnclassifiedInk nel nodo radice dell'analizzatore di input penna che contiene i tratti con lo stesso identificatore di impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="62033-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="62033-129">Se l'analizzatore di input penna non dispone di un nodo con lo stesso identificatore di impostazioni cultura, viene creato un nuovo nodo di contesto UnclassifiedInk nel nodo radice e i tratti vengono aggiunti al nuovo nodo di contesto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="62033-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="62033-130">*plStrokePacketData* contiene i dati dei pacchetti per tutti i tratti.</span><span class="sxs-lookup"><span data-stu-id="62033-130">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="62033-131">*pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="62033-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="62033-132">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="62033-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="62033-133">Solo i tratti con le stesse descrizioni di pacchetti possono essere aggiunti in una singola chiamata al **Metodo IInkAnalyzer:: AddStrokes**.</span><span class="sxs-lookup"><span data-stu-id="62033-133">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokes Method**.</span></span>

 

<span data-ttu-id="62033-134">Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione dei tratti aggiunti.</span><span class="sxs-lookup"><span data-stu-id="62033-134">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="62033-135">Se [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore di uno dei tratti da aggiungere, il **IInkAnalyzer** restituisce un valore **HRESULT** di **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="62033-135">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62033-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62033-136">Requirements</span></span>



| <span data-ttu-id="62033-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="62033-137">Requirement</span></span> | <span data-ttu-id="62033-138">Valore</span><span class="sxs-lookup"><span data-stu-id="62033-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62033-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62033-139">Minimum supported client</span></span><br/> | <span data-ttu-id="62033-140">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="62033-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="62033-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62033-141">Minimum supported server</span></span><br/> | <span data-ttu-id="62033-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="62033-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="62033-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62033-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="62033-144"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="62033-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="62033-145">DLL</span><span class="sxs-lookup"><span data-stu-id="62033-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62033-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62033-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="62033-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62033-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62033-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="62033-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="62033-149">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="62033-149">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="62033-150">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="62033-150">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="62033-151">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="62033-151">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="62033-152">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="62033-152">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="62033-153">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="62033-153">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="62033-154">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="62033-154">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

