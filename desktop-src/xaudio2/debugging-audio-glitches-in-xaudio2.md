---
description: Glitch possono verificarsi in XAudio2. Questo argomento illustra come vengono segnalati e alcuni approcci per correggerli.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Debug di glitch audio in XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8856defc67bc9453b9d83f5ed369bfb96f48b8c2c16c92ea535a0c1b648402b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703621"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Debug di glitch audio in XAudio2

Glitch possono verificarsi in XAudio2. Questo argomento illustra come vengono segnalati e alcuni approcci per correggerli.

Questa panoramica illustra gli argomenti seguenti:

-   [Cause di problemi o problemi di output audio](#causes-of-audio-output-problems-or-glitches)
-   [Come XAudio2 segnala i problemi](#how-xaudio2-reports-problems)
-   [Approcci alla risoluzione dei problemi](#approaches-to-fixing-problems)
-   [Argomenti correlati](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Cause di problemi o problemi di output audio

Gli errori possono verificarsi nell'output di XAudio2 per diversi motivi.

-   Una voce di origine XAudio2 è affamata. Il client non invia audio nuovo ad esso abbastanza velocemente. Si ottiene il silenzio perché non ha dati da riprodurre.
-   XAudio2 nel suo complesso è sovraccarico. La produzione di *X* ms di audio richiede più tempo di *X* ms. Si ottengono dropout perché XAudio2 non può produrre dati alla velocità del dispositivo audio necessario. È possibile che si stiano eseguendo troppe voci o effetti contemporaneamente, che si stiano eseguendo troppe operazioni nei callback XAudio2 o che si esercitino chiamate API XAudio2 con una frequenza troppo frequente.
-   Il thread di elaborazione audio è in fase di stallo perché l'implementazione del client di un callback XAudio2 sta eseguendo operazioni che possono bloccare il thread. Ad esempio, potrebbe accedere al disco, sincronizzarsi con altri thread o chiamare altre funzioni che potrebbero bloccarsi. Usare un thread in background con priorità inferiore che il callback può segnalare per eseguire tali attività.
-   Il sistema nel suo complesso è sottoposto a overload. Altri thread in esecuzione con la stessa priorità o con priorità superiore a XAudio2 eseguono un numero troppo elevato di operazioni. Sono in competizione con il thread audio per il tempo di CPU.

## <a name="how-xaudio2-reports-problems"></a>Come XAudio2 segnala i problemi

XAudio2 può comunicare gli errori nella build di debug in diversi modi.

-   Se una voce viene affamata, XAudio2 visualizza un messaggio in questo formato.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Se il thread audio viene eseguito per troppo tempo, XAudio2 visualizza un messaggio in questo formato.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    In genere, questo messaggio viene visualizzato con il messaggio successivo.

-   Se non è possibile inviare in tempo nuovi dati audio al driver audio, XAudio2 visualizza un messaggio in questo formato.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   La [**chiamata di IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fornisce dati sulle prestazioni di XAudio2, incluso il numero totale di problemi dall'avvio del motore XAudio2.

## <a name="approaches-to-fixing-problems"></a>Approcci alla risoluzione dei problemi

Di seguito sono riportati i modi possibili per ridurre i problemi audio.

-   Nel caso di carestia vocale: aumentare la quantità di dati audio accodati in anticipo su una voce. È possibile usare [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) per individuare il numero di buffer accodati in qualsiasi momento. Se vengono ancora visualizzati errori di carestia vocale, ma non si è in grado di ascoltare alcun problema, assicurarsi di impostare [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flag** per XAUDIO2 \_ END OF STREAM nel buffer finale di un \_ \_ suono. Questo indica a XAudio2 di non aspettarsi che altri buffer siano necessariamente disponibili non appena questo viene completato.

    Negli altri casi:

    -   Ridurre il numero di voci ed effetti attivi nel grafico, in particolare gli effetti costosi come il riverbero.
    -   Disabilitare voci ed effetti non in uso.
    -   Usare i flag XAUDIO2 \_ VOICE \_ NOSRC e XAUDIO2 \_ VOICE \_ NOPITCH in [**IXAudio2::CreateSourceVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)quando possibile. La conversione della frequenza di campionamento è disasserta.
    -   Ridurre la frequenza di campionamento delle singole voci. Ad esempio, una voce submix che ospita un effetto riverbero può avere una frequenza di campionamento inferiore rispetto alla voce di origine che vi invia. Anche suoni come esplosioni e spari che non necessitano di alta fedeltà possono essere registrati a frequenze di campionamento inferiori.
    -   Assicurarsi che le implementazioni di callback funzionino il meno possibile e non si blocchino mai.
    -   Effettuare meno chiamate a XAudio2. I parametri audio in genere non devono essere aggiornati per ogni fotogramma video. Ogni 30 ms è sufficiente. È consigliabile eliminare le chiamate ridondanti, ad esempio impostare il volume più volte in rapida successione.
    -   Ridurre l'utilizzo complessivo della CPU del gioco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di debug](debugging-facilities.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 
