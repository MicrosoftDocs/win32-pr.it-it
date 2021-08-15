---
title: Lettura da un flusso
description: Lettura da un flusso
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- Funzione AVIStreamInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c56e1bd34fb9b0555c4eb0ed86944be3b7603645865144ac053604cd515cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371651"
---
# <a name="reading-from-a-stream"></a>Lettura da un flusso

È possibile recuperare informazioni su un flusso aperto usando la [**funzione AVIStreamInfo.**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) Questa funzione riempie la struttura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) con informazioni quali il tipo di dati nel flusso, il metodo di compressione usato per la scrittura dei dati del flusso, le dimensioni del buffer suggerite, la velocità di riproduzione e una descrizione di testo del flusso.

Alcuni membri della [**struttura AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) sono presenti anche nella [**struttura AVIFILEINFO.**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) Le informazioni nella **struttura AVIFILEINFO** si applicano all'intero file. Le informazioni nella **struttura AVISTREAMINFO** sono specifiche del flusso a cui si accede e hanno la precedenza sulle informazioni nella **struttura AVIFILEINFO.**

Se a un flusso sono associate informazioni supplementari, è possibile recuperare queste informazioni usando la [**funzione AVIStreamReadData.**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) Questa funzione restituisce le informazioni in un buffer fornito dall'applicazione. Le informazioni supplementari sul flusso possono includere impostazioni di configurazione per i metodi di compressione e decompressione usati in un flusso. È possibile ottenere le dimensioni del buffer richieste usando la macro [**AVIStreamDataSize.**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)

È possibile recuperare informazioni di formattazione su un flusso usando la [**funzione AVIStreamReadFormat.**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) Questa funzione restituisce una struttura specifica del flusso in un buffer fornito dall'applicazione. Per un flusso video, il buffer contiene informazioni di formattazione in una [**struttura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Per un flusso audio, il buffer contiene informazioni di formattazione in [**una struttura WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) [**o PCMWAVEFORMAT.**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) Per altri tipi di flusso, il gestore del flusso restituisce informazioni specifiche del flusso. È possibile determinare le dimensioni del buffer richieste usando **AVIStreamReadFormat** e specificando un indirizzo di buffer **NULL** o la macro [**AVIStreamFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)

È possibile recuperare il contenuto multimediale in un flusso usando la [**funzione AVIStreamRead.**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) Questa funzione copia i dati non elaborati dal flusso in un buffer fornito dall'applicazione. Per i flussi video, questa funzione recupera le immagini bitmap che costituiscono il contenuto del fotogramma. Per i flussi audio, questa funzione recupera campioni audio-forma d'onda che costituiscono il contenuto audio. È possibile determinare le dimensioni del buffer richieste usando **AVIStreamRead** e specificando un indirizzo di buffer **NULL** o la macro [**AVIStreamSampleSize.**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)

Alcuni gestori di flusso AVI introducono ritardi associati all'inizializzazione o al coordinamento di software e hardware. È possibile informare questi gestori di prepararsi per il flusso di dati usando la [**funzione AVIStreamBeginStreaming.**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) Questa funzione consente al gestore del flusso di allocare e inizializzare le risorse necessarie. Per informare questi gestori al termine del flusso, usare la [**funzione AVIStreamEndStreaming.**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) Questa funzione consente al gestore di flusso di deallocare le risorse allocate per **AVIStreamBeginStreaming.**

La [**funzione AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) non fornisce servizi di decompressione. Per informazioni sulla compressione e la decompressione dei flussi audio, vedere [Gestione compressione audio.](audio-compression-manager.md) Per informazioni sulla compressione e la decompressione dei flussi video, vedere [Gestione compressione video.](video-compression-manager.md) Per informazioni sulla compressione e la decompressione di singoli fotogrammi in un flusso video, vedere Uso di [dati video compressi in un flusso.](working-with-compressed-video-data-in-a-stream.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di flusso](stream-operations.md)
</dt> </dl>

 

 