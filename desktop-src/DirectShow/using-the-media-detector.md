---
description: Uso di Media Detector
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Uso di Media Detector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320469"
---
# <a name="using-the-media-detector"></a>Uso di Media Detector

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Il rilevatore multimediale è un oggetto helper in grado di recuperare informazioni su un file, ad esempio il numero di flussi, il tipo e la durata. Contiene inoltre metodi per il recupero di frame di poster da un flusso video. Espone l'interfaccia [**IMediaDet**](imediadet.md) .

Il rilevatore multimediale funziona in una delle due modalità. Quando si crea un'istanza del rilevamento multimediale, questa non è associata a un file di origine specifico. In questa modalità è possibile recuperare informazioni sul flusso da più file di origine. Tuttavia, una volta usato il rilevatore multimediale per ottenere un frame di poster, passa alla modalità di acquisizione *bitmap*. In modalità di cattura bitmap, il rilevatore multimediale è collegato a un flusso video specifico e i metodi di informazioni sul flusso non funzionano più. Inoltre, non è possibile riattivare il rilevatore multimediale fino alla modalità di avvio. Pertanto, ottenere tutte le informazioni sul flusso necessarie prima di recuperare i frame dei poster oppure creare nuove istanze del rilevamento multimediale per ogni flusso.

Per ottenere informazioni sul flusso, procedere come segue:

1.  Chiamare [**IMediaDet::p \_ nome file UT**](imediadet-put-filename.md) con il nome del file di origine.
2.  Chiamare [**IMediaDet:: Get \_ OutputStreams**](imediadet-get-outputstreams.md) per ottenere il numero di flussi nell'origine.
3.  Specificare un numero di flusso con [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md). Chiamare quindi uno o più dei metodi seguenti:
    -   [**IMediaDet:: Get \_ StreamType**](imediadet-get-streamtype.md): Recupera il tipo di supporto del flusso.
    -   [**IMediaDet:: Get \_ StreamLength**](imediadet-get-streamlength.md): Recupera la durata del flusso.
    -   [**IMediaDet:: Get \_ FrameRate**](imediadet-get-framerate.md): Recupera la frequenza dei fotogrammi di un flusso video.

Per ottenere un frame di poster, specificare il numero di flusso, come nel passaggio precedente. Chiamare quindi [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md), che copia un frame di poster in un buffer o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md), che salva un frame di poster in un file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di origini](working-with-sources.md)
</dt> </dl>

 

 



