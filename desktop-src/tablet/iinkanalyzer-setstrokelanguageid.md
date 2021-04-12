---
description: Modifica l'identificatore delle impostazioni locali per il tratto specificato.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'Metodo IInkAnalyzer:: SetStrokeLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526473"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a><span data-ttu-id="8ffad-103">Metodo IInkAnalyzer:: SetStrokeLanguageId</span><span class="sxs-lookup"><span data-stu-id="8ffad-103">IInkAnalyzer::SetStrokeLanguageId method</span></span>

<span data-ttu-id="8ffad-104">Modifica l'identificatore delle impostazioni locali per il tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="8ffad-104">Changes the locale identifier for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ffad-105">Syntax</span></span>


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="8ffad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ffad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffad-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-108">Identificatore del tratto a cui assegnare l'identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="8ffad-108">The identifier of the stroke to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8ffad-109">*lStrokeLCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffad-110">Identificatore delle impostazioni locali da assegnare al tratto.</span><span class="sxs-lookup"><span data-stu-id="8ffad-110">The locale identifier to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffad-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ffad-111">Return value</span></span>

<span data-ttu-id="8ffad-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8ffad-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ffad-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ffad-113">Remarks</span></span>

<span data-ttu-id="8ffad-114">Le impostazioni locali di un tratto vengono impostate quando si aggiunge il tratto chiamando il metodo [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer:: AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="8ffad-114">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="8ffad-115">Per ottenere le impostazioni locali attualmente assegnate a un tratto, chiamare il [**Metodo IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="8ffad-115">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="8ffad-116">Il tratto specificato viene spostato in un nodo Ink non classificato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)) che contiene i tratti della stessa lingua.</span><span class="sxs-lookup"><span data-stu-id="8ffad-116">The specified stroke is moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="8ffad-117">Se non esiste alcun [**IContextNode**](icontextnode.md) di questo tipo, questo metodo crea un nuovo nodo Ink non classificato e lo sposta su di esso.</span><span class="sxs-lookup"><span data-stu-id="8ffad-117">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the stroke to it.</span></span> <span data-ttu-id="8ffad-118">Un nodo Ink non classificato è un **IContextNode** di tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="8ffad-118">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="8ffad-119">Se questo metodo sposta un tratto da un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato, questo metodo aggiunge anche il rettangolo di delimitazione del tratto all'area dirty dell'analizzatore dell'input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="8ffad-119">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="8ffad-120">Questo metodo non sposta un tratto se il parametro *lStrokeLCID* corrisponde all'identificatore di lingua corrente del tratto.</span><span class="sxs-lookup"><span data-stu-id="8ffad-120">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="8ffad-121">Se il tratto specificato non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="8ffad-121">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="8ffad-122">Per altre informazioni sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="8ffad-122">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffad-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ffad-123">Requirements</span></span>



| <span data-ttu-id="8ffad-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ffad-124">Requirement</span></span> | <span data-ttu-id="8ffad-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8ffad-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffad-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ffad-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8ffad-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8ffad-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ffad-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ffad-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8ffad-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8ffad-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8ffad-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ffad-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ffad-131"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffad-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8ffad-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8ffad-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ffad-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ffad-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8ffad-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ffad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffad-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8ffad-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8ffad-136">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="8ffad-136">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="8ffad-137">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="8ffad-137">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="8ffad-138">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="8ffad-138">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="8ffad-139">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="8ffad-139">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="8ffad-140">**Metodo IInkAnalyzer:: GetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="8ffad-140">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="8ffad-141">**Metodo IInkAnalyzer:: SetStrokesLanguageId**</span><span class="sxs-lookup"><span data-stu-id="8ffad-141">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="8ffad-142">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="8ffad-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

