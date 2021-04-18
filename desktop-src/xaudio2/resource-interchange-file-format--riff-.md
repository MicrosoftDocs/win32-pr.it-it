---
description: Questa panoramica descrive il formato del file di interscambio di risorse (RIFF), usato nei file WAV. RIFF è il formato tipico da cui verranno caricati i dati audio per XAudio2.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Resource Interchange File Format (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319080"
---
# <a name="resource-interchange-file-format-riff"></a>Resource Interchange File Format (RIFF)

Questa panoramica descrive il formato del file di interscambio di risorse (RIFF), usato nei file WAV. RIFF è il formato tipico da cui verranno caricati i dati audio per XAudio2.

## <a name="riff"></a>RIFF

Un file RIFF è costituito da più sezioni discrete di dati denominati *blocchi*.

## <a name="fourcc-identifiers"></a>Identificatori FOURCC

Il tipo di dati in un blocco è indicato da un identificatore di codice a quattro caratteri (FOURCC). Un FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII usati per identificare i tipi di blocchi in un file RIFF. Ad esempio, FOURCC "abcd" viene rappresentato in un sistema little-endian come 0x64636261. FourCC può contenere caratteri di spazio, quindi "ABC" è un FOURCC valido. I file audio usano i codici FOURCC per identificare i blocchi di formato audio, i blocchi di dati audio e tutti gli altri blocchi specifici del formato audio.

La tabella seguente illustra gli identificatori FOURCC che possono essere previsti nei formati audio supportati da XAudio2. 

| Formato | Identificatori FOURCC                     | Informazioni aggiuntive                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "RIFF", "fmt", "data"                 |                                                                                                      |
| ADPCM  | "RIFF", "fmt", "data", "SMPL", "wsmpl" | Per una descrizione degli identificatori FOURCC specifici di ADPCM, vedere [Cenni preliminari su ADPCM](adpcm-overview.md) . |



 

Gli identificatori FOURCC "RIFF", "fmt" e "data" sono comuni a tutti i formati supportati. Nella tabella seguente vengono descritti gli identificatori FOURCC presenti in tutti i formati supportati. 

| Identificatore FOURCC | Descrizione                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | Blocco RIFF standard contenente un tipo di file con il valore "WAVE" o "XWMA" nei primi quattro byte della sezione relativa ai dati e gli altri blocchi del file nel resto della sezione relativa ai dati.                                   |
| "fmt"             | Contiene l'intestazione del formato per il file audio. I dati in questo blocco corrispondono a una delle strutture seguenti: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| "data"            | Contiene dati audio per il file audio. In XAudio2 il contenuto del blocco di dati verrà letto in un buffer e passato a una voce di origine come membro **pAudioData** di una struttura di [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . |



 

## <a name="chunks"></a>Chunks

Un file RIFF è costituito da un blocco RIFF che contiene zero o più blocchi.

-   Il blocco RIFF ha il formato seguente:

    "RIFF", filesize, FileType, data

    Dove "RIFF" è il codice FOURCC letterale "RIFF", *Filesize* è un valore a 4 byte che assegna la dimensione dei dati nel file e *FileType* è un FourCC che identifica il tipo di file specifico. Il valore di *Filesize* include le dimensioni del *FileType* FourCC più le dimensioni dei dati seguenti, ma non le dimensioni del fourcc "riff" o della dimensione del *Filesize*. I dati sono costituiti da blocchi in qualsiasi ordine.

-   Gli altri blocchi hanno il formato seguente:

    ```
    chunkID, chunkSize, data
    ```

    

    Dove *chunkID* è un FourCC che identifica i dati contenuti nel blocco, *ChunkSize* è un valore a 4 byte che assegna la dimensione della sezione dati del blocco e i dati sono pari a zero o più byte di dati. I dati vengono sempre riempiti al confine di parola più vicino. *ChunkSize* fornisce la dimensione dei dati validi nel blocco. Non include la spaziatura interna, le dimensioni di *chunkID* o le dimensioni di *ChunkSize*.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Procedura: Riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 



