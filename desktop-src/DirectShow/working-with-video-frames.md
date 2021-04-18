---
description: Utilizzo di fotogrammi video
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Utilizzo di fotogrammi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313392"
---
# <a name="working-with-video-frames"></a>Utilizzo di fotogrammi video

Il video non compresso è una sequenza di bitmap riprodotte in rapida successione, in genere con una frequenza di circa 30 fotogrammi al secondo. Poiché la maggior parte dei video entra in un grafico con filtro DirectShow in un formato compresso, il flusso video passa in genere a un decodificatore per la decompressione. Molti decodificatori restituiscono dati in formato YUV e lasciano la conversione finale a RGB per l'hardware video appena prima del rendering. Se un decodificatore usa l'accelerazione video DirectX, l'hardware video esegue operazioni aggiuntive per decodificare l'immagine. Pertanto, la decompressione finale delle bitmap potrebbe non essere eseguita fino a quando i dati non raggiungono l'hardware del video.

Tuttavia, per eseguire molti tipi di analisi video, elaborazione o modifica, è spesso necessario lavorare su bitmap non compresse in un tipo di formato RGB o YUV prima che vengano sottoposti a rendering o scritti nel file. Questa operazione viene in genere eseguita in un filtro di trasformazione basato sulla classe di base [**CTransformFilter**](ctransformfilter.md) , in particolare nel metodo **Transform** . Questo metodo riceve un puntatore a un oggetto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) che incapsula i dati video. Il metodo **IMediaSample:: Getpointer** restituisce un puntatore al primo byte dei dati non elaborati. Per i frame non compressi, i dati sono costituiti da pixel a cui è possibile accedere o che possono essere modificati direttamente dal filtro. Nelle sezioni seguenti vengono fornite informazioni complementari che consentono di utilizzare in modo efficace i dati DIB.

> [!Note]  
> È anche possibile modificare i bit usando le funzioni GDI, GDI+, DirectDraw o Direct3D, ma queste tecniche esulano dall'ambito di questo articolo.

 

Questa sezione contiene i seguenti argomenti:

-   [Top-down rispetto a Bottom-Up](top-down-vs--bottom-up-dibs.md)
-   [Uso di RGB a 16 bit](working-with-16-bit-rgb.md)

 

 



