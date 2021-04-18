---
description: Gestione delle modifiche al formato dal renderer video
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Gestione delle modifiche al formato dal renderer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d731ac4b9d6985cf5ad92f642b6d8262209fa91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303928"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Gestione delle modifiche al formato dal renderer video

In questa sezione viene descritto in che modo un filtro decodificatore o un filtro di trasformazione deve gestire le modifiche al formato dal renderer video.

**Filtro renderer video**

Quando il filtro [renderer video](video-renderer-filter.md) precedente si connette, richiede un formato RGB che corrisponda al formato di visualizzazione del monitor primario. In questo modo è possibile utilizzare GDI per il rendering se DirectDraw non è disponibile. Quando viene avviata la riproduzione, il renderer video può passare a un formato compatibile con DirectDraw. Per verfify se il filtro upstream può supportare il nuovo formato, il renderer video chiama [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output del filtro upstream. Se il filtro upstream accetta il nuovo formato, il metodo **QueryAccept** restituisce S \_ OK. Il renderer video passa i formati connettendo un tipo di supporto con il nuovo formato all'esempio multimediale successivo restituito dall'allocatore. Il filtro upstream deve verificare la presenza di modifiche al formato chiamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) su ogni esempio. Il renderer video può passare dal formato originale al nuovo formato e viceversa in qualsiasi momento durante il flusso. Non chiama **QueryAccept** dopo la modifica del primo formato. Una volta accettato il nuovo formato, il filtro upstream deve essere in grado di spostarsi avanti e indietro.

Il filtro upstream può rifiutare la modifica del formato restituendo S \_ false da **QueryAccept**. In tal caso, il renderer video continua a usare GDI con il formato originale.

**Filtro renderer di combinazione video**

Il filtro del renderer video mixing (VMR-7 e VMR-9) si connetterà con qualsiasi formato supportato dall'hardware grafico nel sistema. VMR-7 utilizza sempre DirectDraw per il rendering e alloca le superfici DirectDraw sottostanti quando il filtro upstream si connette. VMR-9 USA sempre Direct3D per il rendering e alloca le superfici Direct3D sottostanti quando il filtro upstream si connette.

L'hardware grafico potrebbe richiedere uno stride della superficie superiore rispetto alla larghezza dell'immagine. In tal caso, VMR richiede un nuovo formato chiamando **QueryAccept**. Segnala lo stride della superficie nel membro **biWidth** di [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel formato video. Se il filtro upstream non restituisce \_ OK da **QUERYACCEPT**, VMR rifiuta il formato e tenta di connettersi usando il formato successivo annunciato dal filtro upstream. VMR connette il tipo di supporto con il nuovo formato al primo campione multimediale. Dopo il primo esempio, il formato rimane costante; VMR non comporterà il cambio di formato durante l'esecuzione del grafo.

**Rendering video migliorato (EVR)**

EVR usa sempre Direct3D per il rendering. Se è necessario uno stride di superficie più grande, EVR usa lo stesso meccanismo **QueryAccept** di VMR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[QueryAccept (upstream)](queryaccept--upstream.md)
</dt> </dl>

 

 



