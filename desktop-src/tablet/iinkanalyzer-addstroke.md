---
description: Aggiunge i dati del tratto per un singolo tratto a IInkAnalyzer e assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'Metodo IInkAnalyzer:: AddStroke (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226162"
---
# <a name="iinkanalyzeraddstroke-method"></a><span data-ttu-id="dadcf-103">Metodo IInkAnalyzer:: AddStroke</span><span class="sxs-lookup"><span data-stu-id="dadcf-103">IInkAnalyzer::AddStroke method</span></span>

<span data-ttu-id="dadcf-104">Aggiunge i dati del tratto per un singolo tratto a [**IInkAnalyzer**](iinkanalyzer.md) e assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadcf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dadcf-105">Syntax</span></span>


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="dadcf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dadcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadcf-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dadcf-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadcf-108">Identificatore del tratto da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="dadcf-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="dadcf-109">*ulStrokePacketDataCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dadcf-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadcf-110">Numero di pacchetti nell'oggetto Stroke.</span><span class="sxs-lookup"><span data-stu-id="dadcf-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="dadcf-111">*plStrokePacketData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dadcf-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadcf-112">Matrice contenente i dati del pacchetto per il tratto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="dadcf-113">*ulStrokePacketDescriptionCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dadcf-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadcf-114">Numero di proprietà dei pacchetti in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="dadcf-115">*pStrokePacketDescriptionGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dadcf-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadcf-116">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="dadcf-117">*ppContextNodeStrokeAddedTo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dadcf-117">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dadcf-118">Puntatore a [**IContextNode**](icontextnode.md) a cui [**IInkAnalyzer**](iinkanalyzer.md) ha aggiunto il tratto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-118">A pointer to the [**IContextNode**](icontextnode.md) to which the [**IInkAnalyzer**](iinkanalyzer.md) added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadcf-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dadcf-119">Return value</span></span>

<span data-ttu-id="dadcf-120">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dadcf-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dadcf-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="dadcf-121">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dadcf-122">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-122">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="dadcf-123">Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="dadcf-123">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="dadcf-124">[**IInkAnalyzer**](iinkanalyzer.md) aggiunge il tratto a un [**IContextNode**](icontextnode.md) di tipo UnclassifiedInk (vedere tipi di [nodo di contesto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="dadcf-124">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="dadcf-125">Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).</span><span class="sxs-lookup"><span data-stu-id="dadcf-125">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="dadcf-126">[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto e aggiunge il tratto al primo nodo di contesto UnclassifiedInk nel nodo radice dell'analizzatore di input penna che contiene i tratti con lo stesso identificatore di impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="dadcf-126">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="dadcf-127">Se l'analizzatore di input penna non dispone di un nodo con lo stesso identificatore di impostazioni cultura, viene creato un nuovo nodo di contesto UnclassifiedInk nel nodo radice e il tratto viene aggiunto al nuovo nodo di contesto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="dadcf-127">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="dadcf-128">*plStrokePacketData* contiene i dati dei pacchetti per tutti i punti del tratto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-128">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="dadcf-129">*pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto del tratto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-129">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="dadcf-130">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dadcf-130">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="dadcf-131">Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione del tratto aggiunto.</span><span class="sxs-lookup"><span data-stu-id="dadcf-131">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="dadcf-132">Se [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore del tratto, **IInkAnalyzer** restituisce un valore **HRESULT** di **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="dadcf-132">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dadcf-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dadcf-133">Requirements</span></span>



| <span data-ttu-id="dadcf-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dadcf-134">Requirement</span></span> | <span data-ttu-id="dadcf-135">Valore</span><span class="sxs-lookup"><span data-stu-id="dadcf-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dadcf-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dadcf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dadcf-137">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dadcf-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dadcf-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dadcf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dadcf-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dadcf-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dadcf-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dadcf-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dadcf-141"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dadcf-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dadcf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dadcf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dadcf-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dadcf-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dadcf-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dadcf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadcf-145">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="dadcf-145">**InkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dadcf-146">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="dadcf-146">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="dadcf-147">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="dadcf-147">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="dadcf-148">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="dadcf-148">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="dadcf-149">**Metodo IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="dadcf-149">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="dadcf-150">**Metodo IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="dadcf-150">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="dadcf-151">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="dadcf-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

