---
description: Guida di riferimento al file con estensione AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Guida di riferimento al file con estensione AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482548"
---
# <a name="avi-riff-file-reference"></a><span data-ttu-id="de623-103">Guida di riferimento al file con estensione AVI</span><span class="sxs-lookup"><span data-stu-id="de623-103">AVI RIFF File Reference</span></span>

<span data-ttu-id="de623-104">Il formato di file di Microsoft AVI è una specifica del file RIFF usata con le applicazioni che acquisiscono, modificano e riproducono sequenze audio-video.</span><span class="sxs-lookup"><span data-stu-id="de623-104">The Microsoft AVI file format is a RIFF file specification used with applications that capture, edit, and play back audio-video sequences.</span></span> <span data-ttu-id="de623-105">In generale, i file AVI contengono più flussi di tipi diversi di dati.</span><span class="sxs-lookup"><span data-stu-id="de623-105">In general, AVI files contain multiple streams of different types of data.</span></span> <span data-ttu-id="de623-106">La maggior parte delle sequenze AVI USA flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="de623-106">Most AVI sequences use both audio and video streams.</span></span> <span data-ttu-id="de623-107">Una variante semplice per una sequenza AVI usa dati video e non richiede un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="de623-107">A simple variation for an AVI sequence uses video data and does not require an audio stream.</span></span>

<span data-ttu-id="de623-108">Questa sezione non descrive le estensioni di formato file AVI di OpenDML.</span><span class="sxs-lookup"><span data-stu-id="de623-108">This section does not describe the OpenDML AVI file format extensions.</span></span> <span data-ttu-id="de623-109">Per ulteriori informazioni su queste estensioni, vedere *OPENDML AVI file format Extensions*, pubblicato dal sottocomitato del formato di file OpenDML AVI M-JPEG.</span><span class="sxs-lookup"><span data-stu-id="de623-109">For further information on these extensions, see *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="fourccs"></a><span data-ttu-id="de623-110">FourCC</span><span class="sxs-lookup"><span data-stu-id="de623-110">FOURCCs</span></span>

<span data-ttu-id="de623-111">Un FOURCC (codice a quattro caratteri) è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="de623-111">A FOURCC (four-character code) is a 32-bit unsigned integer created by concatenating four ASCII characters.</span></span> <span data-ttu-id="de623-112">Ad esempio, il FOURCC "abcd" viene rappresentato in un sistema di Little-Endian come 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="de623-112">For example, the FOURCC 'abcd' is represented on a Little-Endian system as 0x64636261.</span></span> <span data-ttu-id="de623-113">FourCC può contenere caratteri di spazio, quindi "ABC" è un FOURCC valido.</span><span class="sxs-lookup"><span data-stu-id="de623-113">FOURCCs can contain space characters, so ' abc' is a valid FOURCC.</span></span> <span data-ttu-id="de623-114">Il formato di file AVI usa i codici FOURCC per identificare i tipi di flusso, i blocchi di dati, le voci di indice e altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="de623-114">The AVI file format uses FOURCC codes to identify stream types, data chunks, index entries, and other information.</span></span>

## <a name="riff-file-format"></a><span data-ttu-id="de623-115">Formato file RIFF</span><span class="sxs-lookup"><span data-stu-id="de623-115">RIFF File Format</span></span>

<span data-ttu-id="de623-116">Il formato del file AVI è basato sul formato di documento RIFF (Resource Interchange File Format).</span><span class="sxs-lookup"><span data-stu-id="de623-116">The AVI file format is based on the RIFF (resource interchange file format) document format.</span></span> <span data-ttu-id="de623-117">Un file RIFF è costituito da un'intestazione RIFF seguita da zero o più *elenchi* e *blocchi*.</span><span class="sxs-lookup"><span data-stu-id="de623-117">A RIFF file consists of a RIFF header followed by zero or more *lists* and *chunks*.</span></span>

-   <span data-ttu-id="de623-118">L'intestazione RIFF ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="de623-118">The RIFF header has the following form:</span></span>

    `'RIFF' fileSize fileType (data)`

    <span data-ttu-id="de623-119">dove ' RIFF ' è il codice FOURCC ' RIFF ' letterale, `fileSize` è un valore a 4 byte che fornisce la dimensione dei dati nel file e `fileType` è un FourCC che identifica il tipo di file specifico.</span><span class="sxs-lookup"><span data-stu-id="de623-119">where 'RIFF' is the literal FOURCC code 'RIFF', `fileSize` is a 4-byte value giving the size of the data in the file, and `fileType` is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="de623-120">Il valore di `fileSize` include le dimensioni di `fileType` fourcc più le dimensioni dei dati seguenti, ma non include le dimensioni del FourCC ' riff ' o la dimensione di `fileSize` .</span><span class="sxs-lookup"><span data-stu-id="de623-120">The value of `fileSize` includes the size of the `fileType` FOURCC plus the size of the data that follows, but does not include the size of the 'RIFF' FOURCC or the size of `fileSize`.</span></span> <span data-ttu-id="de623-121">I dati dei file sono costituiti da blocchi ed elenchi, in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="de623-121">The file data consists of chunks and lists, in any order.</span></span>

-   <span data-ttu-id="de623-122">Un blocco ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="de623-122">A chunk has the following form:</span></span>

    `ckID ckSize ckData`

    <span data-ttu-id="de623-123">dove `ckID` è un FourCC che identifica i dati contenuti nel blocco, `ckSize` è un valore a 4 byte che fornisce la dimensione dei dati in `ckData` e `ckData` è pari a zero o più byte di dati.</span><span class="sxs-lookup"><span data-stu-id="de623-123">where `ckID` is a FOURCC that identifies the data contained in the chunk, `ckSize` is a 4-byte value giving the size of the data in `ckData`, and `ckData` is zero or more bytes of data.</span></span> <span data-ttu-id="de623-124">I dati vengono sempre riempiti al confine di **parola** più vicino.</span><span class="sxs-lookup"><span data-stu-id="de623-124">The data is always padded to nearest **WORD** boundary.</span></span> <span data-ttu-id="de623-125">`ckSize` indica la dimensione dei dati validi nel blocco. non include la spaziatura interna, la dimensione `ckID` o la dimensione di `ckSize` .</span><span class="sxs-lookup"><span data-stu-id="de623-125">`ckSize` gives the size of the valid data in the chunk; it does not include the padding, the size of `ckID`, or the size of `ckSize`.</span></span>

-   <span data-ttu-id="de623-126">Un elenco ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="de623-126">A list has the following form:</span></span>

    `'LIST' listSize listType listData`

    <span data-ttu-id="de623-127">dove "LIST" è il valore letterale FOURCC code "LIST", `listSize` è un valore a 4 byte che assegna la dimensione dell'elenco, `listType` è un codice FourCC ed è `listData` costituito da blocchi o elenchi, in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="de623-127">where 'LIST' is the literal FOURCC code 'LIST', `listSize` is a 4-byte value giving the size of the list, `listType` is a FOURCC code, and `listData` consists of chunks or lists, in any order.</span></span> <span data-ttu-id="de623-128">Il valore di `listSize` include le dimensioni di `listType` più le dimensioni di `listData` ; non include il FourCC ' List ' o la dimensione di `listSize` .</span><span class="sxs-lookup"><span data-stu-id="de623-128">The value of `listSize` includes the size of `listType` plus the size of `listData`; it does not include the 'LIST' FOURCC or the size of `listSize`.</span></span>

<span data-ttu-id="de623-129">Il resto di questa sezione usa la notazione seguente per descrivere i blocchi RIFF:</span><span class="sxs-lookup"><span data-stu-id="de623-129">The remainder of this section uses the following notation to describe RIFF chunks:</span></span>

`ckID ( ckData )`

<span data-ttu-id="de623-130">dove le dimensioni del blocco sono implicite.</span><span class="sxs-lookup"><span data-stu-id="de623-130">where the chunk size is implicit.</span></span> <span data-ttu-id="de623-131">Utilizzando questa notazione, un elenco può essere rappresentato come:</span><span class="sxs-lookup"><span data-stu-id="de623-131">Using this notation, a list can be represented as:</span></span>

`'LIST' ( listType ( listData ) )`

<span data-ttu-id="de623-132">Gli elementi facoltativi sono racchiusi tra parentesi quadre: `[ optional element ]`</span><span class="sxs-lookup"><span data-stu-id="de623-132">Optional elements are placed in brackets: `[ optional element ]`</span></span>

## <a name="avi-riff-form"></a><span data-ttu-id="de623-133">Formato AVI RIFF</span><span class="sxs-lookup"><span data-stu-id="de623-133">AVI RIFF Form</span></span>

<span data-ttu-id="de623-134">I file AVI sono identificati da FOURCC ' AVI ' nell'intestazione RIFF.</span><span class="sxs-lookup"><span data-stu-id="de623-134">AVI files are identified by the FOURCC 'AVI ' in the RIFF header.</span></span> <span data-ttu-id="de623-135">Tutti i file AVI includono due blocchi elenco obbligatori, che definiscono rispettivamente il formato dei flussi e i dati di flusso.</span><span class="sxs-lookup"><span data-stu-id="de623-135">All AVI files include two mandatory LIST chunks, which define the format of the streams and the stream data, respectively.</span></span> <span data-ttu-id="de623-136">Un file AVI può includere anche un blocco dell'indice, che fornisce la posizione dei blocchi di dati all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="de623-136">An AVI file might also include an index chunk, which gives the location of the data chunks within the file.</span></span> <span data-ttu-id="de623-137">Un file AVI con questi componenti ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="de623-137">An AVI file with these components has the following form:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



<span data-ttu-id="de623-138">L'elenco ' hdrl ' definisce il formato dei dati ed è il primo blocco di elenco richiesto.</span><span class="sxs-lookup"><span data-stu-id="de623-138">The 'hdrl' list defines the format of the data and is the first required LIST chunk.</span></span> <span data-ttu-id="de623-139">L'elenco ' movi ' contiene i dati per la sequenza AVI ed è il secondo blocco elenco obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="de623-139">The 'movi' list contains the data for the AVI sequence and is the second required LIST chunk.</span></span> <span data-ttu-id="de623-140">L'elenco ' IDX1' contiene l'indice.</span><span class="sxs-lookup"><span data-stu-id="de623-140">The 'idx1' list contains the index.</span></span> <span data-ttu-id="de623-141">I file AVI devono contenere questi tre componenti nella sequenza corretta.</span><span class="sxs-lookup"><span data-stu-id="de623-141">AVI files must keep these three components in the proper sequence.</span></span>

> [!Note]  
> <span data-ttu-id="de623-142">Le estensioni OpenDML definiscono un altro tipo di indice, identificato da FOURCC ' indx '.</span><span class="sxs-lookup"><span data-stu-id="de623-142">The OpenDML extensions define another type of index, identified by the FOURCC 'indx'.</span></span>

 

<span data-ttu-id="de623-143">Gli elenchi ' hdrl ' è movi ' usano i sottoblocchi per i dati.</span><span class="sxs-lookup"><span data-stu-id="de623-143">The 'hdrl' and 'movi' lists use subchunks for their data.</span></span> <span data-ttu-id="de623-144">Nell'esempio seguente viene illustrato il formato AVI RIFF espanso con i blocchi necessari per completare gli elenchi:</span><span class="sxs-lookup"><span data-stu-id="de623-144">The following example shows the AVI RIFF form expanded with the chunks needed to complete these lists:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a><span data-ttu-id="de623-145">Intestazione principale AVI</span><span class="sxs-lookup"><span data-stu-id="de623-145">AVI Main Header</span></span>

<span data-ttu-id="de623-146">L'elenco ' hdrl ' inizia con l'intestazione AVI principale, che è contenuta in un blocco ' AVIH '.</span><span class="sxs-lookup"><span data-stu-id="de623-146">The 'hdrl' list begins with the main AVI header, which is contained in an 'avih' chunk.</span></span> <span data-ttu-id="de623-147">L'intestazione principale contiene informazioni globali per l'intero file AVI, ad esempio il numero di flussi all'interno del file e la larghezza e l'altezza della sequenza AVI.</span><span class="sxs-lookup"><span data-stu-id="de623-147">The main header contains global information for the entire AVI file, such as the number of streams within the file and the width and height of the AVI sequence.</span></span> <span data-ttu-id="de623-148">Il blocco principale dell'intestazione è costituito da una struttura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="de623-148">The main header chunk consists of an [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

## <a name="avi-stream-headers"></a><span data-ttu-id="de623-149">Intestazioni del flusso AVI</span><span class="sxs-lookup"><span data-stu-id="de623-149">AVI Stream Headers</span></span>

<span data-ttu-id="de623-150">Uno o più elenchi ' STRl ' seguono l'intestazione principale.</span><span class="sxs-lookup"><span data-stu-id="de623-150">One or more 'strl' lists follow the main header.</span></span> <span data-ttu-id="de623-151">Per ogni flusso di dati è necessario un elenco ' STRl '.</span><span class="sxs-lookup"><span data-stu-id="de623-151">A 'strl' list is required for each data stream.</span></span> <span data-ttu-id="de623-152">Ogni elenco ' STRl ' contiene informazioni su un flusso nel file e deve contenere un blocco di intestazione del flusso (' Strh ') e un blocco di formato del flusso (' strF ').</span><span class="sxs-lookup"><span data-stu-id="de623-152">Each 'strl' list contains information about one stream in the file, and must contain a stream header chunk ('strh') and a stream format chunk ('strf').</span></span> <span data-ttu-id="de623-153">Inoltre, un elenco ' STRl ' potrebbe contenere un blocco di dati di intestazione del flusso (' Strd ') e un blocco del nome del flusso (' STRN ').</span><span class="sxs-lookup"><span data-stu-id="de623-153">In addition, a 'strl' list might contain a stream-header data chunk ('strd') and a stream name chunk ('strn').</span></span>

<span data-ttu-id="de623-154">Il blocco di intestazione del flusso (' Strh ') è costituito da una struttura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .</span><span class="sxs-lookup"><span data-stu-id="de623-154">The stream header chunk ('strh') consists of an [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure.</span></span>

<span data-ttu-id="de623-155">Un blocco di formato del flusso (' strF ') deve seguire il blocco dell'intestazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="de623-155">A stream format chunk ('strf') must follow the stream header chunk.</span></span> <span data-ttu-id="de623-156">Il blocco formato flusso descrive il formato dei dati nel flusso.</span><span class="sxs-lookup"><span data-stu-id="de623-156">The stream format chunk describes the format of the data in the stream.</span></span> <span data-ttu-id="de623-157">I dati contenuti in questo blocco dipendono dal tipo di flusso.</span><span class="sxs-lookup"><span data-stu-id="de623-157">The data contained in this chunk depends on the stream type.</span></span> <span data-ttu-id="de623-158">Per i flussi video, le informazioni sono una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , incluse le informazioni sulla tavolozza, se appropriato.</span><span class="sxs-lookup"><span data-stu-id="de623-158">For video streams, the information is a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, including palette information if appropriate.</span></span> <span data-ttu-id="de623-159">Per i flussi audio, le informazioni sono una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="de623-159">For audio streams, the information is a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="de623-160">Se il blocco di dati dell'intestazione del flusso (' Strd ') è presente, segue il blocco del formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="de623-160">If the stream-header data ('strd') chunk is present, it follows the stream format chunk.</span></span> <span data-ttu-id="de623-161">Il formato e il contenuto di questo blocco sono definiti dal driver del codec.</span><span class="sxs-lookup"><span data-stu-id="de623-161">The format and content of this chunk are defined by the codec driver.</span></span> <span data-ttu-id="de623-162">In genere, i driver utilizzano queste informazioni per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="de623-162">Typically, drivers use this information for configuration.</span></span> <span data-ttu-id="de623-163">Le applicazioni che leggono e scrivono file AVI non devono interpretare queste informazioni; il trasferimento è semplice da e verso il driver come blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="de623-163">Applications that read and write AVI files do not need to interpret this information; they simple transfer it to and from the driver as a memory block.</span></span>

<span data-ttu-id="de623-164">Il blocco facoltativo ' STRN ' contiene una stringa di testo con terminazione null che descrive il flusso.</span><span class="sxs-lookup"><span data-stu-id="de623-164">The optional 'strn' chunk contains a null-terminated text string describing the stream.</span></span>

<span data-ttu-id="de623-165">Le intestazioni del flusso nell'elenco "hdrl" sono associate ai dati del flusso nell'elenco "movi" in base all'ordine dei blocchi "STRl".</span><span class="sxs-lookup"><span data-stu-id="de623-165">The stream headers in the 'hdrl' list are associated with the stream data in the 'movi' list according to the order of the 'strl' chunks.</span></span> <span data-ttu-id="de623-166">Il primo blocco ' STRl ' si applica al flusso 0, il secondo si applica al flusso 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="de623-166">The first 'strl' chunk applies to stream 0, the second applies to stream 1, and so forth.</span></span>

## <a name="stream-data-movi-list"></a><span data-ttu-id="de623-167">Dati di flusso (elenco ' movi ')</span><span class="sxs-lookup"><span data-stu-id="de623-167">Stream Data ('movi' List)</span></span>

<span data-ttu-id="de623-168">Le informazioni di intestazione sono un elenco ' movi ' che contiene i dati effettivi nei flussi, ovvero i fotogrammi video e gli esempi audio.</span><span class="sxs-lookup"><span data-stu-id="de623-168">Following the header information is a 'movi' list that contains the actual data in the streams—that is, the video frames and audio samples.</span></span> <span data-ttu-id="de623-169">I blocchi di dati possono trovarsi direttamente nell'elenco ' movi ' oppure possono essere raggruppati all'interno degli elenchi ' REC '.</span><span class="sxs-lookup"><span data-stu-id="de623-169">The data chunks can reside directly in the 'movi' list, or they might be grouped within 'rec ' lists.</span></span> <span data-ttu-id="de623-170">Il raggruppamento ' REC ' implica che i blocchi raggruppati devono essere letti dal disco in una sola volta ed è destinato a file con interfoliazione per la riproduzione da CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="de623-170">The 'rec ' grouping implies that the grouped chunks should be read from disk all at once, and is intended for files that are interleaved to play from CD-ROM.</span></span>

<span data-ttu-id="de623-171">Il FOURCC che identifica ogni blocco di dati è costituito da un numero di flusso a due cifre seguito da un codice di due caratteri che definisce il tipo di informazioni nel blocco.</span><span class="sxs-lookup"><span data-stu-id="de623-171">The FOURCC that identifies each data chunk consists of a two-digit stream number followed by a two-character code that defines the type of information in the chunk.</span></span>



| <span data-ttu-id="de623-172">Codice a due caratteri</span><span class="sxs-lookup"><span data-stu-id="de623-172">Two-character code</span></span> | <span data-ttu-id="de623-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de623-173">Description</span></span>              |
|--------------------|--------------------------|
| <span data-ttu-id="de623-174">db</span><span class="sxs-lookup"><span data-stu-id="de623-174">db</span></span>                 | <span data-ttu-id="de623-175">Fotogramma video non compresso</span><span class="sxs-lookup"><span data-stu-id="de623-175">Uncompressed video frame</span></span> |
| <span data-ttu-id="de623-176">dc</span><span class="sxs-lookup"><span data-stu-id="de623-176">dc</span></span>                 | <span data-ttu-id="de623-177">Fotogramma video compresso</span><span class="sxs-lookup"><span data-stu-id="de623-177">Compressed video frame</span></span>   |
| <span data-ttu-id="de623-178">pc</span><span class="sxs-lookup"><span data-stu-id="de623-178">pc</span></span>                 | <span data-ttu-id="de623-179">Modifica tavolozza</span><span class="sxs-lookup"><span data-stu-id="de623-179">Palette change</span></span>           |
| <span data-ttu-id="de623-180">WB</span><span class="sxs-lookup"><span data-stu-id="de623-180">wb</span></span>                 | <span data-ttu-id="de623-181">Dati audio</span><span class="sxs-lookup"><span data-stu-id="de623-181">Audio data</span></span>               |



 

<span data-ttu-id="de623-182">Se, ad esempio, il flusso 0 contiene audio, i blocchi di dati per quel flusso avranno il FOURCC ' 00wb '.</span><span class="sxs-lookup"><span data-stu-id="de623-182">For example, if stream 0 contains audio, the data chunks for that stream would have the FOURCC '00wb'.</span></span> <span data-ttu-id="de623-183">Se Stream 1 contiene video, i blocchi di dati per quel flusso avranno FOURCC ' 01dB ' o ' 01DC '.</span><span class="sxs-lookup"><span data-stu-id="de623-183">If stream 1 contains video, the data chunks for that stream would have the FOURCC '01db' or '01dc'.</span></span> <span data-ttu-id="de623-184">I blocchi di dati video possono anche definire nuove voci della tavolozza per aggiornare la tavolozza durante una sequenza AVI.</span><span class="sxs-lookup"><span data-stu-id="de623-184">Video data chunks can also define new palette entries to update the palette during an AVI sequence.</span></span> <span data-ttu-id="de623-185">Ogni tavolozza-Modifica blocco (' xxpc ') contiene una struttura [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) .</span><span class="sxs-lookup"><span data-stu-id="de623-185">Each palette-change chunk ('xxpc') contains an [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) structure.</span></span> <span data-ttu-id="de623-186">Se un flusso contiene modifiche della tavolozza, impostare il flag **AVISF \_ video \_ PALCHANGES** nel membro **dwFlags** della struttura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) per quel flusso.</span><span class="sxs-lookup"><span data-stu-id="de623-186">If a stream contains palette changes, set the **AVISF\_VIDEO\_PALCHANGES** flag in the **dwFlags** member of the [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure for that stream.</span></span>

<span data-ttu-id="de623-187">I flussi di testo possono utilizzare codici arbitrari di due caratteri.</span><span class="sxs-lookup"><span data-stu-id="de623-187">Text streams can use arbitrary two-character codes.</span></span>

## <a name="avi-index-entries"></a><span data-ttu-id="de623-188">Voci di indice AVI</span><span class="sxs-lookup"><span data-stu-id="de623-188">AVI Index Entries</span></span>

<dl> <dt>

<span data-ttu-id="de623-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Indice AVI 1,0</span><span class="sxs-lookup"><span data-stu-id="de623-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 index</span></span>
</dt> <dd>

<span data-ttu-id="de623-190">Un blocco index (' IDX1') facoltativo può seguire l'elenco ' movi '.</span><span class="sxs-lookup"><span data-stu-id="de623-190">An optional index ('idx1') chunk can follow the 'movi' list.</span></span> <span data-ttu-id="de623-191">L'indice contiene un elenco dei blocchi di dati e la relativa posizione nel file.</span><span class="sxs-lookup"><span data-stu-id="de623-191">The index contains a list of the data chunks and their location in the file.</span></span> <span data-ttu-id="de623-192">È costituito da una struttura [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) con le voci per ogni blocco di dati, inclusi i blocchi "REC".</span><span class="sxs-lookup"><span data-stu-id="de623-192">It consists of an [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) structure with entries for each data chunk, including 'rec ' chunks.</span></span> <span data-ttu-id="de623-193">Se il file contiene un indice, impostare il flag **AVIF \_ HASINDEX** nel membro **dwFlags** della struttura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="de623-193">If the file contains an index, set the **AVIF\_HASINDEX** flag in the **dwFlags** member of the [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="de623-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Indice AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="de623-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 index</span></span>
</dt> <dd>

<span data-ttu-id="de623-195">Un indice AVI 2,0 può essere visualizzato come singolo blocco.</span><span class="sxs-lookup"><span data-stu-id="de623-195">An AVI 2.0 index can appear as a single chunk.</span></span> <span data-ttu-id="de623-196">In alternativa, i segmenti di indice possono essere interfogliati all'interno del blocco ' movi '.</span><span class="sxs-lookup"><span data-stu-id="de623-196">Alternatively, index segments can be interleaved within the 'movi' chunk.</span></span> <span data-ttu-id="de623-197">Se i segmenti di indice vengono posizionati nel blocco ' movi ', un indice Super contiene un indice dei segmenti di indice.</span><span class="sxs-lookup"><span data-stu-id="de623-197">If the index segments are placed in the 'movi' chunk, a super index contains an index of the index segments.</span></span> <span data-ttu-id="de623-198">La struttura [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) è la struttura di base per i segmenti di indice e per l'indice con privilegi avanzati.</span><span class="sxs-lookup"><span data-stu-id="de623-198">The [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) structure is the base structure for both the index segments and the super index.</span></span> <span data-ttu-id="de623-199">Per altre informazioni, vedere le *estensioni di formato file AVI di OpenDML*, pubblicate dal sottocomitato formato file OpenDML AVI M-JPEG.</span><span class="sxs-lookup"><span data-stu-id="de623-199">For more information, see the *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span> <span data-ttu-id="de623-200">Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.</span><span class="sxs-lookup"><span data-stu-id="de623-200">(This resource may not be available in some languages and countries.)</span></span>

</dd> </dl>

## <a name="other-data-chunks"></a><span data-ttu-id="de623-201">Altri blocchi di dati</span><span class="sxs-lookup"><span data-stu-id="de623-201">Other Data Chunks</span></span>

<span data-ttu-id="de623-202">I dati possono essere allineati in un file AVI inserendo i blocchi ' JUNK ' in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="de623-202">Data can be aligned in an AVI file by inserting 'JUNK' chunks as needed.</span></span> <span data-ttu-id="de623-203">Le applicazioni devono ignorare il contenuto di un blocco "JUNK".</span><span class="sxs-lookup"><span data-stu-id="de623-203">Applications should ignore the contents of a 'JUNK' chunk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de623-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de623-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de623-205">Formato file AVI</span><span class="sxs-lookup"><span data-stu-id="de623-205">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
