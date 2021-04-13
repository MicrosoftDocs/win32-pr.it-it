---
description: Aggiunge un nuovo nodo hint di analisi con un'area infinita a IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'Metodo IInkAnalyzer:: CreateAnalysisHint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343706"
---
# <a name="iinkanalyzercreateanalysishint-method"></a><span data-ttu-id="ceba8-103">Metodo IInkAnalyzer:: CreateAnalysisHint</span><span class="sxs-lookup"><span data-stu-id="ceba8-103">IInkAnalyzer::CreateAnalysisHint method</span></span>

<span data-ttu-id="ceba8-104">Aggiunge un nuovo nodo hint di analisi con un'area infinita a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ceba8-104">Adds a new analysis hint node with an infinite area to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ceba8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ceba8-105">Syntax</span></span>


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="ceba8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ceba8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceba8-107">*ppAnalysisHint* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ceba8-107">*ppAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ceba8-108">Nuovo nodo hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ceba8-108">The new analysis hint node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceba8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ceba8-109">Return value</span></span>

<span data-ttu-id="ceba8-110">Vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md) per una descrizione dei valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="ceba8-110">See [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) for a description of the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceba8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ceba8-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ceba8-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAnalysisHint* quando non è più necessario utilizzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ceba8-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHint* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ceba8-113">Per fornire informazioni di contesto aggiuntive per [**IInkAnalyzer**](iinkanalyzer.md), è possibile aggiungere hint di analisi all'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="ceba8-113">To provide extra context information for the [**IInkAnalyzer**](iinkanalyzer.md), you can add analysis hints to the ink analyzer.</span></span> <span data-ttu-id="ceba8-114">Gli hint di analisi possono migliorare l'accuratezza del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="ceba8-114">Analysis hints can improve recognition accuracy.</span></span> <span data-ttu-id="ceba8-115">Ad esempio, è possibile aggiungere il controllo e le informazioni della Guida per i campi in un'applicazione form.</span><span class="sxs-lookup"><span data-stu-id="ceba8-115">For example, you can add factoid and guide information for fields in a form application.</span></span>

<span data-ttu-id="ceba8-116">Questo metodo crea un nuovo [**IContextNode**](icontextnode.md) con un tipo di nodo di contesto di AnalysisHint (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)) e aggiunge il nuovo hint come sottonodo del nodo radice dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il metodo [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="ceba8-116">This method creates a new [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)) and adds the new hint as a subnode of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="ceba8-117">Per aggiungere informazioni di contesto all'hint, utilizzare [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con il parametro *pPropertyDataId* impostato su una delle costanti [proprietà hint di analisi](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="ceba8-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="ceba8-118">Se a un hint viene assegnata un'area infinita, denominato un hint globale, [**IInkAnalyzer**](iinkanalyzer.md) applica il contesto del suggerimento a tutti gli input penna che non si trovano all'interno dell'area di un altro hint.</span><span class="sxs-lookup"><span data-stu-id="ceba8-118">If a hint is assigned an infinite area, termed a global hint, the [**IInkAnalyzer**](iinkanalyzer.md) applies the hint's context to all ink that is not within another hint's area.</span></span> <span data-ttu-id="ceba8-119">È possibile collegare più hint a un singolo **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="ceba8-119">Multiple hints may be attached to a single **IInkAnalyzer**.</span></span> <span data-ttu-id="ceba8-120">Tuttavia, solo un hint globale può essere collegato a un singolo analizzatore di input penna e nessun hint non globale può sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="ceba8-120">However, only one global hint can be attached to a single ink analyzer, and no non-global hints can overlap.</span></span> <span data-ttu-id="ceba8-121">Per ulteriori informazioni sui tipi di informazioni di contesto che possono essere forniti da un hint, vedere [proprietà hint di analisi](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ceba8-121">For more information about the types of context information that a hint can provide, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="ceba8-122">L'aggiunta di un hint di analisi non contrassegna l'area dell'hint per la rianalisi.</span><span class="sxs-lookup"><span data-stu-id="ceba8-122">Adding an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="ceba8-123">Per contrassegnare l'area all'interno dell'hint per la rianalisi, utilizzare il [**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) per impostare l'area dirty sull'Unione dell'area e dell'area dirty correnti dell'hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="ceba8-123">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="ceba8-124">Quando si usano gli hint per un'applicazione form, l'applicazione deve evitare di combinare il contesto del testo con l'input penna nei form.</span><span class="sxs-lookup"><span data-stu-id="ceba8-124">When using hints for a form application, the application should avoid mixing text context with ink in the forms.</span></span> <span data-ttu-id="ceba8-125">Ciò significa che, ad esempio, i nomi dei campi di testo non devono essere creati nell'albero di analisi.</span><span class="sxs-lookup"><span data-stu-id="ceba8-125">This means for example that text field names should not be created in the analysis tree.</span></span> <span data-ttu-id="ceba8-126">Gli hint hanno lo scopo di associare l'input penna alle aree nelle pagine; qualsiasi contesto del testo interferisce con questa associazione Ink-to-hint.</span><span class="sxs-lookup"><span data-stu-id="ceba8-126">Hints are meant to associate the ink to areas on pages; any text context interferes with this ink-to-hint association.</span></span> <span data-ttu-id="ceba8-127">L'operazione di analisi può unire l'input penna e il contesto del testo nella stessa area di scrittura, impedendo che l'input penna venga associato all'area dell'hint.</span><span class="sxs-lookup"><span data-stu-id="ceba8-127">The analysis operation may merge the ink and the text context in the same writing region which would prevent the ink from being associated with the hint area.</span></span>

<span data-ttu-id="ceba8-128">Per altre informazioni sull'analisi dell'input penna, vedere [Cenni preliminari sull'analisi degli input penna](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ceba8-128">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ceba8-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceba8-129">Requirements</span></span>



| <span data-ttu-id="ceba8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceba8-130">Requirement</span></span> | <span data-ttu-id="ceba8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ceba8-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceba8-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceba8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ceba8-133">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ceba8-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ceba8-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceba8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ceba8-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ceba8-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ceba8-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ceba8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceba8-137"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ceba8-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ceba8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ceba8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceba8-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceba8-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ceba8-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceba8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceba8-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ceba8-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ceba8-142">**IContextNode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ceba8-142">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="ceba8-143">**IInkAnalyzer::D Metodo eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="ceba8-143">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="ceba8-144">**Metodo IInkAnalyzer:: GetAnalysisHints**</span><span class="sxs-lookup"><span data-stu-id="ceba8-144">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="ceba8-145">**Metodo IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="ceba8-145">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="ceba8-146">Proprietà hint di analisi</span><span class="sxs-lookup"><span data-stu-id="ceba8-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="ceba8-147">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ceba8-147">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

