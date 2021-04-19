---
description: MSYUV è un codec di convertitore dello spazio colore da YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Codec MSYUV Color Space Converter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332635"
---
# <a name="msyuv-color-space-converter-codec"></a>Codec MSYUV Color Space Converter

MSYUV è un codec di convertitore dello spazio colore da YUV a RGB. Consente la riproduzione dei dati di origine video in formati YUV nei client la cui scheda video non può essere usata per le conversioni da YUV a RGB nell'hardware. Il codec partecipa ai grafici dei filtri tramite il filtro del wrapper di [decompressione AVI](avi-decompressor-filter.md) .

Le videocamere digitali per la comunicazione con 1394 o le interfacce USB possono produrre dati di immagini in diversi formati YUV. Se l'hardware di visualizzazione non supporta la conversione da YUV a RGB a bordo o se non è possibile usare la funzionalità di conversione hardware per altri motivi, i dati dell'immagine YUV devono essere convertiti in formato RGB prima di essere inviati al renderer video.

A causa del requisito del [renderer video](video-renderer-filter.md)per un tipo di input RGB al momento della connessione, questo filtro può essere inserito in un grafico a Monte dal renderer video durante la creazione automatica del grafo. In particolare, se il generatore di grafici rileva un formato YUV nel tipo di supporto del PIN di output del filtro upstream, il generatore di grafi inserirà il decompressore AVI, che caricherà il codec MSYUV e lo configurerà inizialmente per eseguire la conversione in RGB. Dopo la prima transizione del grafico a uno stato di esecuzione o di sospensione, il filtro renderer video può rilevare se la scheda video è in grado di eseguire la conversione nell'hardware. In caso contrario, il decompressore AVI riceve una notifica e riconfigura MSYUV per il funzionamento in modalità pass-through, che fa in modo che il codec ignori la conversione e copi i dati dell'immagine YUV direttamente su una superficie sovrapposta DirectDraw nella memoria video.

Poiché i renderer di mixaggio video (VMR-7 e VMR-9) non utilizzano mai GDI, non richiedono un tipo RGB al momento della connessione e il convertitore dello spazio colori MSYUV non viene mai inserito prima del VMR in un grafico.

MSYUV converte i formati YUV compressi in RGB, come illustrato nell'elenco seguente:

-   Formati di input: UYVY, YUY2, YVYU
-   Formati di output: RGB 8, RGB 16, RGB 24, RGB 32

Il codec MSYUV Color Space Converter è un codec di Gestione compressione video (VCM). Viene usato in DirectShow tramite il filtro di [decompressione AVI](avi-decompressor-filter.md) . Per un convertitore di colori più generico, usare il [**convertitore di colori DSP**](../medfound/colorconverter.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 
