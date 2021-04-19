---
description: Questa panoramica introduce alcuni concetti chiave per l'uso di XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Concetti chiave di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317841"
---
# <a name="xaudio2-key-concepts"></a>Concetti chiave di XAudio2

Questa panoramica introduce alcuni concetti chiave per l'uso di XAudio2.

-   [Motore XAudio2](#xaudio2-engine)
-   [Voci](#voices)
-   [Grafico audio](#audio-graph)
-   [Callback](#callbacks)
-   [Argomenti correlati](#related-topics)

## <a name="xaudio2-engine"></a>Motore XAudio2

L’interfaccia [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) è l’elemento principale del motore XAudio2 La creazione di un'istanza dell'interfaccia **IXAudio2** consente al client di enumerare i dispositivi audio disponibili, di configurare le proprietà globali dell'API, di creare voci e di monitorare le prestazioni. La funzione helper [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) esegue le attività di creazione di istanze e di inizializzazione per XAudio2.

È possibile creare istanze di XAudio2 più volte all'interno di un singolo processo. Ogni oggetto XAudio2 opera in modo indipendente e dispone di un proprio thread di elaborazione audio. Vengono condivise solo le impostazioni di debug. Questo è importante in Windows in cui è possibile caricare diversi componenti in un unico processo. Internet Explorer, ad esempio, potrebbe utilizzare più componenti XAudio2 contemporaneamente. Sebbene sia possibile creare più oggetti motore XAudio2 all'interno di una singola applicazione client, non è necessario passare informazioni tra i rispettivi grafici.

Per un esempio di inizializzazione del motore XAudio2, vedere [procedura: inizializzare XAudio2](how-to--initialize-xaudio2.md).

## <a name="voices"></a>Voci

Le voci sono gli oggetti utilizzati da XAudio2 per elaborare, modificare e riprodurre dati audio. In XAudio2 sono disponibili tre tipi di voci.

-   [**Voci di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    Le voci di origine rappresentano un flusso di dati audio. Le voci di origine inviano i dati ad altri tipi di voci.

-   [**Voci di submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    Le voci submix eseguono una manipolazione dei dati audio ricevuti. Un esempio di manipolazione dei dati audio potrebbe essere la conversione della frequenza di campionamento. Dopo che una voce submix elabora i dati, passa i dati a un'altra voce submix o a una voce Master.

-   [**Voci di mastering**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    Le voci di mastering ricevono i dati dalle voci di origine e submix e inviano i dati all'hardware audio.

Per una panoramica delle voci di XAudio2, vedere [XAudio2 Voices](voices.md) .

## <a name="audio-graph"></a>Grafico audio

Un grafico audio è una raccolta di voci XAudio2. L'audio inizia da un lato di un grafico audio nelle voci di origine, passa facoltativamente da una o più voci submix e termina con una voce di master. Un grafico audio conterrà una voce di origine per ogni suono attualmente in riproduzione, zero o più voci submix e una voce Master. Il grafico audio più semplice e il minimo necessario per creare un rumore in XAudio2 sono una singola voce di origine che consente di ottenere direttamente una voce di master. Vedere [procedura: riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md) per un esempio della procedura minima necessaria per riprodurre un suono con XAudio2.

Per una panoramica dei grafici audio di XAudio2, vedere [XAudio2 audio Graph](audio-graphs.md) .

## <a name="callbacks"></a>Callback

I callback sono il meccanismo usato da XAudio2 per segnalare al codice client che si è verificato un evento in una voce o nell'oggetto motore. Poiché la riproduzione audio è asincrona nel motore XAudio2, i callback forniscono l'unico modo per determinare quando un suono termina la riproduzione.

Per una panoramica dei callback di XAudio2, vedere [callback di XAudio2](callbacks.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Versioni di XAudio2](xaudio2-versions.md)
</dt> <dt>

[Procedura: Inizializzare XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Procedura: riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



