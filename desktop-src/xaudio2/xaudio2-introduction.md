---
description: XAudio2 è un'API audio di basso livello. Fornisce un'elaborazione del segnale e la combinazione di basi per giochi simili ai predecessori, DirectSound e XAudio.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: Introduzione a XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a966e9682a7f605864c0374a588d4b7eb3724036fe284bd6d92c64080e9225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589901"
---
# <a name="xaudio2-introduction"></a>Introduzione a XAudio2

XAudio2 è un'API audio di basso livello. Fornisce un'elaborazione del segnale e la combinazione di basi per giochi simili ai predecessori, DirectSound e XAudio.

XAudio2 è la sostituzione tanto attesa per DirectSound. Risolve diversi problemi in sospeso e richieste di funzionalità.

## <a name="xaudio2-features"></a>Funzionalità di XAudio2

Di seguito è riportato un elenco di funzionalità di XAudio2 e nuove funzionalità che consentono agli sviluppatori di migliorare le prestazioni nei giochi.

-   Effetti DSP e filtro per voce

    Gli effetti DSP (Digital Signal Processing) sono i pixel shader dell'audio. Gestiscono tutto, dalla trasformazione di un suono, trasformando uno squeal di pig in un suono basso e da mostrica, al posizionamento dei suoni nell'ambiente di gioco usando il riverbero e l'occlusione o il filtro di ostruzione. XAudio2 offre un framework DSP flessibile e potente. Fornisce anche un filtro predefinito per ogni voce, per effetti efficienti di filtro basso/alto/pass banda.

    Per altre informazioni sugli effetti DSP e sui filtri vocali, vedere Effetti [audio XAudio2](xaudio2-audio-effects.md) e [**IXAudio2Voice::SetFilterParameters.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)

-   Submixing

    Il submixing combina diversi suoni in un unico flusso audio, ad esempio un suono del motore costituito da parti composite, che vengono riprodotte contemporaneamente. È anche possibile usare il submixing per elaborare e combinare parti simili di un gioco. Ad esempio, è possibile combinare tutti gli effetti sonori del gioco per consentire l'applicazione di un'impostazione del volume utente mentre un'impostazione separata controlla il volume della musica. In combinazione con DSP, il submixing fornisce il tipo di routing dei dati e l'elaborazione necessari per i giochi di oggi. XAudio2 consente livelli arbitrari di submixing, consentendo la creazione di suoni complessi e combinazioni di giochi.

    Vedere [XAudio2 Audio Graph](xaudio2-audio-graph.md) [e XAudio2 Voices](xaudio2-voices.md) per altre informazioni sul submixing.

-   Supporto audio compresso

    Una delle principali richieste di funzionalità per DirectSound è il supporto audio compresso. XAudio2 supporta i formati compressi, ADPCM, in modo nativo con la decompressione in fase di esecuzione.

-   Supporto avanzato di audio multicanale e surround

    Il supporto audio multicanale, 3D e surround è espanso. I suoni 3D e surround sono ora molto più flessibili e trasparenti. XAudio2 rimuove il limite di 6 canali per i suoni multicanale e supporta l'audio multicanale in qualsiasi scheda audio con supporto multicanale. Non è necessario che la scheda sia accelerata dall'hardware.

-   Elaborazione a più velocità

    Per ridurre al minimo l'utilizzo della CPU, XAudio2 offre la tecnologia per creare più grafici di elaborazione audio a bassa velocità. Ciò può ridurre significativamente l'utilizzo della CPU consentendo a un gioco di elaborare l'audio alla velocità del materiale di origine se la velocità è inferiore a 48 kHz.

-   Modello DI API non bloccante

    Con poche eccezioni, una chiamata al metodo XAudio2 non bloccherà il motore di elaborazione audio. Ciò significa che un client può eseguire in modo sicuro un set di chiamate al metodo in qualsiasi momento senza bloccare le chiamate a esecuzione lunga causando ritardi. Le eccezioni sono il metodo [**IXAudio2Voice::D estroyVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) (che può bloccare il motore fino al completamento dell'elaborazione della voce da eliminare) e i metodi che terminano il thread audio: [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) e [**IXAudio2::Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Si noti che, sebbene le chiamate al metodo XAudio2 non blocchino il motore di elaborazione audio, i metodi XAudio2 contengono sezioni critiche e possono essere bloccati in alcune circostanze.

## <a name="when-to-use-xaudio2"></a>Quando usare XAudio2

XAudio2 è destinato principalmente allo sviluppo di motori audio ad alte prestazioni per i giochi. Per gli sviluppatori di giochi che voglio aggiungere effetti audio e musica di sottofondo ai propri giochi, XAudio2 offre un motore di missaggio e grafico audio a bassa latenza con supporto per buffer dinamici, riproduzione sincrona dei campioni e conversione implicita della frequenza di origine. Rispetto a WASAPI, XAudio2 richiede solo una quantità minima di codice anche per soluzioni audio complesse. Rispetto al motore Media Foundation, XAudio2 è un'API C++ a bassa latenza di basso livello progettata per l'uso nei giochi.

Per le applicazioni che necessitano semplicemente di una riproduzione di musica regolare, il motore Media Foundation potrebbe essere una migliore corrispondenza con i requisiti dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 
