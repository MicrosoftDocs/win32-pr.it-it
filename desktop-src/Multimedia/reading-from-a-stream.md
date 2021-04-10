---
title: Lettura da un flusso
description: Lettura da un flusso
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- AVIStreamInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cc7ecd606a33503557e7c7209bff68015756523
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963080"
---
# <a name="reading-from-a-stream"></a>Lettura da un flusso

È possibile recuperare informazioni su un flusso aperto tramite la funzione [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Questa funzione riempie la struttura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) con informazioni quali il tipo di dati nel flusso, il metodo di compressione usato per la scrittura di dati di flusso, la dimensione del buffer suggerita, la velocità di riproduzione e una descrizione del flusso.

Alcuni membri della struttura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) sono presenti anche nella struttura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) . Le informazioni contenute nella struttura **AVIFILEINFO** sono valide per l'intero file. Le informazioni nella struttura **AVISTREAMINFO** sono specifiche del flusso a cui si accede e hanno la precedenza sulle informazioni nella struttura **AVIFILEINFO** .

Se a un flusso sono associate informazioni aggiuntive, è possibile recuperare queste informazioni tramite la funzione [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) . Questa funzione restituisce le informazioni in un buffer fornito dall'applicazione. Le informazioni sul flusso supplementare possono includere le impostazioni di configurazione per i metodi di compressione e decompressione usati in un flusso. È possibile ottenere le dimensioni del buffer richieste usando la macro [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize) .

È possibile recuperare le informazioni sulla formattazione di un flusso tramite la funzione [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) . Questa funzione restituisce una struttura specifica del flusso in un buffer fornito dall'applicazione. Per un flusso video, il buffer contiene informazioni di formattazione in una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Per un flusso audio, il buffer contiene informazioni di formattazione in una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) . Per altri tipi di flusso, il gestore del flusso restituisce informazioni specifiche per il flusso. È possibile determinare le dimensioni del buffer richieste usando **AVIStreamReadFormat** e specificando un indirizzo di buffer **null** o usando la macro [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize) .

È possibile recuperare il contenuto multimediale in un flusso usando la funzione [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) . Questa funzione copia i dati non elaborati dal flusso in un buffer fornito dall'applicazione. Per i flussi video, questa funzione recupera le immagini bitmap che compongono il contenuto del frame. Per i flussi audio, questa funzione recupera i campioni audio della forma d'onda che compongono il contenuto audio. È possibile determinare le dimensioni del buffer richieste usando **AVIStreamRead** e specificando un indirizzo di buffer **null** o usando la macro [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize) .

Alcuni gestori di flussi AVI presentano ritardi associati all'inizializzazione o al coordinamento di software e hardware. È possibile informare questi gestori per prepararsi per lo streaming di dati tramite la funzione [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) . Questa funzione consente al gestore del flusso di allocare e inizializzare le risorse necessarie. Per informare questi gestori quando il flusso è terminato, usare la funzione [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) . Questa funzione consente al gestore del flusso di deallocare le risorse allocate per **AVIStreamBeginStreaming**.

La funzione [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) non fornisce servizi di decompressione. Per informazioni su come comprimere e decomprimere flussi audio, vedere [Gestione compressione audio](audio-compression-manager.md). Per informazioni su come comprimere e decomprimere flussi video, vedere [Gestione compressione video](video-compression-manager.md). Per informazioni su come comprimere e decomprimere singoli frame in un flusso video, vedere [utilizzo di dati video compressi in un flusso](working-with-compressed-video-data-in-a-stream.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di flusso](stream-operations.md)
</dt> </dl>

 

 