---
description: Se non si ha conoscenza dei supporti digitali, questo argomento presenta alcuni concetti che è necessario comprendere prima di scrivere un'Media Foundation appliazione.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation: concetti essenziali'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825e84b3c7ad3060cae0a2530bc9a7af3155fd9113c490ce2c42f69771c1f9b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357266"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation: concetti essenziali

Se non si ha conoscenza dei supporti digitali, questo argomento presenta alcuni concetti che è necessario comprendere prima di scrivere un'Media Foundation appliazione.

-   [Flussi](#streams)
-   [Compressione](#compression)
-   [Contenitori di supporti](#media-containers)
-   [Formati](#formats)
-   [Argomenti correlati](#related-topics)

## <a name="streams"></a>Flussi

Un *flusso* è una sequenza di dati multimediali con un tipo uniforme. I tipi più comuni sono audio e video, ma un flusso può contenere quasi tutti i tipi di dati, tra cui testo, comandi script e immagini fisse. Il termine *flusso* in questa documentazione non implica il recapito in rete. Anche un file multimediale destinato alla riproduzione locale contiene flussi.

In genere, un file multimediale contiene un singolo flusso audio o esattamente un flusso video e un flusso audio. Tuttavia, un file multimediale potrebbe contenere diversi flussi dello stesso tipo. Ad esempio, un file video potrebbe contenere flussi audio in diverse lingue. In fase di esecuzione, l'applicazione seleziona il flusso da usare.

## <a name="compression"></a>Compressione

*La* compressione si riferisce a qualsiasi processo che riduce le dimensioni di un flusso di dati rimuovendo le informazioni ridondanti. Gli algoritmi di compressione rientrano in due ampie categorie:

-   *Compressione senza* perdita di dati. Usando un algoritmo senza perdita di dati, i dati ricostruiti sono identici all'originale.
-   *Compressione con perdita* di dati. Usando un algoritmo di perdita, i dati ricostruiti sono un'approssimazione dell'originale, ma non è una corrispondenza esatta.

Nella maggior parte degli altri domini la compressione con perdita di dati non è accettabile. (Imagine ottenere una "approssimazione" di un foglio di calcolo. Tuttavia, gli schemi di compressione con perdita di dati sono particolarmente adatti per audio e video, per un paio di motivi.

Il primo motivo è la fisica della percezione umana. Quando si ascolta un suono complesso, ad esempio una registrazione musicale, alcune delle informazioni contenute in tale suono non sono percepibili per l'udito. Con l'aiuto della teoria dell'elaborazione dei segnali, è possibile analizzare e separare le frequenze che non possono essere percepite. Queste frequenze possono essere rimosse senza alcun effetto percettivo. Anche se l'audio ricostruito non corrisponde esattamente all'originale, *suonerà* lo stesso al listener. Principi simili si applicano ai video.

In secondo piano, una riduzione della qualità del suono o dell'immagine può essere accettabile, a seconda dello scopo previsto. Nella telefonia, ad esempio, l'audio è spesso altamente compresso. Il risultato è sufficiente per una conversazione telefonica, ma non si vuole ascoltare un'orchestra sinfonica al telefono.

La compressione è detta *anche codifica* e un dispositivo che codifica è denominato *codificatore*. Il processo inverso è *la decodifica* e il dispositivo è un decodificatore chiamato *naturalmente*. Il termine generale per codificatori e decodificatori è *codec*. I codec possono essere implementati nell'hardware o nel software.

La tecnologia di compressione è cambiata rapidamente dall'avvento dei supporti digitali e attualmente sono in uso numerosi schemi di compressione. Questa è una delle principali sfide per la programmazione dei supporti digitali.

## <a name="media-containers"></a>Contenitori di supporti

È raro archiviare un flusso audio o video non elaborato come file del computer o inviarlo direttamente in rete. Per prima cosa, sarebbe impossibile decodificare un flusso di questo tipo, senza sapere in anticipo quale codec usare. Di conseguenza, i file multimediali contengono in genere almeno alcuni degli elementi seguenti:

-   Intestazioni di file che descrivono il numero di flussi, il formato di ogni flusso e così via.
-   Indice che consente l'accesso casuale al contenuto.
-   Metadati che descrivono il contenuto , ad esempio l'artista o il titolo.
-   Intestazioni di pacchetto, per abilitare la trasmissione di rete o l'accesso casuale.

Questa documentazione usa il termine *contenitore* per descrivere l'intero pacchetto di flussi, intestazioni, indici, metadati e così via. Il motivo per cui si usa il termine *contenitore* anziché *file* è che alcuni formati di contenitore sono progettati per la trasmissione live. Un'applicazione potrebbe generare il contenitore in tempo reale, senza archiviarlo mai in un file.

Un primo esempio di contenitore multimediale è il formato di file AVI. Altri esempi includono MP4 e Advanced Systems Format (ASF). I contenitori possono essere identificati dall'estensione del nome file (ad esempio, .mp4) o dal tipo MIME.

Il diagramma seguente illustra una struttura tipica per un contenitore di supporti. Il diagramma non rappresenta alcun formato specifico. i dettagli di ogni formato variano notevolmente.

![Diagramma che mostra un contenitore multimediale tipico](images/concepts01.png)

Si noti che la struttura illustrata nel diagramma è gerarchica, con le informazioni di intestazione visualizzate all'inizio del contenitore. Questa struttura è tipica di molti formati di contenitore (ma non di tutti). Si noti anche che la sezione dei dati contiene pacchetti audio e video interleaved. Questo tipo di interfoliazione è comune nei contenitori multimediali.

Il termine *multiplexing* si riferisce al processo di creazione di pacchetti dei flussi audio e video e dell'interfoliazione dei pacchetti nel contenitore. Il processo inverso, riassemblando i flussi dai dati in pacchetto, è detto *demultiplexing*.

## <a name="formats"></a>Formati

Nei supporti digitali il termine *formato* è ambiguo. Un formato può fare riferimento al tipo *di* codifica , ad esempio il video H.264 o il *contenitore*, ad esempio MP4. Questa distinzione spesso crea confusione per gli utenti comuni. I nomi dati ai formati multimediali non sempre sono utili. Ad esempio, *MP3* si riferisce sia a un formato di codifica (MPEG-1 Audio Layer 3) che a un formato di file.

La distinzione è tuttavia importante, perché la lettura di un file multimediale comporta effettivamente due fasi:

1.  In primo luogo, il contenitore deve essere analizzato. Nella maggior parte dei casi, il numero di flussi e il formato di ogni flusso non possono essere noti fino al completamento di questo passaggio.
2.  Successivamente, se i flussi sono compressi, devono essere decodificati usando i decodificatori appropriati.

Questo fatto porta naturalmente a una progettazione software in cui vengono usati componenti separati per analizzare i contenitori e decodificare i flussi. Inoltre, questo approccio si presta a un modello di plug-in, in modo che terze parti possano fornire parser e codec personalizzati. In Windows, il Component Object Model (COM) fornisce un modo standard per separare un'API dalla relativa implementazione, che è un requisito per qualsiasi modello di plug-in. Per questo motivo (tra gli altri), Media Foundation le interfacce COM.

Il diagramma seguente illustra i componenti usati per leggere un file multimediale:

![diagramma che mostra i componenti per leggere un file multimediale](images/concepts02.png)

La scrittura di un file multimediale richiede anche due passaggi:

1.  Codifica dei dati audio/video non compressi.
2.  Inserimento dei dati compressi in un formato di contenitore specifico.

Il diagramma seguente illustra i componenti usati per scrivere un file multimediale:

![diagramma che mostra i componenti per scrivere un file multimediale.](images/concepts03.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation per programmatori](media-foundation-programming-guide.md)
</dt> </dl>

 

 



