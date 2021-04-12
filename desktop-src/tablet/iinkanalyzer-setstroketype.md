---
description: Modifica il tipo del tratto specificato.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'Metodo IInkAnalyzer:: SetStrokeType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129435"
---
# <a name="iinkanalyzersetstroketype-method"></a><span data-ttu-id="4c38f-103">Metodo IInkAnalyzer:: SetStrokeType</span><span class="sxs-lookup"><span data-stu-id="4c38f-103">IInkAnalyzer::SetStrokeType method</span></span>

<span data-ttu-id="4c38f-104">Modifica il tipo del tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="4c38f-104">Changes the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c38f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c38f-105">Syntax</span></span>


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="4c38f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c38f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c38f-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c38f-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c38f-108">Identificatore del tratto a cui assegnare *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="4c38f-108">The stroke identifier of the stroke to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="4c38f-109">*StrokeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c38f-109">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c38f-110">Valore [**StrokeType**](stroketype.md) da assegnare al tratto.</span><span class="sxs-lookup"><span data-stu-id="4c38f-110">The [**StrokeType**](stroketype.md) value to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c38f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c38f-111">Return value</span></span>

<span data-ttu-id="4c38f-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4c38f-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c38f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c38f-113">Remarks</span></span>

<span data-ttu-id="4c38f-114">Se il tipo del tratto è il [](stroketype.md) valore StrokeType **StrokeType \_ unclassifiedd**, [**IInkAnalyzer**](iinkanalyzer.md) classifica il tratto durante l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="4c38f-114">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="4c38f-115">In caso contrario, **IInkAnalyzer** usa il tipo impostato sul tratto.</span><span class="sxs-lookup"><span data-stu-id="4c38f-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="4c38f-116">[**IInkAnalyzer**](iinkanalyzer.md) non imposta il valore del tipo di tratto come parte dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="4c38f-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="4c38f-117">Per specificare o modificare il tipo di tratto, usare il metodo **IInkAnalyzer:: SetStrokeType** o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="4c38f-117">To specify or change the stroke type, use **IInkAnalyzer::SetStrokeType Method** or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

<span data-ttu-id="4c38f-118">Se un tratto è associato a un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)), questo metodo sposta il tratto in un nodo Ink non classificato che contiene tratti della stessa lingua.</span><span class="sxs-lookup"><span data-stu-id="4c38f-118">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="4c38f-119">Se non esiste alcun nodo di contesto di questo tipo, questo metodo consente di creare un nuovo nodo Ink non classificato e di aggiungervi il tratto.</span><span class="sxs-lookup"><span data-stu-id="4c38f-119">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="4c38f-120">Un nodo Ink non classificato è un **IContextNode** di tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="4c38f-120">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="4c38f-121">Se questo metodo sposta un tratto da un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato, questo metodo aggiunge anche il rettangolo di delimitazione del tratto all'area dirty dell'analizzatore dell'input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="4c38f-121">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="4c38f-122">Questo metodo non sposta un tratto se il parametro *StrokeType* corrisponde al tipo corrente del tratto.</span><span class="sxs-lookup"><span data-stu-id="4c38f-122">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="4c38f-123">Impostando il tipo di tratto sui tratti associati a un oggetto ContextNode con NodeTypeAndProperties confermato, verrà generata un'eccezione InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="4c38f-123">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="4c38f-124">Se il tratto specificato non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="4c38f-124">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c38f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c38f-125">Requirements</span></span>



| <span data-ttu-id="4c38f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c38f-126">Requirement</span></span> | <span data-ttu-id="4c38f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4c38f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c38f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c38f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4c38f-129">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4c38f-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4c38f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c38f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4c38f-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4c38f-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4c38f-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c38f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c38f-133"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4c38f-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4c38f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4c38f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c38f-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c38f-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4c38f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c38f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c38f-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4c38f-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4c38f-138">**Metodo IInkAnalyzer:: GetStrokeType**</span><span class="sxs-lookup"><span data-stu-id="4c38f-138">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="4c38f-139">**Metodo IInkAnalyzer:: SetStrokesType**</span><span class="sxs-lookup"><span data-stu-id="4c38f-139">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="4c38f-140">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4c38f-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




