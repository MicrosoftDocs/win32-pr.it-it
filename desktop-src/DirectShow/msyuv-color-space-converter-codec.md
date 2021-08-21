---
description: MSYUV è un codec di convertitore di spazi colori da YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: MSYUV Color Space Converter Codec
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189ff787ee5b28311dd0357c245c7a6ca251d207f2448fc08a88fb856d7c2fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075741"
---
# <a name="msyuv-color-space-converter-codec"></a>MSYUV Color Space Converter Codec

MSYUV è un codec di convertitore di spazi colori da YUV a RGB. Consente la riproduzione di dati di origine video in formati YUV nei client la cui scheda video non può essere usata per le conversioni da YUV a RGB nell'hardware. Il codec partecipa ai grafici dei filtri tramite il filtro wrapper [AVI Decompressor.](avi-decompressor-filter.md)

Le videocamere per conferenze digitali con interfacce USB o 1394 possono produrre dati di immagine in vari formati YUV. Se l'hardware di visualizzazione non supporta la conversione da YUV a RGB su scheda o se la funzionalità di conversione hardware non può essere usata per altri motivi, i dati dell'immagine YUV devono essere convertiti nel formato RGB prima di essere inviati al renderer video.

A causa del requisito del [renderer video](video-renderer-filter.md)per un tipo di input RGB in fase di connessione, questo filtro potrebbe essere inserito in un grafo a monte dal renderer video durante la compilazione automatica del grafo. In particolare, se Graph Builder rileva un formato YUV nel tipo di supporto del pin di output del filtro upstream, Graph Builder inserirà il decompressore AVI, che carica il codec MSYUV e lo configura inizialmente per eseguire la conversione in RGB. Dopo la prima transizione del grafico a uno stato di esecuzione o sospensione, il filtro renderer video è in grado di rilevare se la scheda video è in grado di eseguire la conversione nell'hardware. Se possibile, il decompressore AVI viene avvisato e riconfigura MSYUV per il funzionamento in "modalità pass-through", che fa sì che il codec ignorare la conversione e copiare i dati dell'immagine YUV direttamente su una superficie di sovrapposizione DirectDraw nella memoria video.

Poiché i renderer di combinazione video (VMR-7 e VMR-9) non usano mai GDI, non richiedono un tipo RGB in fase di connessione e il convertitore di spazi colori MSYUV non viene mai inserito prima del VMR in un grafo.

MSYUV converte i formati YUV in formato RGB, come illustrato nell'elenco seguente:

-   Formati di input: UYVY, YUY2, YVYU
-   Formati di output: RGB 8, RGB 16, RGB 24, RGB 32

Il codec MSYUV Color Space Converter è un codec VCM (Video Compression Manager). Viene usato in DirectShow tramite il [filtro AVI Decompressor.](avi-decompressor-filter.md) Per un convertitore di colori più generico, usare [**il DSP di Color Converter.**](../medfound/colorconverter.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 
