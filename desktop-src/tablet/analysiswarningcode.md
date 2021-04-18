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
# <a name="analysiswarningcode-enumeration"></a>Enumerazione AnalysisWarningCode

Specifica il set di avvisi disponibili che possono verificarsi durante l'analisi dell'input penna.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ interrotto**
</dt> <dd>

L'operazione di analisi è stata interrotta.

Restituito solo quando viene chiamata l'operazione di analisi sincrona. L'interruzione di un'operazione asincrona non genererà un evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**\_NoMatchingInkAnalysisRecognizerFound AnalysisWarningCode**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) non è in grado di trovare un riconoscitore Ink che soddisfi i requisiti di linguaggio o funzionalità necessari per eseguire l'operazione di analisi.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**\_FactoidNotSupported AnalysisWarningCode**
</dt> <dd>

Il riconoscitore di input penna non è stato in grado di rispettare il set di controllo specificato nel nodo hint di analisi (vedere le proprietà [**IContextNode:: GetType**](icontextnode-gettype.md) e [hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**\_FactoidCoercionNotSupported AnalysisWarningCode**
</dt> <dd>

Il riconoscitore di input penna non è riuscito a forzare i risultati nel set di controllo specificato nel nodo hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [proprietà hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**\_GuideNotSupported AnalysisWarningCode**
</dt> <dd>

Il riconoscimento input penna non è stato in grado di rispettare il set di guide specificato nel nodo hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [proprietà hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**\_WordlistNotSupported AnalysisWarningCode**
</dt> <dd>

Il riconoscitore di input penna non è riuscito a rispettare il set di elenchi di parole specificato nel nodo hint di analisi (vedere le proprietà [**IContextNode:: GetType**](icontextnode-gettype.md) e [hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**\_WordModeNotSupported AnalysisWarningCode**
</dt> <dd>

Il riconoscimento input penna non è stato in grado di rispettare la modalità parola specificata impostata sul nodo hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [proprietà hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**\_PartialDictionaryTermsNotSupported AnalysisWarningCode**
</dt> <dd>

Indica che non è stato possibile restituire i termini parziali del dizionario da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**\_TextRecognitionProcessFailed AnalysisWarningCode**
</dt> <dd>

Indica che il processo di riconoscimento del testo non è riuscito.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**\_AddInkToRecognizerFailed AnalysisWarningCode**
</dt> <dd>

Non è stato possibile aggiungere l'input penna a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Ad esempio, l'aggiunta di tratti raccolti da un mouse su un riconoscitore di movimento avrà esito negativo, perché il riconoscitore di movimento richiede tratti raccolti da un digitalizzatore.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**\_SetPrefixSuffixFailed AnalysisWarningCode**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non è riuscito a rispettare il prefisso specificato o il testo del suffisso di un nodo hint di analisi (vedere proprietà [**IContextNode:: GetType**](icontextnode-gettype.md) e [hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**\_InkAnalysisRecognizerInitializationFailed AnalysisWarningCode**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) non è riuscito a creare un'istanza, clonare o impostare tratti in [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**\_ConfirmedWithoutInkRecognition AnalysisWarningCode**
</dt> <dd>

Indica che un oggetto [**IContextNode**](icontextnode.md) è stato confermato dall'utente senza avere alcun valore di riconoscimento calcolato per il nodo.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**
</dt> <dd>

Operazione in background non completata a causa di un'eccezione. Si tratta di un errore irreversibile e richiede che venga ricreata un'istanza di [**IInkAnalyzer**](iinkanalyzer.md) prima di utilizzarlo di nuovo.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**\_ContextNodeLocationNotSet AnalysisWarningCode**
</dt> <dd>

Indica che un oggetto [**IContextNode**](icontextnode.md) non dispone di un set di percorsi appropriato (vedere [**IContextNode:: polocation**](icontextnode-setlocation.md)). Il metodo [**IContextNode:: getLocation**](icontextnode-getlocation.md) deve restituire un valore non vuoto, a meno che l'oggetto **IContextNode** non sia contrassegnato come parzialmente popolato.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**\_LanguageIdNotRespected AnalysisWarningCode**
</dt> <dd>

L'identificatore di lingua impostato in un tratto associato a un nodo di riconoscimento personalizzato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)) non corrisponde all'identificatore di lingua del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usato. L'input penna è stato ancora riconosciuto con il **IInkAnalysisRecognizer** specificato.

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**\_EnableUnicodeCharacterRangesNotSupported AnalysisWarningCode**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non supporta l'abilitazione degli intervalli di caratteri Unicode come specificato.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**\_TopInkBreaksOnlyNotSupported AnalysisWarningCode**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non supporta TopInkBreaks solo se gli hint contengono la richiesta solo per TopInkBreaks.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**\_AnalysisAlreadyRunning AnalysisWarningCode**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) sta già eseguendo l'analisi in background.

</dd> </dl>

## <a name="remarks"></a>Commenti

**AnalysisWarningCode \_ BackgroundException** è l'unico valore del codice di avviso che richiede che venga nuovamente creata un'istanza dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) prima di utilizzare ulteriormente.

Per gli altri valori del codice di avviso, ad esempio **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** e **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, potrebbe essere necessario che l'oggetto [**IInkAnalyzer**](iinkanalyzer.md) usi un riconoscimento diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




