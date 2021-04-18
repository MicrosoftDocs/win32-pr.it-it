---
description: Modifica l'identificatore delle impostazioni locali per i tratti specificati.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'Metodo IInkAnalyzer:: SetStrokesLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307374"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a><span data-ttu-id="86c66-103">Metodo IInkAnalyzer:: SetStrokesLanguageId</span><span class="sxs-lookup"><span data-stu-id="86c66-103">IInkAnalyzer::SetStrokesLanguageId method</span></span>

<span data-ttu-id="86c66-104">Modifica l'identificatore delle impostazioni locali per i tratti specificati.</span><span class="sxs-lookup"><span data-stu-id="86c66-104">Changes the locale identifier for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c66-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86c66-105">Syntax</span></span>


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a><span data-ttu-id="86c66-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86c66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c66-107">*ulStrokeIdCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c66-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c66-108">Il numero di identificatori di tratto in *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="86c66-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="86c66-109">*plStrokes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c66-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c66-110">Matrice di identificatori per i tratti a cui assegnare l'identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="86c66-110">The array of identifiers for the strokes to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="86c66-111">*lStrokesLCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c66-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c66-112">Identificatore delle impostazioni locali da assegnare ai tratti.</span><span class="sxs-lookup"><span data-stu-id="86c66-112">The locale identifier to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c66-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86c66-113">Return value</span></span>

<span data-ttu-id="86c66-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="86c66-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="86c66-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="86c66-115">Remarks</span></span>

<span data-ttu-id="86c66-116">Le impostazioni locali di un tratto vengono impostate quando si aggiunge il tratto chiamando il metodo [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer:: AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="86c66-116">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="86c66-117">Per ottenere le impostazioni locali attualmente assegnate a un tratto, chiamare il [**Metodo IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="86c66-117">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="86c66-118">I tratti specificati vengono spostati in un nodo Ink non classificato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)) che contiene i tratti della stessa lingua.</span><span class="sxs-lookup"><span data-stu-id="86c66-118">The specified strokes are moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="86c66-119">Se non esiste alcun [**IContextNode**](icontextnode.md) di questo tipo, questo metodo crea un nuovo nodo di input penna non classificato e lo sposta.</span><span class="sxs-lookup"><span data-stu-id="86c66-119">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the strokes to it.</span></span> <span data-ttu-id="86c66-120">Un nodo Ink non classificato è un **IContextNode** di tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="86c66-120">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="86c66-121">Se questo metodo sposta i tratti da un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato, questo metodo aggiunge anche i rettangoli di delimitazione dei tratti all'area dirty dell'analizzatore dell'input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="86c66-121">If this method moves strokes from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the strokes' bounding boxes to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="86c66-122">Questo metodo non sposta un tratto se il parametro *lStrokeLCID* corrisponde all'identificatore di lingua corrente del tratto.</span><span class="sxs-lookup"><span data-stu-id="86c66-122">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="86c66-123">Se un tratto specificato non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.</span><span class="sxs-lookup"><span data-stu-id="86c66-123">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="86c66-124">Se nessuno dei tratti specificati identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="86c66-124">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="86c66-125">Questo metodo restituisce un codice di errore quando strokeIds è **null**.</span><span class="sxs-lookup"><span data-stu-id="86c66-125">This method returns an error code when strokeIds is **NULL**.</span></span>

<span data-ttu-id="86c66-126">Per altre informazioni sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="86c66-126">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="86c66-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86c66-127">Requirements</span></span>



| <span data-ttu-id="86c66-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c66-128">Requirement</span></span> | <span data-ttu-id="86c66-129">Valore</span><span class="sxs-lookup"><span data-stu-id="86c66-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c66-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c66-130">Minimum supported client</span></span><br/> | <span data-ttu-id="86c66-131">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="86c66-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="86c66-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c66-132">Minimum supported server</span></span><br/> | <span data-ttu-id="86c66-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="86c66-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="86c66-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86c66-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c66-135"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="86c66-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="86c66-136">DLL</span><span class="sxs-lookup"><span data-stu-id="86c66-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c66-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c66-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="86c66-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86c66-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c66-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="86c66-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="86c66-140">**Metodo IInkAnalyzer:: AddStroke**</span><span class="sxs-lookup"><span data-stu-id="86c66-140">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="86c66-141">**Metodo IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="86c66-141">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="86c66-142">**Metodo IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="86c66-142">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="86c66-143">**Metodo IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="86c66-143">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="86c66-144">**Metodo IInkAnalyzer:: GetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="86c66-144">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="86c66-145">**Metodo IInkAnalyzer:: SetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="86c66-145">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="86c66-146">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="86c66-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

