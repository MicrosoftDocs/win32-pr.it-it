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
# <a name="dv-data-in-the-avi-file-format"></a>Dati DV nel formato di file AVI

Microsoft ha specificato il formato per l'archiviazione dei dati video digitali (DV) in file AVI. La conformità a questa specifica garantisce che i file AVI creati in questo formato saranno compatibili con le versioni future dell'architettura video digitale DirectShow per Windowsplatform.

Questo articolo descrive il formato dei file AVI contenenti dati DV. Sono definiti FourCC specifici (codici a quattro caratteri) per i flussi di dati DV Interleaved e i gestori di flussi di Compressor/decompressore DV. La struttura del formato del flusso per i dati DV è definita. Vengono specificate le specifiche per due metodi di archiviazione dei dati DV nel formato di file AVI.

Si presuppone che il lettore abbia familiarità con il formato di dati DV. Questo formato è definito nella *specifica dei VCR digitali utilizzati dall'utente*, noto anche come libro blu.

Sono disponibili due tipi di file AVI DV: file AVI contenenti un flusso di dati DV, denominati file di *tipo 1* ; e file AVI che contengono video DV come flusso "vids" e audio DV come flussi "Auds", denominati file di *tipo 2* .

**File AVI contenenti un flusso di dati DV (tipo 1)**

I dati DV con interfoliazione possono essere archiviati nel formato nativo come singolo flusso all'interno di un file con estensione AVI. Questo ha il vantaggio di usare la quantità minima di archiviazione dei dati per DV. Lo svantaggio principale è che questo formato di file non è compatibile con le versioni precedenti del video per Windows, perché non contiene un video ' vids ' o un flusso audio ' Auds '. Viene fornito supporto per il flusso DV con interfoliazione tramite i filtri [DV muxer](dv-muxer-filter.md) e [DV Splitter](dv-splitter-filter.md) forniti con DirectShow.

I dati DV possono essere archiviati in un singolo flusso all'interno di un file AVI RIFF specificando ' iAVS ' (flusso audio e video con interfoliazione) FOURCC (codice a quattro caratteri) nel membro **fccType** e uno dei ' DVSD ',' DVHD ' o ' Dvsl ' FourCC nel membro **fccHandler** del blocco dell'intestazione del flusso ' Strh '. I frame al secondo del flusso video devono essere specificati nei membri **dwRate** e **dwScale** e il numero totale di blocchi video nel blocco ' movi ' del membro **dwLength** .

Il gestore di flusso ' DVSD ' FOURCC specifica che i dati DV sono definiti nella parte 2 della *specifica dei VCR digitali usati dall'utente*. Il formato del video è 525 righe a 29,97 Hz (525-60) o 625 righe a 25,00 Hz (625-50).

Il gestore di flusso ' DVHD ' FOURCC specifica che i dati DV sono definiti nella parte 3 della *specifica dei VCR digitali usati dall'utente*. Il formato del video è 1125 righe a 30,00 Hz (1125-60) o 1250 righe a 25,00 Hz (1250-50).

Il gestore del flusso ' dvsl ' FOURCC specifica che i dati DV sono definiti nella parte 6 della *specifica dei VCR digitali usati dall'utente*. Il video è in formato SD (SDL) a compressione elevata.

> [!Note]  
> Nella parte restante di questo articolo vengono fornite le definizioni per i flussi ' DVSD '.

 

Il blocco dell'intestazione del flusso deve essere seguito da un blocco di formato del flusso [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

I dati DV effettivi vengono archiviati come \# \# blocchi ' DC ' nel blocco ' movi ' (il \# \# nel formato rappresenta l'identificatore del flusso). Ogni blocco contiene un frame di dati, rispettivamente le sequenze 10 o 12 DV DIF per i sistemi 525-60 o 625-50. Il formato di sequenza DIF DV SD (' DVSD ') è definito nella parte 2 della *specifica dei VCR digitali con uso del consumer*.

L'esempio seguente mostra il formato di AIFF RIFF per un file AVI con un flusso di dati DV, espanso con blocchi di intestazione completati.


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



**File AVI contenenti video DV e flussi audio DV (tipo 2)**

I dati DV con interfoliazione possono essere suddivisi in un flusso video e da uno a quattro flussi audio all'interno di un file con estensione AVI. Questo è il vantaggio di essere compatibile con le versioni precedenti del video per Windows, perché contiene un flusso video "vids" standard e almeno un flusso audio standard "Auds" lo svantaggio principale è che questo formato di file richiede che i dati audio siano archiviati in modo ridondante come flussi audio. Il flusso "video" è in realtà il flusso di dati DV Interleaved nativo. Tuttavia, come flusso "vids" standard con un tipo di gestore "dvsd", viene usato il [decodificatore video DV](dv-video-decoder-filter.md) . Questo formato richiede anche l'uso del filtro [splitter DV](dv-splitter-filter.md) per suddividere i file "acquisiti" prima di scriverli come file AVI.

I dati DV possono essere archiviati come flusso video con un numero separato di flussi audio in un file con estensione AVI. Il flusso video viene specificato con un'intestazione del flusso video standard (il valore del membro **fccType** è' vids '). Il membro **fccHandler** è specificato come ' DVSD ',' DVHD ' o ' dvsl '. I frame al secondo del flusso video devono essere specificati nei membri **dwRate** e **dwScale** e il numero totale di blocchi video nel blocco ' movi ' del membro **dwLength** .

In questo file AVI che contiene video DV come flusso "vids" e audio DV come flussi "Auds" di DV, il blocco del formato del flusso video è una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) standard. Il blocco di formato del flusso può essere esteso facoltativamente in modo da includere il blocco [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , aumentando la dimensione del blocco del formato del flusso da 40 byte (dimensione della struttura **BITMAPINFOHEADER** ) a 72 byte (dimensioni di **BITMAPINFOHEADER** più strutture **DVinfo** ) e immediatamente dopo la struttura dei dati **BITMAPINFOHEADER** con una struttura di dati **DVinfo** .

I flussi audio sono specificati con un'intestazione del flusso audio standard (il valore del membro **fccType** è' Auds '). Il membro **fccHandler** non viene usato per i flussi audio.

I dati video DV vengono archiviati come \# \# blocchi ' DC ', come definito nella precedente descrizione di un file AVI con un solo dato DV e i dati audio vengono archiviati come \# \# blocchi ' WB ' nel blocco ' movi '.

> [!Note]  
> La *specifica dei VCR digitali per l'uso dei consumer* potrebbe non essere disponibile in alcune lingue e paesi.

 

L'esempio seguente mostra il formato di AIFF RIFF per un file AVI che contiene video DV come flusso "vids" e audio DV come flussi "Auds" espansi con blocchi di intestazione completati (inclusi i dati [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) facoltativi che seguono il [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) nel sottoblocco "strF" per il flusso "vids").


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato file AVI](avi-file-format.md)
</dt> </dl>

 

 
