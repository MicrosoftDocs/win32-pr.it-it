---
description: Consente di eseguire il riconoscimento dell'input penna, recuperare il risultato del riconoscimento e recuperare le alternative. InkRecognizerContext consente ai vari riconoscitori installati in un sistema di usare il riconoscimento dell'input penna per elaborare l'input in modo appropriato.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: Classe InkRecognizerContext (Msinkaut. h)
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
ms.openlocfilehash: afe5469cabf6764ed9b02fdcffcc8c1bedaca1d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231915"
---
# <a name="inkrecognizercontext-class"></a>Classe InkRecognizerContext

Consente di eseguire il riconoscimento dell'input penna, recuperare il risultato del riconoscimento e recuperare le alternative. **InkRecognizerContext** consente ai vari riconoscitori installati in un sistema di usare il riconoscimento dell'input penna per elaborare l'input in modo appropriato.

**InkRecognizerContext** dispone di questi tipi di membri:

-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

La classe **InkRecognizerContext** presenta questi eventi.



| Event                                                                               | Descrizione                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Riconoscimento**](inkrecognizercontext-recognition.md)                             | Si verifica quando InkRecognizerContext ha generato risultati dal metodo BackgroundRecognize.<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Si verifica quando **InkRecognizerContext** genera risultati dopo la chiamata al metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="interfaces"></a>Interfacce

La classe **InkRecognizerContext** definisce queste interfacce.



| Interfaccia                 | Descrizione                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkRecognizerContext** | Questo oggetto implementa l'interfaccia com **IInkRecognizerContext** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkRecognizerContext** dispone di questi metodi.



| Metodo                                                                                              | Descrizione                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Specifica che il riconoscimento deve riconoscere i tratti associati e generare un evento di [**riconoscimento**](inkrecognizercontext-recognition.md) quando il riconoscimento è completo.<br/>                                                                |
| [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Specifica che il riconoscimento deve riconoscere i tratti associati e generare un evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) quando il riconoscimento è completo.<br/>                                    |
| [**Clone**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Crea un **InkRecognizerContext** duplicato.<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Termina l'input penna in **InkRecognizerContext**.<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Indica se il dizionario di sistema, il dizionario utente o l' [**elenco di parole**](inkwordlist-class.md) contengono una stringa specificata.<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Esegue il riconoscimento su una raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e restituisce i risultati del riconoscimento.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Termina il riconoscimento in background avviato con una chiamata a [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) o [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates).<br/> |



 

### <a name="properties"></a>Proprietà

La classe **InkRecognizerContext** dispone di queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la modalità di completamento automatico dei caratteri, che determina quando vengono riconosciuti i caratteri o le parole.<br/>                                         |
| [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Lettura/Scrittura<br/> | Ottiene o imposta il nome di stringa del controllo oggetto utilizzato dall'oggetto **InkRecognizerContext** .<br/>                                                        |
| [**Guida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Lettura/Scrittura<br/> | Ottiene o imposta il [**InkRecognizerGuide**](inkrecognizerguide-class.md) da utilizzare per l'input penna.<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta i caratteri che precedono la raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) nell'oggetto **InkRecognizerContext** .<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta i flag che specificano il modo in cui il riconoscimento interpreta l'input penna e determina la stringa di risultato.<br/>                                     |
| [**Sistema di riconoscimento**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) utilizzato dall'oggetto **InkRecognizerContext** .<br/>                                   |
| [**Tratti**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Lettura/Scrittura<br/> | Ottiene o imposta la raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) associata all'oggetto **InkRecognizerContext** .<br/>                    |
| [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta i caratteri che derivano dalla raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) nell'oggetto **InkRecognizerContext** .<br/>  |
| [**Elenco delle parole**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto [**InkWord**](inkwordlist-class.md) utilizzato per migliorare i risultati del riconoscimento.<br/>                               |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

Esistono due tipi di riconoscimento: background (asincrono) o Foreground (sincrono). Il riconoscimento in background viene avviato da una chiamata ai metodi [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) o [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) , si verifica in un thread in background e segnala i risultati all'applicazione tramite un meccanismo di evento. Il riconoscimento in primo piano non restituisce alcun risultato finché non viene completato tutto il riconoscimento, rendendo quindi disponibili i risultati del riconoscimento al thread chiamante senza attendere l'evento di riconoscimento.

L'input penna viene elaborato in modo continuo in background. Se un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) viene aggiunto alla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) a cui fa riferimento **InkRecognizerContext** , il **IInkStrokeDisp** viene quindi riconosciuto immediatamente. Per ulteriori informazioni, vedere la sezione osservazioni nell'argomento del metodo [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) .

Tutti i riconoscimenti avvengono tramite un contesto di riconoscimento. Il contesto definisce le impostazioni per una singola sessione di riconoscimento. Riceve l'input penna che deve essere riconosciuto e definisce i vincoli sull'input input penna e sull'output del riconoscimento. I vincoli che è possibile impostare nel contesto includono il linguaggio, il dizionario e la grammatica utilizzata.

> [!Note]  
> L'impostazione di proprietà diverse dalle proprietà [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) o [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) ha esito positivo solo se la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) è **null**. È necessario impostare le altre proprietà prima di allineare la raccolta InkStrokes a **InkRecognizerContext** oppure è necessario impostare la raccolta InkStrokes su **null** e quindi impostare le altre proprietà. Se si imposta la raccolta InkStrokes su **null** e quindi si impostano le altre proprietà, potrebbe essere necessario allineare la raccolta InkStrokes. Questo perché il riconoscimento viene avviato subito dopo l'assegnazione di InkStrokes a **InkRecognizerContext**. Quando viene effettuata una chiamata per [**riconoscere il metodo \[ InkRecognizeContext \] Class**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) o [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize), i risultati della chiamata potrebbero essere già disponibili.

 

Per migliorare le prestazioni dell'applicazione, eliminare l'oggetto **InkRecognizerContext** quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

