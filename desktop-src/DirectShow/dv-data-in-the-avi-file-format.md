---
description: Dati DV nel formato di file AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Dati DV nel formato di file AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c048cb42fa3ba49457c115944075c064b9cfd4c31263519e9d5af3e5f0a268a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749111"
---
# <a name="dv-data-in-the-avi-file-format"></a>Dati DV nel formato di file AVI

Microsoft ha specificato il formato per l'archiviazione dei dati video digitali (DV) nei file AVI. La conformità a questa specifica garantisce che i file AVI creati in questo formato siano compatibili con le versioni future dell'architettura video digitale di DirectShow per Windowsplatform.

Questo articolo descrive il formato dei file AVI contenenti dati DV. Sono definiti QUATTROCC (codici a quattro caratteri) specifici per i flussi di dati DV interleaved e i gestori di flussi di compressione/decompressione DV. La struttura del formato di flusso per i dati DV è definita. Vengono specificate le specifiche per due metodi di archiviazione dei dati DV nel formato di file AVI.

Si presuppone che il lettore abbia familiarità con il formato dati DV. Questo formato è definito nella specifica dei videoregistratori digitali per uso *consumer,* denominata anche Blue Book.

Esistono due tipi di file AVI DV: file AVI che contengono un flusso di dati DV, denominati *file di tipo 1;* e file AVI che contengono video DV come flusso "vids" e audio DV come flussi "auds", detti file *di tipo 2.*

**File AVI contenenti un flusso di dati DV (tipo-1)**

I dati DV interleaved possono essere archiviati nel formato nativo come flusso singolo all'interno di un file RIFF AVI. Ciò ha il vantaggio di usare la quantità minima di archiviazione dei dati per DV. Lo svantaggio principale è che questo formato di file non è compatibile con le versioni precedenti di Video per Windows, perché non contiene un flusso video 'vids' o audio 'auds'. Viene fornito il supporto per il flusso DV interleaved tramite i filtri [DV Muxer](dv-muxer-filter.md) e [DV Splitter](dv-splitter-filter.md) forniti con DirectShow.

I dati DV possono essere archiviati in un singolo flusso all'interno di un file RIFF AVI specificando "iavs" (flusso audio e video interleaved) FOURCC (codice a quattro caratteri) nel membro **fccType** e uno dei blocchi di intestazione del flusso 'dvsd', 'dvhd' o 'dvsl' FOURCC nel membro **fccHandler** del blocco di intestazione del flusso 'strh'. I fotogrammi al secondo del flusso video devono essere specificati nei membri **dwRate** e **dwScale** e il numero totale di blocchi video nel blocco 'movi' nel membro **dwLength.**

Il gestore di flusso "dvsd" FOURCC specifica che i dati DV sono definiti nella parte 2 della specifica dei videoregistratori digitali *consumer-use*. Il formato del video è di 525 righe a 29,97 Hz (525-60) o di 625 righe a 25,00 Hz (625-50).

Il gestore di flusso "dvhd" FOURCC specifica che i dati DV sono definiti nella parte 3 della specifica dei videoregistratori digitali *consumer-use*. Il formato del video è di 1125 righe a 30,00 Hz (1125-60) o di 1250 righe a 25,00 Hz (1250-50).

Il gestore di flusso "dvsl" FOURCC specifica che i dati DV sono definiti nella parte 6 della specifica dei videoregistratori digitali per uso *consumer.* Il formato del video è SD (SDL) a compressione elevata.

> [!Note]  
> Il resto di questo articolo fornisce le definizioni per i flussi 'dvsd'.

 

Il blocco di intestazione del flusso deve essere seguito da un blocco [**di formato di flusso DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo)

I dati DV effettivi vengono archiviati come blocchi 'dc' nel blocco \# \# 'movi' (nel formato rappresenta \# \# l'identificatore di flusso). Ogni blocco contiene un frame di dati, rispettivamente 10 o 12 sequenze DIF DV per 525-60 o 625-50 sistemi. Il formato di sequenza DIF DV SD ('dvsd') è definito nella parte 2 della specifica dei videoregistratori digitali *consumer-use*.

L'esempio seguente mostra il modulo AIFF RIFF per un file AVI con un flusso di dati DV, espanso con blocchi di intestazione completati.


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



**File AVI contenenti video DV e audio DV Flussi (tipo 2)**

I dati DV interleaved possono essere suddivisi in un flusso video e da uno a quattro flussi audio all'interno di un file RIFF AVI. Questo ha il vantaggio di essere compatibile con le versioni precedenti di Video per Windows, perché contiene un flusso "vids" video standard e almeno un flusso "auds" audio standard Lo svantaggio principale è che questo formato di file richiede che i dati audio vengano archiviati in modo ridondante come flussi audio. Il flusso "video" è in realtà il flusso di dati DV interleaved nativo. Tuttavia, come flusso "vids" standard con un tipo di gestore "dvsd", viene usato il decodificatore [video DV.](dv-video-decoder-filter.md) Questo formato richiede anche l'uso del filtro [DV Splitter](dv-splitter-filter.md) per dividere i file "acquisiti" prima di scriverli come file AVI.

I dati DV possono essere archiviati come flusso video con un numero separato di flussi audio in un file RIFF AVI. Il flusso video viene specificato con un'intestazione di flusso video standard (il valore del membro **fccType** è 'vids'). Il **membro fccHandler** è specificato come 'dvsd', 'dvhd' o 'dvsl'. I fotogrammi al secondo del flusso video devono essere specificati nei membri **dwRate** e **dwScale** e il numero totale di blocchi video nel blocco 'movi' nel membro **dwLength.**

In questo file AVI contenente video DV come flusso "vids" e audio DV come flussi "auds" forma di DV, il blocco di formato del flusso video è una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) standard. Il blocco di formato del flusso può essere esteso facoltativamente per includere il blocco [**DVINFO,**](/windows/desktop/api/strmif/ns-strmif-dvinfo) aumentando le dimensioni del blocco del formato di flusso da 40 byte (dimensione della struttura **BITMAPINFOHEADER)** a 72 byte (dimensioni **delle strutture BITMAPINFOHEADER** e **DVINFO)** e immediatamente dopo la struttura di dati **BITMAPINFOHEADER** con una struttura di dati **DVINFO.**

I flussi audio vengono specificati con un'intestazione di flusso audio standard (il valore del membro **fccType** è 'auds'). Il **membro fccHandler** non viene usato per i flussi audio.

I dati video DV vengono archiviati come blocchi 'dc', come definito nella descrizione precedente di un file AVI con un dato DV, e i dati audio vengono archiviati come blocchi 'wb' nel blocco \# \# \# \# 'movi'.

> [!Note]  
> La *specifica dei videoregistratori digitali per* uso consumer potrebbe non essere disponibile in alcune lingue e paesi.

 

L'esempio seguente mostra il modulo AIFF RIFF per un file AVI contenente video DV come flusso "vids" e audio DV come flussi "auds" espansi con blocchi di intestazione completati (inclusi i dati [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) facoltativi che segue [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) nel sotto chunk 'strf' per il flusso 'vids').


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

[Formato di file AVI](avi-file-format.md)
</dt> </dl>

 

 
