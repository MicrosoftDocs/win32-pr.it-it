---
description: Rappresenta le possibili corrispondenze delle parole per il riconoscimento della grafia per gli oggetti IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interfaccia IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226177"
---
# <a name="ianalysisalternate-interface"></a><span data-ttu-id="ddd42-103">Interfaccia IAnalysisAlternate</span><span class="sxs-lookup"><span data-stu-id="ddd42-103">IAnalysisAlternate interface</span></span>

<span data-ttu-id="ddd42-104">Rappresenta le possibili corrispondenze delle parole per il riconoscimento della grafia per gli oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd42-104">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="ddd42-105">Membri</span><span class="sxs-lookup"><span data-stu-id="ddd42-105">Members</span></span>

<span data-ttu-id="ddd42-106">L'interfaccia **IAnalysisAlternate** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ddd42-106">The **IAnalysisAlternate** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ddd42-107">**IAnalysisAlternate** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ddd42-107">**IAnalysisAlternate** also has these types of members:</span></span>

-   [<span data-ttu-id="ddd42-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddd42-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ddd42-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddd42-109">Methods</span></span>

<span data-ttu-id="ddd42-110">L'interfaccia **IAnalysisAlternate** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ddd42-110">The **IAnalysisAlternate** interface has these methods.</span></span>



| <span data-ttu-id="ddd42-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ddd42-111">Method</span></span>                                                                          | <span data-ttu-id="ddd42-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddd42-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddd42-113">**GetAlternateNodes**</span><span class="sxs-lookup"><span data-stu-id="ddd42-113">**GetAlternateNodes**</span></span>](ianalysisalternate-getalternatenodes.md)               | <span data-ttu-id="ddd42-114">Recupera gli oggetti [**IContextNode**](icontextnode.md) associati a questa alternativa.</span><span class="sxs-lookup"><span data-stu-id="ddd42-114">Retrieves the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span><br/>                                                       |
| [<span data-ttu-id="ddd42-115">**GetRecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="ddd42-115">**GetRecognitionConfidence**</span></span>](ianalysisalternate-getrecognitionconfidence.md) | <span data-ttu-id="ddd42-116">Recupera un valore che indica il livello di attendibilità di [**IInkAnalyzer**](iinkanalyzer.md) nell'accuratezza di **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="ddd42-116">Retrieves a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the **IAnalysisAlternate**.</span></span><br/> |
| [<span data-ttu-id="ddd42-117">**GetRecognizedString**</span><span class="sxs-lookup"><span data-stu-id="ddd42-117">**GetRecognizedString**</span></span>](ianalysisalternate-getrecognizedstring.md)           | <span data-ttu-id="ddd42-118">Recupera il valore stringa riconosciuto dell'oggetto **IAnalysisAlternate** .</span><span class="sxs-lookup"><span data-stu-id="ddd42-118">Retrieves the recognized string value of the **IAnalysisAlternate** object.</span></span><br/>                                                                               |
| [<span data-ttu-id="ddd42-119">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="ddd42-119">**GetStrokeIds**</span></span>](ianalysisalternate-getstrokeids.md)                         | <span data-ttu-id="ddd42-120">Recupera gli identificatori di tratto associati a questo **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="ddd42-120">Retrieves the stroke identifiers that are associated with this **IAnalysisAlternate**.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="ddd42-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddd42-121">Remarks</span></span>

<span data-ttu-id="ddd42-122">Esistono molte varianti nella grafia degli utenti.</span><span class="sxs-lookup"><span data-stu-id="ddd42-122">There are many variations in users' handwriting.</span></span> <span data-ttu-id="ddd42-123">Per questo motivo, i riconoscitori della grafia possono a volte convertire la grafia in testo diverso da quello previsto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ddd42-123">For that reason, handwriting recognizers can sometimes convert handwriting into text that is different from what the user intended.</span></span> <span data-ttu-id="ddd42-124">Quando un [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi su una raccolta di tratti, il **IInkAnalyzer** trova il set di parole più probabile rappresentato dalla grafia.</span><span class="sxs-lookup"><span data-stu-id="ddd42-124">When an [**IInkAnalyzer**](iinkanalyzer.md) performs analysis on a collection of strokes, the **IInkAnalyzer** finds the most likely set of words that the handwriting represents.</span></span> <span data-ttu-id="ddd42-125">Inoltre, **IInkAnalyzer** trova anche set di corrispondenze di riconoscimento alternative, che vengono archiviate in una raccolta [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd42-125">In addition, the **IInkAnalyzer** also finds sets of alternative recognition matches, which are stored in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span> <span data-ttu-id="ddd42-126">Per consentire a un utente di sfruttare le alternative di riconoscimento, è necessario creare un'interfaccia utente che consenta all'utente di selezionare il **IAnalysisAlternate** corretto.</span><span class="sxs-lookup"><span data-stu-id="ddd42-126">In order for a user to take advantage of recognition alternates, you must create a user interface that allows the user to select the correct **IAnalysisAlternate**.</span></span>

<span data-ttu-id="ddd42-127">Gli oggetti **IAnalysisAlternate** vengono in genere ottenuti tramite il [**Metodo IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md).</span><span class="sxs-lookup"><span data-stu-id="ddd42-127">**IAnalysisAlternate** objects are generally obtained through [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md).</span></span> <span data-ttu-id="ddd42-128">Il primo oggetto **IAnalysisAlternate** nella raccolta è quello che [**IInkAnalyzer**](iinkanalyzer.md) considera l'alternativa più probabile.</span><span class="sxs-lookup"><span data-stu-id="ddd42-128">The first **IAnalysisAlternate** object in the collection is what the [**IInkAnalyzer**](iinkanalyzer.md) considers to be the most likely alternate.</span></span>

<span data-ttu-id="ddd42-129">Questa interfaccia è equivalente a [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) nel .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ddd42-129">This interface is equivalent to [System.Windows.Ink.AnalysisCore.AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd42-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddd42-130">Requirements</span></span>



| <span data-ttu-id="ddd42-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddd42-131">Requirement</span></span> | <span data-ttu-id="ddd42-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd42-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd42-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddd42-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd42-134">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ddd42-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ddd42-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddd42-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd42-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ddd42-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ddd42-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddd42-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd42-138"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ddd42-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ddd42-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ddd42-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddd42-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddd42-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ddd42-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddd42-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd42-142">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="ddd42-142">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="ddd42-143">**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="ddd42-143">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="ddd42-144">**Metodo IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="ddd42-144">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="ddd42-145">**Metodo IInkAnalyzer:: getalters**</span><span class="sxs-lookup"><span data-stu-id="ddd42-145">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="ddd42-146">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ddd42-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

