---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IInkAnalysisRecognizer e che rappresentano la possibilità di riconoscere grafia, oggetti o movimenti.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interfaccia IInkAnalysisRecognizers (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343716"
---
# <a name="iinkanalysisrecognizers-interface"></a><span data-ttu-id="502f1-103">Interfaccia IInkAnalysisRecognizers</span><span class="sxs-lookup"><span data-stu-id="502f1-103">IInkAnalysisRecognizers interface</span></span>

<span data-ttu-id="502f1-104">Contiene una raccolta di oggetti che implementano l'interfaccia [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e che rappresentano la possibilità di riconoscere grafia, oggetti o movimenti.</span><span class="sxs-lookup"><span data-stu-id="502f1-104">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span>

## <a name="members"></a><span data-ttu-id="502f1-105">Membri</span><span class="sxs-lookup"><span data-stu-id="502f1-105">Members</span></span>

<span data-ttu-id="502f1-106">L'interfaccia **IInkAnalysisRecognizers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="502f1-106">The **IInkAnalysisRecognizers** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="502f1-107">**IInkAnalysisRecognizers** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="502f1-107">**IInkAnalysisRecognizers** also has these types of members:</span></span>

-   [<span data-ttu-id="502f1-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="502f1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="502f1-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="502f1-109">Methods</span></span>

<span data-ttu-id="502f1-110">L'interfaccia **IInkAnalysisRecognizers** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="502f1-110">The **IInkAnalysisRecognizers** interface has these methods.</span></span>



| <span data-ttu-id="502f1-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="502f1-111">Method</span></span>                                                                               | <span data-ttu-id="502f1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="502f1-112">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="502f1-113">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="502f1-113">**GetCount**</span></span>](iinkanalysisrecognizers-getcount.md)                                 | <span data-ttu-id="502f1-114">Recupera il numero di oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="502f1-114">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span><br/> |
| [<span data-ttu-id="502f1-115">**GetInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="502f1-115">**GetInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | <span data-ttu-id="502f1-116">Recupera l'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="502f1-116">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="502f1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="502f1-117">Remarks</span></span>

<span data-ttu-id="502f1-118">Il metodo [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) metodo di [**IInkAnalyzer**](iinkanalyzer.md) restituisce una raccolta **IInkAnalysisRecognizers** contenente i riconoscitori Ink disponibili sul Tablet PC corrente.</span><span class="sxs-lookup"><span data-stu-id="502f1-118">The [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method of [**IInkAnalyzer**](iinkanalyzer.md) returns an **IInkAnalysisRecognizers** collection containing the ink recognizers available on the current Tablet PC.</span></span>

<span data-ttu-id="502f1-119">Per un riconoscimento della lingua, il metodo [**IInkAnalysisRecognizer:: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) restituisce una matrice non vuota.</span><span class="sxs-lookup"><span data-stu-id="502f1-119">For a language recognizer, the [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) method returns a non-empty array.</span></span> <span data-ttu-id="502f1-120">Per i riconoscitori di movimento e i riconoscitori di oggetti, il metodo **IInkAnalysisRecognizer:: GetLanguages** restituisce una matrice vuota.</span><span class="sxs-lookup"><span data-stu-id="502f1-120">For both gesture recognizers and object recognizers, the **IInkAnalysisRecognizer::GetLanguages** method returns an empty array.</span></span>

## <a name="requirements"></a><span data-ttu-id="502f1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="502f1-121">Requirements</span></span>



| <span data-ttu-id="502f1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="502f1-122">Requirement</span></span> | <span data-ttu-id="502f1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="502f1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="502f1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="502f1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="502f1-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="502f1-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="502f1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="502f1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="502f1-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="502f1-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="502f1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="502f1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="502f1-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="502f1-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="502f1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="502f1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="502f1-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="502f1-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="502f1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="502f1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="502f1-133">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="502f1-133">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="502f1-134">**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**</span><span class="sxs-lookup"><span data-stu-id="502f1-134">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="502f1-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="502f1-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

