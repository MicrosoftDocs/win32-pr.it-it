---
description: Specifica il set di avvisi disponibili che possono verificarsi durante l'analisi dell'input penna.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: Enumerazione AnalysisWarningCode (IACom.h)
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
ms.openlocfilehash: 48d03c0f4c479ddf6a3f1f9f371bc13b889641994f86df75b107b17ca081a97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660871"
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

Restituito solo quando viene chiamata l'operazione di analisi sincrona. L'interruzione di un'operazione asincrona non genererà un evento [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) non riesce a trovare un riconoscimento input penna che soddisfi i requisiti di lingua o funzionalità necessari per eseguire l'operazione di analisi.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**
</dt> <dd>

Il riconoscimento input penna non è stato in grado di rispettare il factoid specificato impostato nel nodo dell'hint di analisi (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e [Proprietà hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**
</dt> <dd>

Il riconoscimento input penna non è riuscito a forzare i risultati al factoid specificato impostato nel nodo dell'hint di analisi (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e [Proprietà hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**Guida di \_ AnalysisWarningCodeNotSupported**
</dt> <dd>

Il riconoscimento input penna non è stato in grado di rispettare la guida specificata impostata nel nodo dell'hint di analisi (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e [Proprietà hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**
</dt> <dd>

Il riconoscimento input penna non è stato in grado di rispettare l'elenco di parole specificato impostato nel nodo dei suggerimenti di analisi (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e [Proprietà hint di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**
</dt> <dd>

Il riconoscimento input penna non è stato in grado di rispettare la modalità parola specificata impostata nel nodo dei suggerimenti di analisi (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e Proprietà hint [di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**
</dt> <dd>

Indica che non è stato possibile restituire termini parziali del dizionario da [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**
</dt> <dd>

Indica che il processo di riconoscimento del testo non è riuscito.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**
</dt> <dd>

Impossibile aggiungere l'input penna a [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md) Ad esempio, l'aggiunta di tratti raccolti da un mouse su un riconoscitore movimento avrà esito negativo, perché il riconoscimento movimenti richiede tratti raccolti da un digitalizzatore.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non è stato in grado di rispettare il prefisso o il testo del suffisso specificato di un nodo hint di analisi (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e Proprietà hint [di analisi](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) non è stato in grado di creare un'istanza, clonare o impostare tratti in [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**
</dt> <dd>

Indica che un [**oggetto IContextNode**](icontextnode.md) è stato confermato dall'utente senza che siano stati calcolati valori di riconoscimento per il nodo.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**
</dt> <dd>

L'operazione in background non è stata completata a causa di un'eccezione. Si tratta di un errore irreversibile e richiede che venga creata di nuovo un'istanza di [**IInkAnalyzer**](iinkanalyzer.md) prima di un ulteriore utilizzo.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**
</dt> <dd>

Indica che per un [**oggetto IContextNode**](icontextnode.md) non è impostata una posizione appropriata (vedere [**IContextNode::SetLocation**](icontextnode-setlocation.md)). Il [**metodo IContextNode::GetLocation**](icontextnode-getlocation.md) deve restituire un valore non vuoto a meno che l'oggetto **IContextNode** non sia contrassegnato come parzialmente popolato.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**LanguageIdNotRespected di AnalysisWarningCode \_**
</dt> <dd>

L'identificatore di lingua impostato su un tratto associato a un nodo di riconoscimento personalizzato (vedere [**IContextNode::GetType)**](icontextnode-gettype.md)non corrisponde all'identificatore della lingua [**dell'oggetto IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usato. L'input penna è stato ancora riconosciuto con **l'oggetto IInkAnalysisRecognizer specificato.**

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non supporta l'abilitazione di intervalli di caratteri Unicode come specificato.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) non supporta TopInkBreaks solo se gli hint contenevano solo la richiesta per TopInkBreaks.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**
</dt> <dd>

[**IInkAnalyzer sta**](iinkanalyzer.md) già eseguendo l'analisi in background.

</dd> </dl>

## <a name="remarks"></a>Commenti

**AnalysisWarningCode \_ BackgroundException è** l'unico valore di codice di avviso che richiede la nuova istanza dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) prima di un ulteriore utilizzo.

Altri valori del codice degli avvisi, ad esempio **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** e **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound,** potrebbero richiedere che l'oggetto [**IInkAnalyzer**](iinkanalyzer.md) usi un sistema di riconoscimento diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




