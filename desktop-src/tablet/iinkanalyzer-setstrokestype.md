---
description: Modifica il tipo dei tratti specificati.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'Metodo IInkAnalyzer:: SetStrokesType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307373"
---
# <a name="iinkanalyzersetstrokestype-method"></a><span data-ttu-id="e0ac1-103">Metodo IInkAnalyzer:: SetStrokesType</span><span class="sxs-lookup"><span data-stu-id="e0ac1-103">IInkAnalyzer::SetStrokesType method</span></span>

<span data-ttu-id="e0ac1-104">Modifica il tipo dei tratti specificati.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-104">Changes the type of the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ac1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0ac1-105">Syntax</span></span>


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="e0ac1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0ac1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0ac1-107">*strokeIdCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0ac1-107">*strokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ac1-108">Il numero di identificatori di tratto in *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="e0ac1-109">*plStrokes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0ac1-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ac1-110">Matrice contenente gli identificatori di tratto dei tratti a cui assegnare *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-110">An array containing the stroke identifiers of the strokes to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="e0ac1-111">*StrokeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0ac1-111">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ac1-112">Valore [**StrokeType**](stroketype.md) da assegnare ai tratti.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-112">The [**StrokeType**](stroketype.md) value to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0ac1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0ac1-113">Return value</span></span>

<span data-ttu-id="e0ac1-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e0ac1-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0ac1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0ac1-115">Remarks</span></span>

<span data-ttu-id="e0ac1-116">Se il tipo del tratto è il [](stroketype.md) valore StrokeType **StrokeType \_ unclassifiedd**, [**IInkAnalyzer**](iinkanalyzer.md) classifica il tratto durante l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-116">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="e0ac1-117">In caso contrario, **IInkAnalyzer** usa il tipo impostato sul tratto.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-117">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="e0ac1-118">[**IInkAnalyzer**](iinkanalyzer.md) non imposta il valore del tipo di tratto come parte dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-118">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="e0ac1-119">Per specificare o modificare il tipo di tratto, usare il metodo [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o **IInkAnalyzer:: SetStrokesType**.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-119">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or **IInkAnalyzer::SetStrokesType Method**.</span></span>

<span data-ttu-id="e0ac1-120">Se un tratto è associato a un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)), questo metodo sposta il tratto in un nodo Ink non classificato che contiene tratti della stessa lingua.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-120">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="e0ac1-121">Se non esiste alcun nodo di contesto di questo tipo, questo metodo consente di creare un nuovo nodo Ink non classificato e di aggiungervi il tratto.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-121">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="e0ac1-122">Un nodo Ink non classificato è un **IContextNode** di tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-122">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="e0ac1-123">Se questo metodo sposta un tratto da un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato, questo metodo aggiunge anche il rettangolo di delimitazione del tratto all'area dirty dell'analizzatore dell'input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="e0ac1-123">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="e0ac1-124">Questo metodo non sposta un tratto se il parametro *StrokeType* corrisponde al tipo corrente del tratto.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-124">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="e0ac1-125">Se un tratto identificato in *strokeIds* non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-125">If a stroke identified in *strokeIds* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="e0ac1-126">Se nessuno dei tratti specificati identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-126">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="e0ac1-127">Impostando il tipo di tratto sui tratti associati a un oggetto ContextNode con NodeTypeAndProperties confermato, verrà generata un'eccezione InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-127">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="e0ac1-128">Questo metodo restituisce un codice di errore quando *plStrokes* è **null**.</span><span class="sxs-lookup"><span data-stu-id="e0ac1-128">This method returns an error code when *plStrokes* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ac1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0ac1-129">Requirements</span></span>



| <span data-ttu-id="e0ac1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0ac1-130">Requirement</span></span> | <span data-ttu-id="e0ac1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e0ac1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ac1-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ac1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ac1-133">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e0ac1-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e0ac1-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ac1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ac1-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e0ac1-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e0ac1-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0ac1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0ac1-137"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e0ac1-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e0ac1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e0ac1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0ac1-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0ac1-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e0ac1-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0ac1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ac1-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e0ac1-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e0ac1-142">**Metodo IInkAnalyzer:: GetStrokeType**</span><span class="sxs-lookup"><span data-stu-id="e0ac1-142">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="e0ac1-143">**Metodo IInkAnalyzer:: SetStrokeType**</span><span class="sxs-lookup"><span data-stu-id="e0ac1-143">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="e0ac1-144">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="e0ac1-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




