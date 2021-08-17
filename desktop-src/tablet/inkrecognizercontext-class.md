---
description: Consente di eseguire il riconoscimento input penna, recuperare il risultato del riconoscimento e recuperare le alternative. InkRecognizerContext consente ai vari sistemi di riconoscimento installati in un sistema di usare il riconoscimento input penna per elaborare l'input in modo appropriato.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: Classe InkRecognizerContext (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 781d1b440f1287b22d5c3ddf7ecf7132f7311fc5f48da5da20e4145717f65bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218402"
---
# <a name="inkrecognizercontext-class"></a>Classe InkRecognizerContext

Consente di eseguire il riconoscimento input penna, recuperare il risultato del riconoscimento e recuperare le alternative. **InkRecognizerContext** consente ai vari sistemi di riconoscimento installati in un sistema di usare il riconoscimento input penna per elaborare l'input in modo appropriato.

**InkRecognizerContext** ha questi tipi di membri:

-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

La **classe InkRecognizerContext** include questi eventi.



| Event                                                                               | Descrizione                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Riconoscimento**](inkrecognizercontext-recognition.md)                             | Si verifica quando InkRecognizerContext ha generato risultati dal metodo BackgroundRecognize.<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Si verifica quando **InkRecognizerContext ha** generato risultati dopo la chiamata al metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="interfaces"></a>Interfacce

La **classe InkRecognizerContext** definisce queste interfacce.



| Interfaccia                 | Descrizione                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkRecognizerContext** | Questo oggetto implementa **l'interfaccia COM IInkRecognizerContext.**<br/> |



 

### <a name="methods"></a>Metodi

La **classe InkRecognizerContext** include questi metodi.



| Metodo                                                                                              | Descrizione                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Specifica che il riconoscimento deve riconoscere i tratti associati e genera un [**evento Recognition**](inkrecognizercontext-recognition.md) al termine del riconoscimento.<br/>                                                                |
| [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Specifica che il riconoscimento deve riconoscere i tratti associati e genera un [**evento RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) al termine del riconoscimento.<br/>                                    |
| [**Clone**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Crea un **oggetto InkRecognizerContext duplicato.**<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Termina l'input penna **per InkRecognizerContext.**<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Indica se il dizionario di sistema, il dizionario utente o l'elenco [**di parole**](inkwordlist-class.md) contengono una stringa specificata.<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Esegue il riconoscimento su una [**raccolta InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e restituisce i risultati del riconoscimento.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Termina il riconoscimento in background avviato con una chiamata a [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) o [**BackgroundRecognizeWithAlternates.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="properties"></a>Proprietà

La **classe InkRecognizerContext** ha queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la modalità di completamento automatico dei caratteri, che determina quando vengono riconosciuti i caratteri o le parole.<br/>                                         |
| [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Lettura/Scrittura<br/> | Ottiene o imposta il nome stringa del factoid usato **dall'oggetto InkRecognizerContext.**<br/>                                                        |
| [**Guida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Lettura/Scrittura<br/> | Ottiene o imposta [**l'oggetto InkRecognizerGuide**](inkrecognizerguide-class.md) da usare per l'input penna.<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta i caratteri che vengono prima della [**raccolta InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) nell'oggetto **InkRecognizerContext.**<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta i flag che specificano come il riconoscimento interpreta l'input penna e determina la stringa di risultato.<br/>                                     |
| [**Riconoscimento**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta [**l'oggetto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) usato **dall'oggetto InkRecognizerContext.**<br/>                                   |
| [**Tratti**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Lettura/Scrittura<br/> | Ottiene o imposta la [**raccolta InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) associata all'oggetto **InkRecognizerContext.**<br/>                    |
| [**Suffixtext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta i caratteri che vengono dopo la [**raccolta InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) nell'oggetto **InkRecognizerContext.**<br/>  |
| [**Wordlist**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Lettura/Scrittura<br/> | Ottiene o imposta [**l'oggetto InkWordList**](inkwordlist-class.md) utilizzato per migliorare i risultati del riconoscimento.<br/>                               |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

Esistono due tipi di riconoscimento: in background (asincrono) o in primo piano (sincrono). Il riconoscimento in background viene avviato da una chiamata ai metodi [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) o [**BackgroundRecognizeWithAlternates,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) si verifica in un thread in background e segnala i risultati all'applicazione tramite un meccanismo di eventi. Il riconoscimento in primo piano non restituisce alcun risultato fino al completamento di tutti i riconoscimenti, rendendo così disponibili i risultati del riconoscimento al thread chiamante senza attendere l'evento di riconoscimento.

L'input penna viene elaborato continuamente in background. Se viene [**aggiunto un oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) alla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) a cui fa riferimento **InkRecognizerContext,** **l'oggetto IInkStrokeDisp** viene riconosciuto immediatamente. Per altri dettagli, vedere la sezione [**osservazioni nell'argomento Metodo EndInkInput.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)

Tutto il riconoscimento avviene tramite un contesto di riconoscimento. Il contesto definisce le impostazioni per una singola sessione di riconoscimento. Riceve l'input penna che deve essere riconosciuto e definisce i vincoli sull'input penna e sull'output di riconoscimento. I vincoli che possono essere impostati nel contesto includono la lingua, il dizionario e la grammatica in uso.

> [!Note]  
> L'impostazione di proprietà [**diverse da Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) o [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) ha esito positivo solo se la [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) è **NULL.** È necessario impostare le altre proprietà prima di collegare la raccolta InkStrokes a **InkRecognizerContext** oppure è necessario impostare la raccolta InkStrokes su **NULL** e quindi impostare le altre proprietà. Se si imposta la raccolta InkStrokes su **NULL** e quindi si impostano le altre proprietà, potrebbe essere necessario ricollegare la raccolta InkStrokes. Questo perché il riconoscimento inizia subito dopo l'assegnazione di InkStrokes a **InkRecognizerContext.** Quando viene effettuata una chiamata al metodo [**\[ Recognize \] InkRecognizeContext Class**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) o [**BackgroundRecognize,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)i risultati della chiamata potrebbero essere già disponibili.

 

Per migliorare le prestazioni dell'applicazione, eliminare **l'oggetto InkRecognizerContext** quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

