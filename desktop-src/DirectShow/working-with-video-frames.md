---
description: Uso dei fotogrammi video
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Uso dei fotogrammi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86407f99138e0b38b67468668fc963bd1bcd7b65e875571643bc7727b4d0d339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870931"
---
# <a name="working-with-video-frames"></a>Uso dei fotogrammi video

Il video non compresso è una sequenza di bitmap riprodotte in rapida successione, in genere a una velocità di circa 30 fotogrammi al secondo. Poiché la maggior parte dei video DirectShow un grafico di filtro in un formato compresso, il flusso video passa in genere attraverso un decodificatore per la decompressione. Molti decodificatori generano dati in formato YUV e lasciano la conversione finale in RGB per l'hardware video appena prima del rendering. Se un decodificatore usa l'accelerazione video DirectX, l'hardware video esegue operazioni aggiuntive per decodificare l'immagine. Di conseguenza, la decompressione finale delle bitmap non può essere eseguita fino a quando i dati non raggiungono l'hardware video.

Tuttavia, per eseguire molti tipi di analisi video, elaborazione o modifica, è spesso necessario lavorare su bitmap non compresse in un tipo di formato RGB o YUV prima che ne venga eseguito il rendering o la scrittura su file. Questa operazione viene in genere eseguita all'interno di un filtro di trasformazione basato sulla classe di base [**CTransformFilter,**](ctransformfilter.md) in particolare nel **metodo Transform.** Questo metodo riceve un puntatore a un [**oggetto IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) che incapsula i dati video. Il **metodo IMediaSample::GetPointer** restituisce un puntatore al primo byte dei dati non elaborati. Per i frame non compressi, questi dati sono costituiti da pixel accessibili o modificati direttamente dal filtro. Le sezioni seguenti forniscono informazioni di base che consentono di usare in modo efficace i dati DIB in questo modo.

> [!Note]  
> È anche possibile modificare i bit usando le funzioni GDI, GDI+, DirectDraw o Direct3D, ma queste tecniche non sono nell'ambito di questo articolo.

 

Questa sezione contiene i seguenti argomenti:

-   [Dib dall'alto verso il basso Bottom-Up di archiviazione](top-down-vs--bottom-up-dibs.md)
-   [Uso di RGB a 16 bit](working-with-16-bit-rgb.md)

 

 



