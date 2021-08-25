---
description: Questa panoramica descrive il formato RIFF (Resource Interchange File Format), usato nei file wav. RIFF è il formato tipico da cui verranno caricati i dati audio per XAudio2.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Resource Interchange File Format (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c223c5a1047ffc9828a42ccc09ce4a94f5e766a1bc4851996b911f15f90995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054331"
---
# <a name="resource-interchange-file-format-riff"></a>Resource Interchange File Format (RIFF)

Questa panoramica descrive il formato RIFF (Resource Interchange File Format), usato nei file wav. RIFF è il formato tipico da cui verranno caricati i dati audio per XAudio2.

## <a name="riff"></a>RIFF

Un file RIFF è costituito da più sezioni discrete di dati denominate *blocchi*.

## <a name="fourcc-identifiers"></a>Identificatori FOURCC

Il tipo di dati in un blocco è indicato da un identificatore four-character code (FOURCC). FOURCC è un intero senza segno a 32 bit creato concatenando quattro caratteri ASCII usati per identificare i tipi di blocco in un file RIFF. Ad esempio, fourCC "abcd" è rappresentato in un sistema little-endian come 0x64636261. I quattroCC possono contenere spazi, quindi " abc" è un valore FOURCC valido. I file audio usano codici FOURCC per identificare i blocchi di formato audio, i blocchi di dati audio e qualsiasi altro blocco specifico per il formato audio.

La tabella seguente illustra gli identificatori FOURCC che possono essere previsti nei formati audio supportati da XAudio2. 

| Formato | Identificatori FOURCC                     | Informazioni aggiuntive                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "RIFF", "fmt", "data"                 |                                                                                                      |
| Adpcm  | "RIFF", "fmt", "data", "smpl", "wsmpl" | Per una descrizione degli identificatori FOURCC specifici di ADPCM, vedere Panoramica di [ADPCM.](adpcm-overview.md) |



 

Gli identificatori FOURCC "RIFF", "fmt" e "data" sono comuni a tutti i formati supportati. Nella tabella seguente vengono descritti gli identificatori FOURCC disponibili in tutti i formati supportati. 

| Identificatore FOURCC | Descrizione                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | Blocco RIFF standard contenente un tipo di file con il valore "WAVE" o "XWMA" nei primi quattro byte della sezione dei dati e gli altri blocchi nel file nella parte restante della sezione dei dati.                                   |
| "fmt"             | Contiene l'intestazione di formato per il file audio. I dati in questo blocco corrispondono a una delle strutture seguenti: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| "data"            | Contiene i dati audio per il file audio. In XAudio2 il contenuto del blocco di dati verrà letto in un buffer e passato a una voce di origine come membro **pAudioData** di una [**struttura BUFFER XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) |



 

## <a name="chunks"></a>Chunks

Un file RIFF è costituito da un blocco RIFF contenente zero o più altri blocchi.

-   Il blocco RIFF ha il formato seguente:

    "RIFF", fileSize, fileType, data

    Dove "RIFF" è il codice FOURCC letterale "RIFF", *fileSize* è un valore a 4 byte che specifica le dimensioni dei dati nel file e *fileType* è un elemento FOURCC che identifica il tipo di file specifico. Il valore di *fileSize* include le dimensioni di *fileType* FOURCC più le dimensioni dei dati che seguono, ma non include la dimensione di "RIFF" FOURCC o la dimensione di *fileSize*. I dati sono costituiti da blocchi in qualsiasi ordine.

-   Altri blocchi hanno il formato seguente:

    ```
    chunkID, chunkSize, data
    ```

    

    Dove *chunkID* è un elemento FOURCC che identifica i dati contenuti nel blocco, *chunkSize* è un valore a 4 byte che specifica le dimensioni della sezione data del blocco e i dati sono pari a zero o più byte di dati. I dati vengono sempre riempiti fino al limite WORD più vicino. *chunkSize* fornisce le dimensioni dei dati validi nel blocco. Non include la spaziatura interna, la dimensione *di chunkID* o la dimensione *di chunkSize.*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Procedura: Riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 



