---
description: Configurazione dei pin di output di Demux
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Configurazione dei pin di output di Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56a24af3f49f26efe4ff6afad075a3cef61fcd1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124872"
---
# <a name="configuring-the-demux-output-pins"></a>Configurazione dei pin di output di Demux

Quando il demux MPEG-2 riceve un pacchetto di dati, deve determinare quale pin di output deve analizzare e recapitare i dati. In modalità flusso di programma, demux esegue il mapping degli ID di flusso ai pin di output. In modalità flusso di trasporto, esegue il mapping dei PID ai pin di output. Ad esempio, in modalità flusso di trasporto, se PID 0x31 è mappato al pin 0, ogni pacchetto TS con tale numero PID viene indirizzato al pin di output 0. Se il demux riceve un pacchetto il cui ID di flusso o PID non è mappato a un pin di output, il pacchetto viene semplicemente ignorato.

In modalità pull, demux crea automaticamente i pin di output per i flussi audio e video nel file e associa gli ID del flusso ai pin.

In modalità push, i pin di output devono essere configurati dall'applicazione o da un altro filtro. Per le origini della televisione digitale che usano l'architettura del driver di trasmissione (BDA), il filtro del provider di rete funziona con il filtro TIF per configurare demux. L'applicazione non deve eseguire alcuna operazione. In altri scenari, l'applicazione deve configurare i pin di output.

Il demux inizia senza pin di output. Per creare un pin di output, chiamare il metodo [**IMpeg2Demultiplexer:: CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) sul filtro. Questo metodo accetta un tipo di supporto e un nome di pin e restituisce un puntatore **Ipin** . Il tipo di supporto viene usato quando il pin si connette a un altro filtro, in genere un decodificatore, a un esempio viene assegnata la sezione [uso di Demux con flussi elementari](using-the-demux-with-elementary-streams.md). Il nome del PIN può essere qualsiasi elemento, ad eccezione del fatto che i nomi di pin duplicati non sono consentiti.

Quindi, assegnare uno o più ID di flusso o PID al nuovo PIN di output. Per i flussi di programma, eseguire una query sul pin per **IMPEG2StreamIdMap** e chiamare [**IMPEG2StreamIdMap:: MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). Per i flussi di trasporto, eseguire una query sul pin per **IMPEG2PIDMap** e chiamare [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Esistono diversi modi in cui demux può analizzare i pacchetti di Servizi terminal. Per ogni pin di output, il metodo di analisi è determinato dal parametro *MediaSampleContent* per il metodo **MapPID** .



| Valore                     | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_flusso elementare \_ multimediale | Il filtro recapita i payload di PES. In questa modalità, il filtro depacketizes i pacchetti PES, in modo che il filtro downstream riceva il flusso di byte ES, senza le intestazioni dei pacchetti PES. (Solo flussi audio e video).                                                                                                                                                     |
| MEDIA \_ MPEG2 \_ PSI         | Il filtro recapita le sezioni complete PSI, ad esempio le tabelle PAT, le tabelle PMT, le tabelle CAT e così via.                                                                                                                                                                                                                                                               |
| \_payload del trasporto multimediale \_ | Il filtro estrae i payload dai pacchetti di Servizi terminal e li recapita senza ulteriore analisi. Per i flussi elementari, questo significa che demux fornirà interi pacchetti PES, incluse le intestazioni dei pacchetti PES.                                                                                                                                                    |
| \_pacchetto di trasporto multimediale \_  | Il filtro recapita interi pacchetti di Servizi terminal. Il demux instrada i pacchetti di Servizi terminal in base ai relativi PID, ma in caso contrario non esamina né elabora i pacchetti. I pacchetti con errori non vengono filtrati. Il demux non esegue nuovamente il multiplexing dei pacchetti e il flusso di output risultante non è un flusso di trasporto MPEG-2 conforme. Questa modalità viene chiamata modalità *pass-through* . |



 

Per i flussi di programma, demux fornisce sempre payload PES.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



