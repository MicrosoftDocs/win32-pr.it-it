---
description: Fornisce l'accesso ai riconoscitori della grafia per l'utilizzo con l'analisi dell'input penna.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interfaccia IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307405"
---
# <a name="iinkanalysisrecognizer-interface"></a><span data-ttu-id="91abe-103">Interfaccia IInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="91abe-103">IInkAnalysisRecognizer interface</span></span>

<span data-ttu-id="91abe-104">Fornisce l'accesso ai riconoscitori della grafia per l'utilizzo con l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="91abe-104">Provides access to handwriting recognizers for use with ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="91abe-105">Membri</span><span class="sxs-lookup"><span data-stu-id="91abe-105">Members</span></span>

<span data-ttu-id="91abe-106">L'interfaccia **IInkAnalysisRecognizer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="91abe-106">The **IInkAnalysisRecognizer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91abe-107">**IInkAnalysisRecognizer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="91abe-107">**IInkAnalysisRecognizer** also has these types of members:</span></span>

-   [<span data-ttu-id="91abe-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="91abe-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="91abe-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="91abe-109">Methods</span></span>

<span data-ttu-id="91abe-110">L'interfaccia **IInkAnalysisRecognizer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="91abe-110">The **IInkAnalysisRecognizer** interface has these methods.</span></span>



| <span data-ttu-id="91abe-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="91abe-111">Method</span></span>                                                                          | <span data-ttu-id="91abe-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91abe-112">Description</span></span>                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91abe-113">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="91abe-113">**GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)               | <span data-ttu-id="91abe-114">Recupera le funzionalità del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="91abe-114">Retrieves the capabilities of the recognizer.</span></span><br/>                                                                       |
| [<span data-ttu-id="91abe-115">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="91abe-115">**GetGuid**</span></span>](iinkanalysisrecognizer-getguid.md)                               | <span data-ttu-id="91abe-116">Recupera l'identificatore univoco globale (GUID) del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="91abe-116">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span><br/>                                                  |
| [<span data-ttu-id="91abe-117">**GetLanguages**</span><span class="sxs-lookup"><span data-stu-id="91abe-117">**GetLanguages**</span></span>](iinkanalysisrecognizer-getlanguages.md)                     | <span data-ttu-id="91abe-118">Recupera gli identificatori per le impostazioni locali supportate da questo **IInkAnalysisRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="91abe-118">Retrieves the identifiers for the locales that this **IInkAnalysisRecognizer** supports.</span></span><br/>                            |
| [<span data-ttu-id="91abe-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="91abe-119">**GetName**</span></span>](iinkanalysisrecognizer-getname.md)                               | <span data-ttu-id="91abe-120">Recupera il nome del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="91abe-120">Retrieves the name of the recognizer.</span></span><br/>                                                                               |
| [<span data-ttu-id="91abe-121">**GetSupportedProperties**</span><span class="sxs-lookup"><span data-stu-id="91abe-121">**GetSupportedProperties**</span></span>](iinkanalysisrecognizer-getsupportedproperties.md) | <span data-ttu-id="91abe-122">Recupera gli identificatori univoci globali (GUID) per le proprietà supportate da questo **IInkAnalysisRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="91abe-122">Retrieves the globally unique identifiers (GUIDs) for the properties that this **IInkAnalysisRecognizer** supports.</span></span><br/> |
| [<span data-ttu-id="91abe-123">**Getvendor**</span><span class="sxs-lookup"><span data-stu-id="91abe-123">**GetVendor**</span></span>](iinkanalysisrecognizer-getvendor.md)                           | <span data-ttu-id="91abe-124">Recupera il nome del fornitore del **IInkAnalysisRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="91abe-124">Retrieves the vendor name of the **IInkAnalysisRecognizer**.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="91abe-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="91abe-125">Remarks</span></span>

<span data-ttu-id="91abe-126">Un riconoscitore ha attributi e proprietà specifici che consentono di eseguire il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="91abe-126">A recognizer has specific attributes and properties that allow it to perform recognition.</span></span> <span data-ttu-id="91abe-127">È necessario determinare le proprietà di un riconoscimento prima che possa verificarsi il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="91abe-127">The properties of a recognizer must be determined before recognition can occur.</span></span> <span data-ttu-id="91abe-128">I tipi di proprietà che un riconoscimento supporta determinano i tipi di riconoscimento che può eseguire.</span><span class="sxs-lookup"><span data-stu-id="91abe-128">The types of properties that a recognizer supports determine the types of recognition that it can perform.</span></span> <span data-ttu-id="91abe-129">Se, ad esempio, un riconoscimento non supporta la grafia in corsivo, restituisce risultati non accurati quando un utente scrive in corsivo.</span><span class="sxs-lookup"><span data-stu-id="91abe-129">For instance, if a recognizer does not support cursive handwriting, it returns inaccurate results when a user writes in cursive.</span></span>

<span data-ttu-id="91abe-130">Un riconoscimento dispone inoltre di una funzionalità incorporata che gestisce automaticamente molti aspetti della grafia.</span><span class="sxs-lookup"><span data-stu-id="91abe-130">A recognizer also has built-in functionality that automatically manages many aspects of handwriting.</span></span> <span data-ttu-id="91abe-131">Ad esempio, determina la metrica per le linee in cui vengono disegnati i tratti.</span><span class="sxs-lookup"><span data-stu-id="91abe-131">For instance, it determines the metrics for the lines on which strokes are drawn.</span></span> <span data-ttu-id="91abe-132">È possibile restituire il numero di riga di un tratto, ma non è mai necessario specificare come vengono determinate le metriche della riga a causa della funzionalità incorporata del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="91abe-132">You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.</span></span>

<span data-ttu-id="91abe-133">[**IInkAnalyzer**](iinkanalyzer.md) gestisce un elenco di riconoscitori disponibili.</span><span class="sxs-lookup"><span data-stu-id="91abe-133">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a list of available recognizers.</span></span> <span data-ttu-id="91abe-134">Per accedere a questo elenco, usare il metodo [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .</span><span class="sxs-lookup"><span data-stu-id="91abe-134">To access this list, use the [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91abe-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91abe-135">Requirements</span></span>



| <span data-ttu-id="91abe-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="91abe-136">Requirement</span></span> | <span data-ttu-id="91abe-137">Valore</span><span class="sxs-lookup"><span data-stu-id="91abe-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91abe-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91abe-138">Minimum supported client</span></span><br/> | <span data-ttu-id="91abe-139">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="91abe-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="91abe-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91abe-140">Minimum supported server</span></span><br/> | <span data-ttu-id="91abe-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="91abe-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="91abe-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91abe-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="91abe-143"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="91abe-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="91abe-144">DLL</span><span class="sxs-lookup"><span data-stu-id="91abe-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91abe-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91abe-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="91abe-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91abe-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91abe-147">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="91abe-147">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="91abe-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="91abe-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="91abe-149">**Metodo IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="91abe-149">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="91abe-150">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="91abe-150">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="91abe-151">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="91abe-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

