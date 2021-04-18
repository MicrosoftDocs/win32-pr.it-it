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
# <a name="resource-interchange-file-format-riff"></a><span data-ttu-id="847a5-104">Resource Interchange File Format (RIFF)</span><span class="sxs-lookup"><span data-stu-id="847a5-104">Resource Interchange File Format (RIFF)</span></span>

<span data-ttu-id="847a5-105">Questa panoramica descrive il formato del file di interscambio di risorse (RIFF), usato nei file WAV.</span><span class="sxs-lookup"><span data-stu-id="847a5-105">This overview describes the Resource Interchange File Format (RIFF), which is used in .wav files.</span></span> <span data-ttu-id="847a5-106">RIFF è il formato tipico da cui verranno caricati i dati audio per XAudio2.</span><span class="sxs-lookup"><span data-stu-id="847a5-106">RIFF is the typical format from which audio data for XAudio2 will be loaded.</span></span>

## <a name="riff"></a><span data-ttu-id="847a5-107">RIFF</span><span class="sxs-lookup"><span data-stu-id="847a5-107">RIFF</span></span>

<span data-ttu-id="847a5-108">Un file RIFF è costituito da più sezioni discrete di dati denominati *blocchi*.</span><span class="sxs-lookup"><span data-stu-id="847a5-108">A RIFF file is composed of multiple discrete sections of data called *chunks*.</span></span>

## <a name="fourcc-identifiers"></a><span data-ttu-id="847a5-109">Identificatori FOURCC</span><span class="sxs-lookup"><span data-stu-id="847a5-109">FOURCC Identifiers</span></span>

<span data-ttu-id="847a5-110">Il tipo di dati in un blocco è indicato da un identificatore di codice a quattro caratteri (FOURCC).</span><span class="sxs-lookup"><span data-stu-id="847a5-110">The type of data in a chunk is indicated by a four-character code (FOURCC) identifier.</span></span> <span data-ttu-id="847a5-111">Un FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII usati per identificare i tipi di blocchi in un file RIFF.</span><span class="sxs-lookup"><span data-stu-id="847a5-111">A FOURCC is a 32-bit unsigned integer created by concatenating four ASCII characters used to identify chunk types in a RIFF file.</span></span> <span data-ttu-id="847a5-112">Ad esempio, FOURCC "abcd" viene rappresentato in un sistema little-endian come 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="847a5-112">For example, the FOURCC "abcd" is represented on a little-endian system as 0x64636261.</span></span> <span data-ttu-id="847a5-113">FourCC può contenere caratteri di spazio, quindi "ABC" è un FOURCC valido.</span><span class="sxs-lookup"><span data-stu-id="847a5-113">FOURCCs can contain space characters, so " abc" is a valid FOURCC.</span></span> <span data-ttu-id="847a5-114">I file audio usano i codici FOURCC per identificare i blocchi di formato audio, i blocchi di dati audio e tutti gli altri blocchi specifici del formato audio.</span><span class="sxs-lookup"><span data-stu-id="847a5-114">Audio files use FOURCC codes to identify audio format chunks, audio data chunks, and any other chunks specific to the audio format.</span></span>

<span data-ttu-id="847a5-115">La tabella seguente illustra gli identificatori FOURCC che possono essere previsti nei formati audio supportati da XAudio2.</span><span class="sxs-lookup"><span data-stu-id="847a5-115">The following table shows the FOURCC identifiers that can be expected in the audio formats supported by XAudio2.</span></span> 

| <span data-ttu-id="847a5-116">Formato</span><span class="sxs-lookup"><span data-stu-id="847a5-116">Format</span></span> | <span data-ttu-id="847a5-117">Identificatori FOURCC</span><span class="sxs-lookup"><span data-stu-id="847a5-117">FOURCC identifiers</span></span>                     | <span data-ttu-id="847a5-118">Informazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="847a5-118">Additional information</span></span>                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="847a5-119">PCM</span><span class="sxs-lookup"><span data-stu-id="847a5-119">PCM</span></span>    | <span data-ttu-id="847a5-120">"RIFF", "fmt", "data"</span><span class="sxs-lookup"><span data-stu-id="847a5-120">"RIFF", "fmt" , "data"</span></span>                 |                                                                                                      |
| <span data-ttu-id="847a5-121">ADPCM</span><span class="sxs-lookup"><span data-stu-id="847a5-121">ADPCM</span></span>  | <span data-ttu-id="847a5-122">"RIFF", "fmt", "data", "SMPL", "wsmpl"</span><span class="sxs-lookup"><span data-stu-id="847a5-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span></span> | <span data-ttu-id="847a5-123">Per una descrizione degli identificatori FOURCC specifici di ADPCM, vedere [Cenni preliminari su ADPCM](adpcm-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="847a5-123">See [ADPCM Overview](adpcm-overview.md) for a description of the ADPCM-specific FOURCC identifiers.</span></span> |



 

<span data-ttu-id="847a5-124">Gli identificatori FOURCC "RIFF", "fmt" e "data" sono comuni a tutti i formati supportati.</span><span class="sxs-lookup"><span data-stu-id="847a5-124">The FOURCC identifiers "RIFF", "fmt", and "data" are common to all of the supported formats.</span></span> <span data-ttu-id="847a5-125">Nella tabella seguente vengono descritti gli identificatori FOURCC presenti in tutti i formati supportati.</span><span class="sxs-lookup"><span data-stu-id="847a5-125">The following table describes the FOURCC identifiers that are found in all of the supported formats.</span></span> 

| <span data-ttu-id="847a5-126">Identificatore FOURCC</span><span class="sxs-lookup"><span data-stu-id="847a5-126">FOURCC identifier</span></span> | <span data-ttu-id="847a5-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="847a5-127">Description</span></span>                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="847a5-128">"RIFF"</span><span class="sxs-lookup"><span data-stu-id="847a5-128">"RIFF"</span></span>            | <span data-ttu-id="847a5-129">Blocco RIFF standard contenente un tipo di file con il valore "WAVE" o "XWMA" nei primi quattro byte della sezione relativa ai dati e gli altri blocchi del file nel resto della sezione relativa ai dati.</span><span class="sxs-lookup"><span data-stu-id="847a5-129">Standard RIFF chunk containing a file type with the value of "WAVE" or "XWMA" in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                   |
| <span data-ttu-id="847a5-130">"fmt"</span><span class="sxs-lookup"><span data-stu-id="847a5-130">"fmt"</span></span>             | <span data-ttu-id="847a5-131">Contiene l'intestazione del formato per il file audio.</span><span class="sxs-lookup"><span data-stu-id="847a5-131">Contains the format header for the audio file.</span></span> <span data-ttu-id="847a5-132">I dati in questo blocco corrispondono a una delle strutture seguenti: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span><span class="sxs-lookup"><span data-stu-id="847a5-132">The data in this chunk corresponds to one of the following structures: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span></span>                                                  |
| <span data-ttu-id="847a5-133">"data"</span><span class="sxs-lookup"><span data-stu-id="847a5-133">"data"</span></span>            | <span data-ttu-id="847a5-134">Contiene dati audio per il file audio.</span><span class="sxs-lookup"><span data-stu-id="847a5-134">Contains audio data for the audio file.</span></span> <span data-ttu-id="847a5-135">In XAudio2 il contenuto del blocco di dati verrà letto in un buffer e passato a una voce di origine come membro **pAudioData** di una struttura di [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="847a5-135">In XAudio2, the contents of the data chunk will be read into a buffer and passed to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> |



 

## <a name="chunks"></a><span data-ttu-id="847a5-136">Chunks</span><span class="sxs-lookup"><span data-stu-id="847a5-136">Chunks</span></span>

<span data-ttu-id="847a5-137">Un file RIFF è costituito da un blocco RIFF che contiene zero o più blocchi.</span><span class="sxs-lookup"><span data-stu-id="847a5-137">A RIFF file consists of a RIFF chunk containing zero or more other chunks.</span></span>

-   <span data-ttu-id="847a5-138">Il blocco RIFF ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="847a5-138">The RIFF chunk has the following form:</span></span>

    <span data-ttu-id="847a5-139">"RIFF", filesize, FileType, data</span><span class="sxs-lookup"><span data-stu-id="847a5-139">"RIFF", fileSize, fileType, data</span></span>

    <span data-ttu-id="847a5-140">Dove "RIFF" è il codice FOURCC letterale "RIFF", *Filesize* è un valore a 4 byte che assegna la dimensione dei dati nel file e *FileType* è un FourCC che identifica il tipo di file specifico.</span><span class="sxs-lookup"><span data-stu-id="847a5-140">Where "RIFF" is the literal FOURCC code "RIFF", *fileSize* is a 4-byte value giving the size of the data in the file, and *fileType* is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="847a5-141">Il valore di *Filesize* include le dimensioni del *FileType* FourCC più le dimensioni dei dati seguenti, ma non le dimensioni del fourcc "riff" o della dimensione del *Filesize*.</span><span class="sxs-lookup"><span data-stu-id="847a5-141">The value of *fileSize* includes the size of *fileType* FOURCC plus the size of the data that follows, but does not include the size of the "RIFF" FOURCC or the size of *fileSize*.</span></span> <span data-ttu-id="847a5-142">I dati sono costituiti da blocchi in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="847a5-142">The data consists of chunks in any order.</span></span>

-   <span data-ttu-id="847a5-143">Gli altri blocchi hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="847a5-143">Other chunks have the following form:</span></span>

    ```
    chunkID, chunkSize, data
    ```

    

    <span data-ttu-id="847a5-144">Dove *chunkID* è un FourCC che identifica i dati contenuti nel blocco, *ChunkSize* è un valore a 4 byte che assegna la dimensione della sezione dati del blocco e i dati sono pari a zero o più byte di dati.</span><span class="sxs-lookup"><span data-stu-id="847a5-144">Where *chunkID* is a FOURCC that identifies the data contained in the chunk, *chunkSize* is a 4-byte value giving the size of the data section of the chunk, and data is zero or more bytes of data.</span></span> <span data-ttu-id="847a5-145">I dati vengono sempre riempiti al confine di parola più vicino.</span><span class="sxs-lookup"><span data-stu-id="847a5-145">The data is always padded to the nearest WORD boundary.</span></span> <span data-ttu-id="847a5-146">*ChunkSize* fornisce la dimensione dei dati validi nel blocco.</span><span class="sxs-lookup"><span data-stu-id="847a5-146">*chunkSize* gives the size of the valid data in the chunk.</span></span> <span data-ttu-id="847a5-147">Non include la spaziatura interna, le dimensioni di *chunkID* o le dimensioni di *ChunkSize*.</span><span class="sxs-lookup"><span data-stu-id="847a5-147">It does not include the padding, the size of *chunkID*, or the size of *chunkSize*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="847a5-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="847a5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847a5-149">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="847a5-149">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="847a5-150">Procedura: Riprodurre un suono con XAudio2</span><span class="sxs-lookup"><span data-stu-id="847a5-150">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="847a5-151">Guida di riferimento alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="847a5-151">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 



