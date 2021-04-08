---
title: Implementazione di un plug-in DSP audio
description: Implementazione di un plug-in DSP audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, implementazione del codice
- Plug-in DSP, implementazione del codice
- plug-in di elaborazione dei segnali digitali, modifica del codice di esempio
- Plug-in DSP, modifica del codice di esempio
- plug-in di elaborazione dei segnali digitali, implementazione audio
- Plug-in DSP, implementazione audio
- plug-in DSP audio, implementazione del codice
- plug-in audio DSP, modifica del codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045031"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementazione di un plug-in DSP audio

Per creare un plug-in Windows Media Player DSP che elabora l'audio, è necessario modificare il codice di esempio nella funzione denominata **DoProcessOutput**. **DoProcessOutput** viene chiamato ogni volta che Windows Media Player chiama correttamente **IMediaObject::P rocessoutput**. Si tratta della funzione che esegue le attività di elaborazione dei segnali digitali che producono il risultato udibile che il plug-in DSP deve produrre.

L'elaborazione di un flusso audio è simile alla gestione di un evento temporizzato. **DoProcessOutput** verrà chiamato ripetutamente e a intervalli specifici. Ogni volta che il codice viene eseguito, sarà necessario elaborare un numero specifico di byte di dati. **DoProcessOutput** contiene i parametri seguenti:



| Parametro          | Descrizione                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Si tratta di un puntatore di **byte** al buffer in cui l'implementazione di **DoProcessOutput** deve copiare i dati elaborati. |
| *pbInputData*      | Puntatore di **byte** costante al buffer che contiene i dati da elaborare.                               |
| *cbBytesToProcess* | Si tratta di un valore **DWORD** che contiene un conteggio del numero di byte nel buffer di input da elaborare.             |



 

Nelle sezioni seguenti vengono fornite informazioni dettagliate su come modificare il codice generato dalla procedura guidata plug-in di Windows Media Player per creare un plug-in di DSP audio personalizzato:

-   [Implementazione di DoProcessOutput](implementing-doprocessoutput.md)
-   [Aggiunta di proprietà al plug-in audio DSP di esempio](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementazione della pagina delle proprietà per un plug-in DSP](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Modifica della proprietà del plug-in audio DSP di esempio](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Informazioni sulla discontinuità](about-discontinuity.md)
-   [Informazioni sull'allocazione delle risorse di streaming](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui plug-in DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




