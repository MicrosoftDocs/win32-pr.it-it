---
description: Se non si ha familiarità con i supporti digitali, in questo argomento vengono introdotti alcuni concetti che è necessario conoscere prima di scrivere un'applicazione Media Foundation.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation: concetti essenziali'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0298a20518df91dab4439770e0f1193802969ae8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104401820"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation: concetti essenziali

Se non si ha familiarità con i supporti digitali, in questo argomento vengono introdotti alcuni concetti che è necessario conoscere prima di scrivere un'applicazione Media Foundation.

-   [Flussi](#streams)
-   [Compressione](#compression)
-   [Contenitori multimediali](#media-containers)
-   [Formati](#formats)
-   [Argomenti correlati](#related-topics)

## <a name="streams"></a>Flussi

Un *flusso* è una sequenza di dati multimediali con un tipo uniforme. I tipi più comuni sono audio e video, ma un flusso può contenere quasi qualsiasi tipo di dati, tra cui testo, comandi di script e immagini ancora. Il termine *flusso* in questa documentazione non implica il recapito in una rete. Un file multimediale destinato alla riproduzione locale contiene anche flussi.

In genere, un file multimediale contiene un solo flusso audio o un flusso video e un flusso audio. Tuttavia, un file multimediale potrebbe contenere diversi flussi dello stesso tipo. Ad esempio, un file video potrebbe contenere flussi audio in diverse lingue. In fase di esecuzione, l'applicazione seleziona il flusso da usare.

## <a name="compression"></a>Compressione

La *compressione* si riferisce a qualsiasi processo che riduce le dimensioni di un flusso di dati rimuovendo le informazioni ridondanti. Gli algoritmi di compressione rientrano in due categorie generali:

-   Compressione senza *perdita di perdite* . Usando un algoritmo senza perdita di dati, i dati ricostruiti sono identici a quelli originali.
-   Compressione con *perdita di perdite* . Usando un algoritmo con perdita di dati, i dati ricostruiti sono un'approssimazione del originale, ma non è una corrispondenza esatta.

Nella maggior parte degli altri domini, la compressione con perdita di perdite non è accettabile. Si supponga di ottenere una "approssimazione" di un foglio di calcolo. Tuttavia, gli schemi di compressione con perdita di perdite sono particolarmente adatti per audio e video, per un paio di motivi.

Il primo motivo ha a che fare con la fisica della percezione umana. Quando ascoltiamo un suono complesso, ad esempio una registrazione musicale, alcune delle informazioni contenute in tale suono non sono percettibili all'orecchio. Con l'ausilio della teoria dell'elaborazione dei segnali, è possibile analizzare e separare le frequenze che non possono essere percepite. Queste frequenze possono essere rimosse senza effetti percettivi. Sebbene l'audio ricostruito non corrisponda esattamente a quello originale *, suonerà lo stesso* per il listener. Principi simili si applicano ai video.

In secondo luogo, potrebbe essere accettabile una riduzione della qualità del suono o dell'immagine, a seconda dello scopo designato. In telefonia, ad esempio, l'audio è spesso fortemente compresso. Il risultato è abbastanza adatto per una conversazione telefonica, ma non è opportuno ascoltare un'orchestrazione sinfonica tramite telefono.

La compressione è detta anche *codifica* e un dispositivo che codifica viene *definito codificatore.* Il processo inverso è la *decodifica* e il dispositivo è naturalmente chiamato *decodificatore*. Il termine generale per codificatori e decodificatori è il *codec*. I codec possono essere implementati in hardware o software.

La tecnologia di compressione è cambiata rapidamente rispetto all'avvento dei supporti digitali e attualmente è in uso un numero elevato di schemi di compressione. Questo è uno dei principali problemi della programmazione multimediale digitale.

## <a name="media-containers"></a>Contenitori multimediali

È raro archiviare un flusso audio o video non elaborato come file del computer oppure inviarne uno direttamente sulla rete. Per una cosa, sarebbe impossibile decodificare un flusso di questo tipo, senza conoscere in anticipo quale codec usare. Pertanto, i file multimediali contengono in genere almeno alcuni degli elementi seguenti:

-   Intestazioni di file che descrivono il numero di flussi, il formato di ogni flusso e così via.
-   Indice che consente l'accesso casuale al contenuto.
-   Metadati che descrivono il contenuto (ad esempio, l'artista o il titolo).
-   Intestazioni di pacchetti, per abilitare la trasmissione di rete o l'accesso casuale.

In questa documentazione viene usato il termine *contenitore* per descrivere l'intero pacchetto di flussi, intestazioni, indici, metadati e così via. Il motivo per cui si usa il termine *contenitore* anziché il *file* è che alcuni formati di contenitore sono progettati per la trasmissione in tempo reale. Un'applicazione può generare il contenitore in tempo reale, senza mai archiviarlo in un file.

Un esempio anticipato di un contenitore multimediale è il formato di file AVI. Altri esempi sono MP4 e Advanced Systems Format (ASF). I contenitori possono essere identificati in base all'estensione del nome file, ad esempio MP4, o al tipo MIME.

Il diagramma seguente illustra una struttura tipica per un contenitore multimediale. Il diagramma non rappresenta un formato specifico. i dettagli di ogni formato variano notevolmente.

![diagramma che mostra un contenitore multimediale tipico](images/concepts01.png)

Si noti che la struttura mostrata nel diagramma è gerarchica, con le informazioni di intestazione visualizzate all'inizio del contenitore. Questa struttura è tipica di molti formati di contenitore (ma non tutti). Si noti anche che la sezione dati contiene pacchetti audio e video con interfoliazione. Questo tipo di interfoliazione è comune nei contenitori di contenuti multimediali.

Il termine *multiplexing* si riferisce al processo di packetizing dei flussi audio e video e all'interfoliazione dei pacchetti nel contenitore. Il processo inverso, ovvero il riassemblaggio dei flussi dai dati in pacchetto, viene definito *demultiplexing*.

## <a name="formats"></a>Formati

Nei supporti digitali il *formato* del termine è ambiguo. Un formato può riferirsi al tipo di *codifica*, ad esempio il video H. 264 o il *contenitore*, ad esempio MP4. Questa distinzione è spesso confusa per gli utenti normali. I nomi assegnati ai formati multimediali non sempre sono utili. Il formato *MP3* , ad esempio, si riferisce sia a un formato di codifica (MPEG-1 Audio Layer 3) che a un formato di file.

Questa distinzione è importante, tuttavia, perché la lettura di un file multimediale comporta effettivamente due fasi:

1.  Prima di tutto, il contenitore deve essere analizzato. Nella maggior parte dei casi, il numero di flussi e il formato di ogni flusso non possono essere noti fino al completamento di questo passaggio.
2.  Successivamente, se i flussi sono compressi, è necessario decodificarli usando i decodificatori appropriati.

Questo fatto conduce abbastanza naturalmente a una progettazione software in cui vengono usati componenti separati per analizzare i contenitori e decodificare i flussi. Inoltre, questo approccio si presta a un modello di plug-in, in modo che le terze parti possano fornire i propri parser e codec. In Windows, il Component Object Model (COM) fornisce un modo standard per separare un'API dalla relativa implementazione, che è un requisito per qualsiasi modello di plug-in. Per questo motivo, tra gli altri, Media Foundation usa le interfacce COM.

Il diagramma seguente illustra i componenti usati per leggere un file multimediale:

![diagramma che mostra i componenti per la lettura di un file multimediale](images/concepts02.png)

La scrittura di un file multimediale richiede anche due passaggi:

1.  Codifica dei dati audio/video non compressi.
2.  Inserimento dei dati compressi in un formato contenitore specifico.

Il diagramma seguente illustra i componenti usati per scrivere un file multimediale:

![diagramma che mostra i componenti per la scrittura di un file multimediale.](images/concepts03.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 



