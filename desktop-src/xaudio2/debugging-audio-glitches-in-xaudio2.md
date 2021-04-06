---
description: Le anomalie possono verificarsi in XAudio2, in questo argomento vengono illustrate le modalità di segnalazione e alcuni approcci per correggerli.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Debug di glitch audio in XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883138"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Debug di glitch audio in XAudio2

Le anomalie possono verificarsi in XAudio2, in questo argomento vengono illustrate le modalità di segnalazione e alcuni approcci per correggerli.

Questa panoramica illustra gli argomenti seguenti:

-   [Cause di problemi di output audio o glitch](#causes-of-audio-output-problems-or-glitches)
-   [Come XAudio2 segnala i problemi](#how-xaudio2-reports-problems)
-   [Approcci alla risoluzione dei problemi](#approaches-to-fixing-problems)
-   [Argomenti correlati](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Cause di problemi di output audio o glitch

Per diversi motivi, è possibile che si verifichino problemi nell'output di XAudio2.

-   Una voce di origine XAudio2 è affamata. Il client non invia audio aggiornato in modo sufficientemente rapido. Si ottiene il silenzio perché non sono disponibili dati da riprodurre.
-   Il XAudio2 nel suo complesso è sovraccarico. Sono necessari più di *x* MS per produrre *x* MS di audio. Si ottengono forcelle perché XAudio2 non può produrre dati con la stessa velocità con cui il dispositivo audio lo richiede. È possibile che si stiano eseguendo troppe voci o effetti per volta, eseguendo troppe operazioni nei callback XAudio2 o eseguendo troppo spesso chiamate API XAudio2.
-   Il thread di elaborazione audio è bloccato perché l'implementazione del client di un callback XAudio2 sta eseguendo operazioni che possono bloccare il thread. Ad esempio, potrebbe accedere al disco, sincronizzarsi con altri thread o chiamare altre funzioni che potrebbero bloccarsi. Usare un thread in background con priorità bassa che il callback può segnalare per eseguire tali attività.
-   Il sistema nel suo complesso è sovraccarico. Gli altri thread in esecuzione con una priorità uguale o superiore a quella di XAudio2 eseguono troppe operazioni. Sono in competizione con il thread audio per il tempo di CPU.

## <a name="how-xaudio2-reports-problems"></a>Come XAudio2 segnala i problemi

XAudio2 può comunicare le anomalie nella compilazione di debug in diversi modi.

-   Se una voce sta per esaurirsi, XAudio2 Visualizza un messaggio in questo formato.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Se il thread audio viene eseguito per troppo tempo, XAudio2 Visualizza un messaggio in questo formato.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    In genere, questo messaggio viene visualizzato con il messaggio successivo.

-   Se non è possibile alimentare i nuovi dati audio in un driver audio, XAudio2 Visualizza un messaggio in questo modulo.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   La chiamata di [**IXAudio2:: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fornisce dati sulle prestazioni di XAudio2, incluso il numero totale di glitch dall'avvio del motore XAudio2.

## <a name="approaches-to-fixing-problems"></a>Approcci alla risoluzione dei problemi

Di seguito sono riportati i possibili modi per ridurre i problemi di audio.

-   Nel caso di inedia vocale: aumentare la quantità di dati audio accodati in avanti su una voce. È possibile usare [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) per individuare il numero di buffer accodati in qualsiasi momento. Se si verificano ancora errori di inedia vocale, ma non è possibile udire alcun problema, assicurarsi di impostare il [**\_ buffer di XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flag** per XAUDIO2 \_ \_ la fine del \_ flusso sul buffer finale di un suono. Ciò indica a XAudio2 di non prevedere che altri buffer siano necessariamente disponibili non appena questo viene completato.

    Negli altri casi:

    -   Ridurre il numero di voci attive ed effetti nel grafico, soprattutto gli effetti costosi come il riverbero.
    -   Disabilitare le voci e gli effetti che non si sta usando.
    -   Usare i \_ flag XAUDIO2 Voice \_ NOSRC e XAUDIO2 \_ Voice \_ nopitch in [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), quando possibile. La conversione della frequenza di campionamento è costosa.
    -   Ridurre la frequenza di campionamento delle singole voci. Ad esempio, una voce submix che ospita un effetto di riverbero può avere una frequenza di campionamento inferiore rispetto a quella di origine che invia alla voce. I suoni come le esplosioni e gli spari che non necessitano di fedeltà elevata possono essere registrati anche a tariffe di campionamento inferiori.
    -   Assicurarsi che le implementazioni di callback eseguano il minor lavoro possibile e mai si blocchino.
    -   Effettuare un minor numero di chiamate a XAudio2. In genere non è necessario aggiornare i parametri audio per ogni fotogramma video. Ogni 30 ms è sufficiente. È consigliabile eliminare le chiamate ridondanti, ad esempio impostando il volume più volte in rapida successione.
    -   Ridurre l'utilizzo complessivo della CPU del gioco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di debug](debugging-facilities.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 
