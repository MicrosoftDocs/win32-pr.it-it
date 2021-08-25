---
description: Gestione delle modifiche al formato dal renderer video
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Gestione delle modifiche al formato dal renderer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1dd0ec2f87a8604d3b03aa6c2f334161d218f4d7fb45c76aad1015f071d947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905301"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Gestione delle modifiche al formato dal renderer video

Questa sezione descrive in che modo un filtro decodificatore o un filtro di trasformazione deve gestire le modifiche di formato dal renderer video.

**Filtro renderer video**

Quando si connette [il filtro del renderer](video-renderer-filter.md) video precedente, è necessario un formato RGB corrispondente al formato di visualizzazione del monitor primario. In questo modo può usare GDI per il rendering se DirectDraw non è disponibile. All'avvio della riproduzione, il renderer video può passare a un formato compatibile con DirectDraw. Per verificare se il filtro upstream può supportare il nuovo formato, il renderer video chiama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output del filtro upstream. Se il filtro upstream accetta il nuovo formato, il **metodo QueryAccept** restituisce S \_ OK. Il renderer video cambia i formati collegando un tipo di supporto con il nuovo formato all'esempio multimediale successivo restituito dall'allocatore. Il filtro upstream deve verificare la presenza di modifiche al formato chiamando [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) in ogni esempio. Il renderer video può passare dal formato originale al nuovo formato in qualsiasi momento durante lo streaming. Non chiama **QueryAccept dopo la** prima modifica del formato. Dopo che il filtro upstream ha accettato il nuovo formato, deve essere in grado di spostarsi avanti e indietro.

Il filtro upstream può rifiutare la modifica del formato restituisce S \_ FALSE da **QueryAccept.** In tal caso, il renderer video continua a usare GDI con il formato originale.

**Filtro del renderer di combinazione video**

Il filtro del renderer di combinazione video (VMR-7 e VMR-9) si connetterà a qualsiasi formato supportato dall'hardware grafico del sistema. VMR-7 usa sempre DirectDraw per il rendering e alloca le superfici DirectDraw sottostanti quando il filtro upstream si connette. VMR-9 usa sempre Direct3D per il rendering e alloca le superfici Direct3D sottostanti quando il filtro upstream si connette.

L'hardware grafico può richiedere uno stride di superficie maggiore rispetto alla larghezza dell'immagine. In tal caso, la macchina virtuale richiede un nuovo formato chiamando **QueryAccept**. Segnala lo stride della superficie nel **membro biWidth** di [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel formato video. Se il filtro upstream non restituisce S OK da \_ **QueryAccept,** il vmr rifiuta il formato e tenta di connettersi usando il formato successivo annunciato dal filtro upstream. La macchina virtuale collega il tipo di supporto con il nuovo formato al primo campione di supporti. Dopo il primo esempio, il formato rimane costante. La macchina virtuale non cambia formato mentre il grafo è in esecuzione.

**Rendering video avanzato (EVR)**

EVR usa sempre Direct3D per il rendering. Se è necessario uno stride di superficie più grande, L'EVR usa lo stesso **meccanismo QueryAccept** del VMR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[QueryAccept (Upstream)](queryaccept--upstream.md)
</dt> </dl>

 

 



