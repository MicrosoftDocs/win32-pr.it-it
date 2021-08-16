---
title: Implementazione di un plug-in DSP audio
description: Implementazione di un plug-in DSP audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Windows Media Player plug-in, DSP audio
- plug-in, DSP audio
- plug-in di elaborazione del segnale digitale, implementazione di codice
- plug-in DSP, implementazione di codice
- plug-in di elaborazione del segnale digitale, modifica del codice di esempio
- plug-in DSP, modifica del codice di esempio
- plug-in di elaborazione del segnale digitale, implementazione audio
- Plug-in DSP, implementazione audio
- plug-in DSP audio,implementazione di codice
- plug-in DSP audio, modifica del codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f18ca0aada7072ca7cd1c0796c3cd6770a9b45340a4d9f67a342944f4c22887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338642"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementazione di un plug-in DSP audio

Per creare Windows Media Player plug-in DSP che elabora l'audio, è necessario modificare il codice di esempio nella funzione denominata **DoProcessOutput**. **DoProcessOutput** viene chiamato ogni volta Windows Media Player chiama **correttamente IMediaObject::P rocessOutput**. È la funzione che esegue le attività di elaborazione del segnale digitale che producono il risultato udibile che il plug-in DSP è destinato a produrre.

L'elaborazione di un flusso audio è simile alla gestione di un evento a tempo. **DoProcessOutput** verrà chiamato ripetutamente e a intervalli specifici. Ogni volta che il codice viene eseguito, sarà necessario elaborare un numero specifico di byte di dati. **DoProcessOutput** contiene i parametri seguenti:



| Parametro          | Descrizione                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Si tratta di un **puntatore BYTE** al buffer in cui l'implementazione **di DoProcessOutput** deve copiare i dati elaborati. |
| *pbInputData*      | Si tratta di un **puntatore BYTE** costante al buffer che contiene i dati da elaborare.                               |
| *cbBytesToProcess* | Si tratta di **un valore DWORD** che contiene un conteggio del numero di byte nel buffer di input da elaborare.             |



 

Le sezioni seguenti forniscono informazioni dettagliate su come modificare il codice generato dalla creazione guidata plug-in Windows Media Player per creare un plug-in DSP audio personalizzato:

-   [Implementazione di DoProcessOutput](implementing-doprocessoutput.md)
-   [Aggiunta di proprietà al plug-in Audio DSP di esempio](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementazione della pagina delle proprietà per un plug-in DSP](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Modifica della proprietà del plug-in Audio DSP di esempio](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Informazioni sulla discontinuità](about-discontinuity.md)
-   [Informazioni sull'allocazione di risorse di streaming](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui plug-in DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




