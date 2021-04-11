---
description: Aggiunge i dati del tratto per più tratti a IInkAnalyzer e assegna l'identificatore delle impostazioni cultura specificato ai tratti.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'Metodo IInkAnalyzer:: AddStrokesForLanguage (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226161"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a><span data-ttu-id="f78f6-103">Metodo IInkAnalyzer:: AddStrokesForLanguage</span><span class="sxs-lookup"><span data-stu-id="f78f6-103">IInkAnalyzer::AddStrokesForLanguage method</span></span>

<span data-ttu-id="f78f6-104">Aggiunge i dati del tratto per più tratti a [**IInkAnalyzer**](iinkanalyzer.md) e assegna l'identificatore delle impostazioni cultura specificato ai tratti.</span><span class="sxs-lookup"><span data-stu-id="f78f6-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the specified culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f78f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f78f6-105">Syntax</span></span>


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="f78f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f78f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f78f6-107">*ulStrokeIdsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-108">Numero di tratti da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f78f6-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="f78f6-109">*plIdofStrokesToAdd* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-109">*plIdofStrokesToAdd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-110">Matrice contenente gli identificatori del tratto.</span><span class="sxs-lookup"><span data-stu-id="f78f6-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f78f6-111">*lStrokesLCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-112">Valore che rappresenta l'identificatore di impostazioni cultura da assegnare ai tratti.</span><span class="sxs-lookup"><span data-stu-id="f78f6-112">A value that represents the culture identifier to assign to the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="f78f6-113">*ulStrokePacketDescriptionCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-114">Numero di proprietà in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f78f6-114">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="f78f6-115">*pStrokePacketDescriptionGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-116">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f78f6-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f78f6-117">*pulPacketDataCountPerStroke* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-117">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-118">Matrice contenente il numero di pacchetti in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="f78f6-118">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="f78f6-119">*plStrokePacketData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-119">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-120">Matrice contenente i dati dei pacchetti per i tratti.</span><span class="sxs-lookup"><span data-stu-id="f78f6-120">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="f78f6-121">*ppContextNodeStrokeAddedTo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f78f6-122">[**IContextNode**](icontextnode.md) a cui sono stati aggiunti i tratti dall'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="f78f6-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f78f6-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f78f6-123">Return value</span></span>

<span data-ttu-id="f78f6-124">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f78f6-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f78f6-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f78f6-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f78f6-126">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f78f6-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="f78f6-127">Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="f78f6-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="f78f6-128">[**IInkAnalyzer**](iinkanalyzer.md) aggiunge i tratti a un [**IContextNode**](icontextnode.md) di tipo UnclassifiedInk (vedere tipi di [nodo di contesto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="f78f6-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="f78f6-129">Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).</span><span class="sxs-lookup"><span data-stu-id="f78f6-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="f78f6-130">[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura *lStrokeLCID* ai tratti e aggiunge i tratti al primo nodo di contesto UnclassifiedInk nel nodo radice dell'analizzatore di input penna che contiene i tratti con lo stesso identificatore di impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="f78f6-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the *lStrokeLCID* culture identifier to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="f78f6-131">Se l'analizzatore di input penna non dispone di un nodo con lo stesso identificatore di impostazioni cultura, viene creato un nuovo nodo di contesto UnclassifiedInk nel nodo radice e i tratti vengono aggiunti al nuovo nodo di contesto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="f78f6-131">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="f78f6-132">*plStrokePacketData* contiene i dati dei pacchetti per tutti i tratti.</span><span class="sxs-lookup"><span data-stu-id="f78f6-132">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="f78f6-133">*pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto.</span><span class="sxs-lookup"><span data-stu-id="f78f6-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="f78f6-134">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f78f6-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="f78f6-135">Solo i tratti con le stesse descrizioni di pacchetti possono essere aggiunti in una singola chiamata al [**Metodo IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="f78f6-135">Only strokes with the same packet descriptions can be added in a single call to [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md).</span></span>

 

<span data-ttu-id="f78f6-136">Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione dei tratti aggiunti.</span><span class="sxs-lookup"><span data-stu-id="f78f6-136">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="f78f6-137">Se [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore di uno dei tratti da aggiungere, il **IInkAnalyzer** restituisce un valore **HRESULT** di **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="f78f6-137">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f78f6-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f78f6-138">Requirements</span></span>



| <span data-ttu-id="f78f6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f78f6-139">Requirement</span></span> | <span data-ttu-id="f78f6-140">Valore</span><span class="sxs-lookup"><span data-stu-id="f78f6-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f78f6-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f78f6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f78f6-142">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f78f6-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f78f6-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f78f6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f78f6-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f78f6-144">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f78f6-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f78f6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f78f6-146"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f78f6-146"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f78f6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f78f6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f78f6-148"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f78f6-148"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f78f6-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f78f6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78f6-150">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f78f6-150">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f78f6-151">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="f78f6-151">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="f78f6-152">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="f78f6-152">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="f78f6-153">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="f78f6-153">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="f78f6-154">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="f78f6-154">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="f78f6-155">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="f78f6-155">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="f78f6-156">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f78f6-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

