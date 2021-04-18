---
description: Specifica il set di avvisi disponibili che possono verificarsi durante l'analisi dell'input penna.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: Enumerazione AnalysisWarningCode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 651408678daa64788952b2706980968ca315abf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313467"
---
# <a name="analysiswarningcode-enumeration"></a><span data-ttu-id="a0e50-103">Enumerazione AnalysisWarningCode</span><span class="sxs-lookup"><span data-stu-id="a0e50-103">AnalysisWarningCode enumeration</span></span>

<span data-ttu-id="a0e50-104">Specifica il set di avvisi disponibili che possono verificarsi durante l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="a0e50-104">Specifies the set of available warnings that can occur during ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e50-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0e50-105">Syntax</span></span>


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a><span data-ttu-id="a0e50-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a0e50-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a0e50-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ interrotto**</span><span class="sxs-lookup"><span data-stu-id="a0e50-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode\_Aborted**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-108">L'operazione di analisi è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="a0e50-108">The analysis operation was aborted.</span></span>

<span data-ttu-id="a0e50-109">Restituito solo quando viene chiamata l'operazione di analisi sincrona.</span><span class="sxs-lookup"><span data-stu-id="a0e50-109">Returned only when the synchronous analysis operation is called.</span></span> <span data-ttu-id="a0e50-110">L'interruzione di un'operazione asincrona non genererà un evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e50-110">Aborting an asynchronous operation will not raise an [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**\_NoMatchingInkAnalysisRecognizerFound AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-112">[**IInkAnalyzer**](iinkanalyzer.md) non è in grado di trovare un riconoscitore Ink che soddisfi i requisiti di linguaggio o funzionalità necessari per eseguire l'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="a0e50-112">The [**IInkAnalyzer**](iinkanalyzer.md) cannot find an ink recognizer that meets language or capability requirements needed to perform the analysis operation.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**\_FactoidNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-114">Il riconoscitore di input penna non è stato in grado di rispettare il set di controllo specificato nel nodo hint di analisi (vedere le proprietà [**IContextNode:: GetType**](icontextnode-gettype.md) e [hint di analisi](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a0e50-114">The ink recognizer was unable to respect the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**\_FactoidCoercionNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidCoercionNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-116">Il riconoscitore di input penna non è riuscito a forzare i risultati nel set di controllo specificato nel nodo hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [proprietà hint di analisi](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a0e50-116">The ink recognizer was unable to coerce its results to the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**\_GuideNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode\_GuideNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-118">Il riconoscimento input penna non è stato in grado di rispettare il set di guide specificato nel nodo hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [proprietà hint di analisi](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a0e50-118">The ink recognizer was unable to respect the specified guide set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**\_WordlistNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode\_WordlistNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-120">Il riconoscitore di input penna non è riuscito a rispettare il set di elenchi di parole specificato nel nodo hint di analisi (vedere le proprietà [**IContextNode:: GetType**](icontextnode-gettype.md) e [hint di analisi](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a0e50-120">The ink recognizer was unable to respect the specified word list set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**\_WordModeNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode\_WordModeNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-122">Il riconoscimento input penna non è stato in grado di rispettare la modalità parola specificata impostata sul nodo hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [proprietà hint di analisi](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a0e50-122">The ink recognizer was unable to respect the specified word mode set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**\_PartialDictionaryTermsNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode\_PartialDictionaryTermsNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-124">Indica che non è stato possibile restituire i termini parziali del dizionario da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="a0e50-124">Indicates that partial dictionary terms could not be returned from the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**\_TextRecognitionProcessFailed AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode\_TextRecognitionProcessFailed**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-126">Indica che il processo di riconoscimento del testo non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a0e50-126">Indicates the text recognition process failed.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**\_AddInkToRecognizerFailed AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode\_AddInkToRecognizerFailed**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-128">Non è stato possibile aggiungere l'input penna a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="a0e50-128">The ink could not be added to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="a0e50-129">Ad esempio, l'aggiunta di tratti raccolti da un mouse su un riconoscitore di movimento avrà esito negativo, perché il riconoscitore di movimento richiede tratti raccolti da un digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="a0e50-129">For example, adding strokes collected from a mouse on a gesture recognizer will fail, as the gesture recognizer requires strokes collected from a digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**\_SetPrefixSuffixFailed AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode\_SetPrefixSuffixFailed**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-131">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non è riuscito a rispettare il prefisso specificato o il testo del suffisso di un nodo hint di analisi (vedere proprietà [**IContextNode:: GetType**](icontextnode-gettype.md) e [hint di analisi](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a0e50-131">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) was unable to respect the specified prefix or suffix text of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**\_InkAnalysisRecognizerInitializationFailed AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-133">[**IInkAnalyzer**](iinkanalyzer.md) non è riuscito a creare un'istanza, clonare o impostare tratti in [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="a0e50-133">The [**IInkAnalyzer**](iinkanalyzer.md) was not able to instantiate, clone, or set strokes on the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**\_ConfirmedWithoutInkRecognition AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode\_ConfirmedWithoutInkRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-135">Indica che un oggetto [**IContextNode**](icontextnode.md) è stato confermato dall'utente senza avere alcun valore di riconoscimento calcolato per il nodo.</span><span class="sxs-lookup"><span data-stu-id="a0e50-135">Indicates that an [**IContextNode**](icontextnode.md) object has been confirmed by the user without having any recognition values computed for the node.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**</span><span class="sxs-lookup"><span data-stu-id="a0e50-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode\_BackgroundException**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-137">Operazione in background non completata a causa di un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a0e50-137">The background operation did not complete due to an exception.</span></span> <span data-ttu-id="a0e50-138">Si tratta di un errore irreversibile e richiede che venga ricreata un'istanza di [**IInkAnalyzer**](iinkanalyzer.md) prima di utilizzarlo di nuovo.</span><span class="sxs-lookup"><span data-stu-id="a0e50-138">This is a fatal error and requires that the [**IInkAnalyzer**](iinkanalyzer.md) is re-instantiated before further use.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**\_ContextNodeLocationNotSet AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode\_ContextNodeLocationNotSet**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-140">Indica che un oggetto [**IContextNode**](icontextnode.md) non dispone di un set di percorsi appropriato (vedere [**IContextNode:: polocation**](icontextnode-setlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="a0e50-140">Indicates that an [**IContextNode**](icontextnode.md) object does not have a proper location set (see [**IContextNode::SetLocation**](icontextnode-setlocation.md)).</span></span> <span data-ttu-id="a0e50-141">Il metodo [**IContextNode:: getLocation**](icontextnode-getlocation.md) deve restituire un valore non vuoto, a meno che l'oggetto **IContextNode** non sia contrassegnato come parzialmente popolato.</span><span class="sxs-lookup"><span data-stu-id="a0e50-141">The [**IContextNode::GetLocation**](icontextnode-getlocation.md) method must return a non-empty value unless the **IContextNode** object is marked as partially populated.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**\_LanguageIdNotRespected AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode\_LanguageIdNotRespected**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-143">L'identificatore di lingua impostato in un tratto associato a un nodo di riconoscimento personalizzato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)) non corrisponde all'identificatore di lingua del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usato.</span><span class="sxs-lookup"><span data-stu-id="a0e50-143">The language identifier set on a stroke associated with a custom recognizer node (see [**IContextNode::GetType**](icontextnode-gettype.md)) did not match the language identifier of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) used.</span></span> <span data-ttu-id="a0e50-144">L'input penna è stato ancora riconosciuto con il **IInkAnalysisRecognizer** specificato.</span><span class="sxs-lookup"><span data-stu-id="a0e50-144">The ink was still recognized with the specified **IInkAnalysisRecognizer**.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**\_EnableUnicodeCharacterRangesNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode\_EnableUnicodeCharacterRangesNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-146">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non supporta l'abilitazione degli intervalli di caratteri Unicode come specificato.</span><span class="sxs-lookup"><span data-stu-id="a0e50-146">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support enabling Unicode character ranges as specified.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**\_TopInkBreaksOnlyNotSupported AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode\_TopInkBreaksOnlyNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-148">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non supporta TopInkBreaks solo se gli hint contengono la richiesta solo per TopInkBreaks.</span><span class="sxs-lookup"><span data-stu-id="a0e50-148">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support TopInkBreaks only even though the hints contained the request for TopInkBreaks only.</span></span>

</dd> <dt>

<span data-ttu-id="a0e50-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**\_AnalysisAlreadyRunning AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode\_AnalysisAlreadyRunning**</span></span>
</dt> <dd>

<span data-ttu-id="a0e50-150">[**IInkAnalyzer**](iinkanalyzer.md) sta già eseguendo l'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="a0e50-150">The [**IInkAnalyzer**](iinkanalyzer.md) is already performing background analysis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0e50-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0e50-151">Remarks</span></span>

<span data-ttu-id="a0e50-152">**AnalysisWarningCode \_ BackgroundException** è l'unico valore del codice di avviso che richiede che venga nuovamente creata un'istanza dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) prima di utilizzare ulteriormente.</span><span class="sxs-lookup"><span data-stu-id="a0e50-152">**AnalysisWarningCode\_BackgroundException** is the only warning code value that requires that the [**IInkAnalyzer**](iinkanalyzer.md) object is re-instantiated before further use.</span></span>

<span data-ttu-id="a0e50-153">Per gli altri valori del codice di avviso, ad esempio **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** e **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, potrebbe essere necessario che l'oggetto [**IInkAnalyzer**](iinkanalyzer.md) usi un riconoscimento diverso.</span><span class="sxs-lookup"><span data-stu-id="a0e50-153">Other warnings code values, such as **AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed** and **AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**, might require that the [**IInkAnalyzer**](iinkanalyzer.md) object use a different recognizer.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e50-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0e50-154">Requirements</span></span>



| <span data-ttu-id="a0e50-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0e50-155">Requirement</span></span> | <span data-ttu-id="a0e50-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a0e50-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e50-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0e50-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e50-158">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a0e50-158">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0e50-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0e50-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e50-160">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a0e50-160">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a0e50-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0e50-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0e50-162"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a0e50-162"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0e50-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0e50-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e50-164">**IAnalysisWarning::GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="a0e50-164">**IAnalysisWarning::GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[<span data-ttu-id="a0e50-165">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a0e50-165">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




