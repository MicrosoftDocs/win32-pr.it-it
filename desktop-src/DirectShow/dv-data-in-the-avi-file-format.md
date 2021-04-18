---
description: Dati DV nel formato di file AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Dati DV nel formato di file AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482389"
---
# <a name="dv-data-in-the-avi-file-format"></a><span data-ttu-id="9cf5a-103">Dati DV nel formato di file AVI</span><span class="sxs-lookup"><span data-stu-id="9cf5a-103">DV Data in the AVI File Format</span></span>

<span data-ttu-id="9cf5a-104">Microsoft ha specificato il formato per l'archiviazione dei dati video digitali (DV) in file AVI.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-104">Microsoft has specified the format for storage of digital video (DV) data in AVI files.</span></span> <span data-ttu-id="9cf5a-105">La conformità a questa specifica garantisce che i file AVI creati in questo formato saranno compatibili con le versioni future dell'architettura video digitale DirectShow per Windowsplatform.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-105">Conforming to this specification will ensure that the AVI files authored in this format will be compatible with future versions of the DirectShow digital video architecture for the Windowsplatform.</span></span>

<span data-ttu-id="9cf5a-106">Questo articolo descrive il formato dei file AVI contenenti dati DV.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-106">This article describes the format of AVI files containing DV data.</span></span> <span data-ttu-id="9cf5a-107">Sono definiti FourCC specifici (codici a quattro caratteri) per i flussi di dati DV Interleaved e i gestori di flussi di Compressor/decompressore DV.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-107">Specific FOURCCs (four-character codes) for interleaved DV data streams and DV compressor/decompressor stream handlers are defined.</span></span> <span data-ttu-id="9cf5a-108">La struttura del formato del flusso per i dati DV è definita.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-108">The stream format structure for DV data is defined.</span></span> <span data-ttu-id="9cf5a-109">Vengono specificate le specifiche per due metodi di archiviazione dei dati DV nel formato di file AVI.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-109">Specifications for two methods of storing DV data in the AVI file format are specified.</span></span>

<span data-ttu-id="9cf5a-110">Si presuppone che il lettore abbia familiarità con il formato di dati DV.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-110">It is assumed that the reader is familiar with the DV data format.</span></span> <span data-ttu-id="9cf5a-111">Questo formato è definito nella *specifica dei VCR digitali utilizzati dall'utente*, noto anche come libro blu.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-111">(This format is defined in the *Specification of Consumer-use Digital VCRs*, also called the Blue Book.)</span></span>

<span data-ttu-id="9cf5a-112">Sono disponibili due tipi di file AVI DV: file AVI contenenti un flusso di dati DV, denominati file di *tipo 1* ; e file AVI che contengono video DV come flusso "vids" e audio DV come flussi "Auds", denominati file di *tipo 2* .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-112">There are two types of DV AVI files: AVI files that contain one DV data stream, called *type-1* files; and AVI files that contain DV video as a 'vids' stream and DV audio as 'auds' streams, called *type-2* files.</span></span>

<span data-ttu-id="9cf5a-113">**File AVI contenenti un flusso di dati DV (tipo 1)**</span><span class="sxs-lookup"><span data-stu-id="9cf5a-113">**AVI Files Containing One DV Data Stream (Type-1)**</span></span>

<span data-ttu-id="9cf5a-114">I dati DV con interfoliazione possono essere archiviati nel formato nativo come singolo flusso all'interno di un file con estensione AVI.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-114">Interleaved DV data can be stored in its native format as a single stream within an AVI RIFF file.</span></span> <span data-ttu-id="9cf5a-115">Questo ha il vantaggio di usare la quantità minima di archiviazione dei dati per DV.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-115">This has the advantage of using the minimum amount of data storage for DV.</span></span> <span data-ttu-id="9cf5a-116">Lo svantaggio principale è che questo formato di file non è compatibile con le versioni precedenti del video per Windows, perché non contiene un video ' vids ' o un flusso audio ' Auds '.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-116">The primary disadvantage is that this file format is not backward-compatible with Video for Windows, because it doesn't contain either a video 'vids' or an audio 'auds' stream.</span></span> <span data-ttu-id="9cf5a-117">Viene fornito supporto per il flusso DV con interfoliazione tramite i filtri [DV muxer](dv-muxer-filter.md) e [DV Splitter](dv-splitter-filter.md) forniti con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-117">Support is provided for the interleaved DV stream through the [DV Muxer](dv-muxer-filter.md) and [DV Splitter](dv-splitter-filter.md) filters provided with DirectShow.</span></span>

<span data-ttu-id="9cf5a-118">I dati DV possono essere archiviati in un singolo flusso all'interno di un file AVI RIFF specificando ' iAVS ' (flusso audio e video con interfoliazione) FOURCC (codice a quattro caratteri) nel membro **fccType** e uno dei ' DVSD ',' DVHD ' o ' Dvsl ' FourCC nel membro **fccHandler** del blocco dell'intestazione del flusso ' Strh '.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-118">DV data can be stored in a single stream within an AVI RIFF file by specifying the 'iavs' (interleaved audio and video stream) FOURCC (four-character code) in the **fccType** member and either of the 'dvsd', 'dvhd', or 'dvsl' FOURCCs in the **fccHandler** member of the 'strh' stream header chunk.</span></span> <span data-ttu-id="9cf5a-119">I frame al secondo del flusso video devono essere specificati nei membri **dwRate** e **dwScale** e il numero totale di blocchi video nel blocco ' movi ' del membro **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-119">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="9cf5a-120">Il gestore di flusso ' DVSD ' FOURCC specifica che i dati DV sono definiti nella parte 2 della *specifica dei VCR digitali usati dall'utente*.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-120">The 'dvsd' stream handler FOURCC specifies that the DV data is as defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="9cf5a-121">Il formato del video è 525 righe a 29,97 Hz (525-60) o 625 righe a 25,00 Hz (625-50).</span><span class="sxs-lookup"><span data-stu-id="9cf5a-121">Video is in the format of 525 lines at 29.97 Hz (525-60) or 625 lines at 25.00 Hz (625-50).</span></span>

<span data-ttu-id="9cf5a-122">Il gestore di flusso ' DVHD ' FOURCC specifica che i dati DV sono definiti nella parte 3 della *specifica dei VCR digitali usati dall'utente*.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-122">The 'dvhd' stream handler FOURCC specifies that the DV data is as defined in Part 3 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="9cf5a-123">Il formato del video è 1125 righe a 30,00 Hz (1125-60) o 1250 righe a 25,00 Hz (1250-50).</span><span class="sxs-lookup"><span data-stu-id="9cf5a-123">Video is in the format of 1125 lines at 30.00 Hz (1125-60) or 1250 lines at 25.00 Hz (1250-50).</span></span>

<span data-ttu-id="9cf5a-124">Il gestore del flusso ' dvsl ' FOURCC specifica che i dati DV sono definiti nella parte 6 della *specifica dei VCR digitali usati dall'utente*.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-124">The 'dvsl' stream handler FOURCC specifies that the DV data is as defined in Part 6 of *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="9cf5a-125">Il video è in formato SD (SDL) a compressione elevata.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-125">Video is in the format of high-compression SD (SDL).</span></span>

> [!Note]  
> <span data-ttu-id="9cf5a-126">Nella parte restante di questo articolo vengono fornite le definizioni per i flussi ' DVSD '.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-126">The remainder of this article provides definitions for 'dvsd' streams.</span></span>

 

<span data-ttu-id="9cf5a-127">Il blocco dell'intestazione del flusso deve essere seguito da un blocco di formato del flusso [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-127">The stream header chunk must be followed by a [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) stream format chunk.</span></span>

<span data-ttu-id="9cf5a-128">I dati DV effettivi vengono archiviati come \# \# blocchi ' DC ' nel blocco ' movi ' (il \# \# nel formato rappresenta l'identificatore del flusso).</span><span class="sxs-lookup"><span data-stu-id="9cf5a-128">The actual DV data is stored as '\#\#dc' chunks in the 'movi' chunk (the \#\# in the format represents the stream identifier).</span></span> <span data-ttu-id="9cf5a-129">Ogni blocco contiene un frame di dati, rispettivamente le sequenze 10 o 12 DV DIF per i sistemi 525-60 o 625-50.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-129">Each chunk contains one frame of data, either 10 or 12 DV DIF sequences for 525-60 or 625-50 systems, respectively.</span></span> <span data-ttu-id="9cf5a-130">Il formato di sequenza DIF DV SD (' DVSD ') è definito nella parte 2 della *specifica dei VCR digitali con uso del consumer*.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-130">The DV SD ('dvsd') DIF sequence format is defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span>

<span data-ttu-id="9cf5a-131">L'esempio seguente mostra il formato di AIFF RIFF per un file AVI con un flusso di dati DV, espanso con blocchi di intestazione completati.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-131">The following example shows the AIFF RIFF form for an AVI file with one DV data stream, expanded with completed header chunks.</span></span>


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



<span data-ttu-id="9cf5a-132">**File AVI contenenti video DV e flussi audio DV (tipo 2)**</span><span class="sxs-lookup"><span data-stu-id="9cf5a-132">**AVI Files Containing DV Video and DV Audio Streams (Type-2)**</span></span>

<span data-ttu-id="9cf5a-133">I dati DV con interfoliazione possono essere suddivisi in un flusso video e da uno a quattro flussi audio all'interno di un file con estensione AVI.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-133">Interleaved DV data can be split into a video stream and one to four audio streams within an AVI RIFF file.</span></span> <span data-ttu-id="9cf5a-134">Questo è il vantaggio di essere compatibile con le versioni precedenti del video per Windows, perché contiene un flusso video "vids" standard e almeno un flusso audio standard "Auds" lo svantaggio principale è che questo formato di file richiede che i dati audio siano archiviati in modo ridondante come flussi audio.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-134">This has the advantage of being backward-compatible with Video for Windows, because it contains a standard video 'vids' stream and at least one standard audio 'auds' stream The primary disadvantage is that this file format requires the audio data to be redundantly stored as audio streams.</span></span> <span data-ttu-id="9cf5a-135">Il flusso "video" è in realtà il flusso di dati DV Interleaved nativo.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-135">The "video" stream is actually the native interleaved DV data stream.</span></span> <span data-ttu-id="9cf5a-136">Tuttavia, come flusso "vids" standard con un tipo di gestore "dvsd", viene usato il [decodificatore video DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-136">However, as a standard 'vids' stream with a handler type of 'dvsd', the [DV Video Decoder](dv-video-decoder-filter.md) is used.</span></span> <span data-ttu-id="9cf5a-137">Questo formato richiede anche l'uso del filtro [splitter DV](dv-splitter-filter.md) per suddividere i file "acquisiti" prima di scriverli come file AVI.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-137">This format also requires using the [DV Splitter](dv-splitter-filter.md) filter to split "captured" files before writing them as AVI files.</span></span>

<span data-ttu-id="9cf5a-138">I dati DV possono essere archiviati come flusso video con un numero separato di flussi audio in un file con estensione AVI.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-138">DV data can be stored as a video stream with a separate number of audio streams in an AVI RIFF file.</span></span> <span data-ttu-id="9cf5a-139">Il flusso video viene specificato con un'intestazione del flusso video standard (il valore del membro **fccType** è' vids ').</span><span class="sxs-lookup"><span data-stu-id="9cf5a-139">The video stream is specified with a standard video stream header (the **fccType** member value is 'vids').</span></span> <span data-ttu-id="9cf5a-140">Il membro **fccHandler** è specificato come ' DVSD ',' DVHD ' o ' dvsl '.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-140">The **fccHandler** member is specified as 'dvsd', 'dvhd', or 'dvsl'.</span></span> <span data-ttu-id="9cf5a-141">I frame al secondo del flusso video devono essere specificati nei membri **dwRate** e **dwScale** e il numero totale di blocchi video nel blocco ' movi ' del membro **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-141">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="9cf5a-142">In questo file AVI che contiene video DV come flusso "vids" e audio DV come flussi "Auds" di DV, il blocco del formato del flusso video è una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) standard.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-142">In this AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams form of DV, the video stream format chunk is a standard [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="9cf5a-143">Il blocco di formato del flusso può essere esteso facoltativamente in modo da includere il blocco [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , aumentando la dimensione del blocco del formato del flusso da 40 byte (dimensione della struttura **BITMAPINFOHEADER** ) a 72 byte (dimensioni di **BITMAPINFOHEADER** più strutture **DVinfo** ) e immediatamente dopo la struttura dei dati **BITMAPINFOHEADER** con una struttura di dati **DVinfo** .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-143">The stream format chunk can be optionally extended to include the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) chunk, by increasing the stream format chunk size from 40 bytes (size of the **BITMAPINFOHEADER** structure) to 72 bytes (size of **BITMAPINFOHEADER** plus **DVINFO** structures) and immediately following the **BITMAPINFOHEADER** data structure with a **DVINFO** data structure.</span></span>

<span data-ttu-id="9cf5a-144">I flussi audio sono specificati con un'intestazione del flusso audio standard (il valore del membro **fccType** è' Auds ').</span><span class="sxs-lookup"><span data-stu-id="9cf5a-144">The audio stream(s) is specified with a standard audio stream header (the **fccType** member value is 'auds').</span></span> <span data-ttu-id="9cf5a-145">Il membro **fccHandler** non viene usato per i flussi audio.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-145">The **fccHandler** member is not used for audio streams.</span></span>

<span data-ttu-id="9cf5a-146">I dati video DV vengono archiviati come \# \# blocchi ' DC ', come definito nella precedente descrizione di un file AVI con un solo dato DV e i dati audio vengono archiviati come \# \# blocchi ' WB ' nel blocco ' movi '.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-146">The DV video data is stored as '\#\#dc' chunks, as defined in the preceding description of an AVI file with one DV data, and the audio data is stored as '\#\#wb' chunks in the 'movi' chunk.</span></span>

> [!Note]  
> <span data-ttu-id="9cf5a-147">La *specifica dei VCR digitali per l'uso dei consumer* potrebbe non essere disponibile in alcune lingue e paesi.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-147">The *Specification of Consumer-use Digital VCRs* may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="9cf5a-148">L'esempio seguente mostra il formato di AIFF RIFF per un file AVI che contiene video DV come flusso "vids" e audio DV come flussi "Auds" espansi con blocchi di intestazione completati (inclusi i dati [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) facoltativi che seguono il [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) nel sottoblocco "strF" per il flusso "vids").</span><span class="sxs-lookup"><span data-stu-id="9cf5a-148">The following example shows the AIFF RIFF form for an AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams expanded with completed header chunks (including optional [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) data following the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) in the 'strf' sub-chunk for the 'vids' stream).</span></span>


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a><span data-ttu-id="9cf5a-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cf5a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf5a-150">Formato file AVI</span><span class="sxs-lookup"><span data-stu-id="9cf5a-150">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
