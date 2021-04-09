---
description: 'Definisce gli identificatori univoci globali (GUID) per le proprietà di un nodo hint di analisi (vedere IContextNode:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Proprietà hint di analisi (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966390"
---
# <a name="analysis-hint-properties"></a><span data-ttu-id="ca793-103">Proprietà hint di analisi</span><span class="sxs-lookup"><span data-stu-id="ca793-103">Analysis Hint Properties</span></span>

<span data-ttu-id="ca793-104">Definisce gli identificatori univoci globali (GUID) per le proprietà di un nodo hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="ca793-104">Defines globally unique identifiers (GUIDs) for properties of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="ca793-105">Nella tabella seguente vengono descritte le informazioni a cui fa riferimento ogni costante.</span><span class="sxs-lookup"><span data-stu-id="ca793-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="ca793-106">Costante</span><span class="sxs-lookup"><span data-stu-id="ca793-106">Constant</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="ca793-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca793-107">Description</span></span>                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <span data-ttu-id="ca793-108"><dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-108"><dt>**GUID\_AHP\_ALLOWPARTIALDICTIONARYTERMS**</dt></span></span> </dl>       | <span data-ttu-id="ca793-109">Indica se i termini parziali del dizionario sono consentiti in un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-109">Whether partial dictionary terms are allowed on an analysis hint.</span></span><br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <span data-ttu-id="ca793-110"><dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-110"><dt>**GUID\_AHP\_ANALYSISHINTNAME**</dt></span></span> </dl>                                        | <span data-ttu-id="ca793-111">Nome di un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-111">The name of an analysis hint.</span></span><br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <span data-ttu-id="ca793-112"><dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-112"><dt>**GUID\_AHP\_COERCETOFACTOID**</dt></span></span> </dl>                                           | <span data-ttu-id="ca793-113">Indica se l'analizzatore di input penna limita l'analisi dell'input penna all'interno dell'area dell'hint per la conformità al controllo del controllo.</span><span class="sxs-lookup"><span data-stu-id="ca793-113">Whether the ink analyzer limits its analysis of ink within the hint's area to conform to the factoid.</span></span><br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <span data-ttu-id="ca793-114"><dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-114"><dt>**GUID\_AHP\_ENABLEDUNICODECHARACTERRANGES**</dt></span></span> </dl> | <span data-ttu-id="ca793-115">L'hint contiene una matrice di caratteri che rappresentano il set limitato di set di caratteri Unicode supportati da questo oggetto InkRecognizer.</span><span class="sxs-lookup"><span data-stu-id="ca793-115">The hint contains an array of characters that represent the restricted set of supported unicode character set supported by this InkRecognizer.</span></span><br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <span data-ttu-id="ca793-116"><dt>**controllo controllo \_ AHP GUID \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-116"><dt>**GUID\_AHP\_FACTOID**</dt></span></span> </dl>                                                                   | <span data-ttu-id="ca793-117">Controllo del controllo in un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-117">The factoid on an analysis hint.</span></span><br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <span data-ttu-id="ca793-118"><dt>**\_Guida AHP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-118"><dt>**GUID\_AHP\_GUIDE**</dt></span></span> </dl>                                                                         | <span data-ttu-id="ca793-119">Struttura [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) che rappresenta la guida per un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-119">The [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) structure that represents the guide for an analysis hint.</span></span><br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <span data-ttu-id="ca793-120"><dt>**GUID \_ AHP \_ PREFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-120"><dt>**GUID\_AHP\_PREFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="ca793-121">Testo del prefisso in un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-121">The prefix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <span data-ttu-id="ca793-122"><dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-122"><dt>**GUID\_AHP\_SUFFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="ca793-123">Testo del suffisso in un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-123">The suffix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <span data-ttu-id="ca793-124"><dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-124"><dt>**GUID\_AHP\_TOPINKBREAKSONLY**</dt></span></span> </dl>                                        | <span data-ttu-id="ca793-125">Indica se le segmentazioni multiple nei risultati del riconoscimento input penna sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="ca793-125">Whether the multiple segmentations in the ink recognition results are disabled.</span></span><br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <span data-ttu-id="ca793-126"><dt>**\_nome dell'AHP GUID \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-126"><dt>**GUID\_AHP\_WORDLIST**</dt></span></span> </dl>                                                                | <span data-ttu-id="ca793-127">Matrice di stringhe che rappresenta l'elenco di parole per un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-127">The array of strings that represents the word list for an analysis hint.</span></span><br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <span data-ttu-id="ca793-128"><dt>**GUID \_ AHP \_ WORDMODE**</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-128"><dt>**GUID\_AHP\_WORDMODE**</dt></span></span> </dl>                                                                | <span data-ttu-id="ca793-129">Se l'analizzatore di input penna assegna la priorità a una singola parola ai risultati di più parole per un hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca793-129">Whether the ink analyzer prioritizes single-word results over multiple-word results for an analysis hint.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="ca793-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca793-130">Remarks</span></span>

<span data-ttu-id="ca793-131">Questi GUID vengono usati per identificare le proprietà che [**IInkAnalyzer**](iinkanalyzer.md) può impostare in un nodo di contesto dell'hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="ca793-131">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="ca793-132">Per ottenere o impostare le proprietà di un [**IContextNode**](icontextnode.md) in generale, vedere [proprietà del nodo di contesto](context-node-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ca793-132">To get or set properties of an [**IContextNode**](icontextnode.md) in general, see [Context Node Properties](context-node-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca793-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca793-133">Requirements</span></span>



| <span data-ttu-id="ca793-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca793-134">Requirement</span></span> | <span data-ttu-id="ca793-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ca793-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca793-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca793-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ca793-137">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ca793-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ca793-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca793-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ca793-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ca793-139">None supported</span></span><br/>                                                           |
| <span data-ttu-id="ca793-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca793-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca793-141"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca793-141"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca793-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca793-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca793-143">Proprietà del nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="ca793-143">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="ca793-144">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="ca793-144">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="ca793-145">**Metodo IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="ca793-145">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="ca793-146">**Metodo IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="ca793-146">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="ca793-147">**IContextNode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca793-147">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca793-148">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca793-148">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca793-149">**IContextNode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="ca793-149">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="ca793-150">**IContextNode:: LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="ca793-150">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="ca793-151">**IContextNode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca793-151">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca793-152">**IContextNode:: SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="ca793-152">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="ca793-153">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ca793-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




