---
description: XAudio2 è un'API audio di basso livello. Fornisce una base per l'elaborazione e la combinazione dei segnali per i giochi simili ai predecessori, DirectSound e XAudio.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: Introduzione a XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7cde958256d9126746a07764dc0c792e88289c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319074"
---
# <a name="xaudio2-introduction"></a>Introduzione a XAudio2

XAudio2 è un'API audio di basso livello. Fornisce una base per l'elaborazione e la combinazione dei segnali per i giochi simili ai predecessori, DirectSound e XAudio.

XAudio2 è la sostituzione molto attesa per DirectSound. Risolve diversi problemi e richieste di funzionalità in attesa.

## <a name="xaudio2-features"></a>Funzionalità di XAudio2

Di seguito è riportato un elenco di funzionalità XAudio2 e nuove funzionalità che consentono agli sviluppatori di migliorare le prestazioni nei giochi.

-   Effetti DSP e filtro per voce

    Gli effetti del Digital Signal Processing (DSP) sono i pixel shader dell'audio. Gestiscono tutti gli elementi dalla trasformazione di un suono, trasformando un Pig strillo in un basso, spaventoso mostro, per inserire i suoni nell'ambiente del gioco usando il filtro di riverbero e occlusione o ostruzione. XAudio2 fornisce un Framework DSP flessibile e potente. Fornisce anche un filtro incorporato su ogni voce, per effetti di filtro efficienti Low/High o di fascia passa.

    Per ulteriori informazioni sugli effetti DSP e sul filtro vocale, vedere [XAudio2 Audio Effects](xaudio2-audio-effects.md) e [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) .

-   Sottocombinazione

    La sottocombinazione combina diversi suoni in un singolo flusso audio, ad esempio un suono del motore costituito da parti composite, che giocano tutti simultaneamente. Inoltre, è possibile utilizzare la combinazione di combinazioni per elaborare e combinare parti simili di un gioco. È ad esempio possibile combinare tutti gli effetti audio del gioco per consentire l'applicazione di un'impostazione del volume utente mentre un'impostazione separata controlla il volume musicale. In combinazione con DSP, la sottocombinazione fornisce il tipo di routing e elaborazione dei dati necessari per i giochi odierni. XAudio2 consente livelli arbitrari di Submixaggio, consentendo la creazione di suoni complessi e miscele di gioco.

    Vedere [XAudio2 audio Graph](xaudio2-audio-graph.md) e [XAudio2 Voices](xaudio2-voices.md) per altre informazioni sulla sottocombinazione.

-   Supporto audio compresso

    Una delle principali richieste di funzionalità per DirectSound è stata per il supporto audio compresso. XAudio2 supporta formati compressi, ADPCM, in modo nativo con la decompressione in fase di esecuzione.

-   Supporto migliorato multicanale e audio surround

    Il supporto per l'audio multicanale, 3D e surround è stato espanso. i suoni 3D e surround sono ora molto più flessibili e trasparenti. XAudio2 rimuove il limite di 6 canali sui suoni multicanale e supporta l'audio multicanale su qualsiasi scheda audio con supporto multicanale. Non è necessario che la scheda sia con accelerazione hardware.

-   Elaborazione multitasso

    Per ridurre al minimo l'utilizzo della CPU, XAudio2 offre la tecnologia per creare più grafici di elaborazione audio a bassa frequenza. Questo può ridurre significativamente l'utilizzo della CPU consentendo a un gioco di elaborare l'audio alla velocità del materiale di origine se la velocità è inferiore a 48 kHz.

-   Modello API non di blocco

    Con poche eccezioni, una chiamata al metodo XAudio2 non bloccherà il motore di elaborazione audio. Ciò significa che un client può eseguire in modo sicuro un set di chiamate al metodo in qualsiasi momento senza bloccare le chiamate con esecuzione prolungata che causano ritardi. Le eccezioni sono il metodo [**IXAudio2Voice::D estroyvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) (che può bloccare il motore fino a quando non viene terminata l'elaborazione della voce) e i metodi che terminano il thread audio: [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) e [**IXAudio2:: Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Si noti che, mentre le chiamate al metodo XAudio2 non bloccano il motore di elaborazione audio, i metodi XAudio2 contengono sezioni critiche e possono essere bloccati in alcune circostanze.

## <a name="when-to-use-xaudio2"></a>Quando usare XAudio2

XAudio2 è progettato principalmente per lo sviluppo di motori audio a prestazioni elevate per i giochi. Per gli sviluppatori di giochi che voglio aggiungere effetti audio e musica di sottofondo ai propri giochi, XAudio2 offre un motore di missaggio e grafico audio a bassa latenza con supporto per buffer dinamici, riproduzione sincrona dei campioni e conversione implicita della frequenza di origine. Rispetto a WASAPI, XAudio2 richiede solo una quantità minima di codice anche per soluzioni audio complesse. Rispetto al motore di Media Foundation, XAudio2 è un'API C++ a bassa latenza di basso livello progettata per l'uso nei giochi.

Per le applicazioni che richiedono semplicemente la riproduzione di musica normale, il motore di Media Foundation può essere una corrispondenza migliore con i requisiti dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 
