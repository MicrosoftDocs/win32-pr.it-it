---
description: Tipo di formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo di formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308952"
---
# <a name="videoinfo2-format-type"></a>Tipo di formato VideoInfo2

Il tipo di supporto preferito del PIN di anteprima potrebbe essere un tipo con formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Questa struttura di formato supporta funzionalità speciali, ad esempio proporzioni di video e immagini interlacciate.

VMR-7 e VMR-9 supportano entrambi [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) direttamente. Quando si connette VMR al decodificatore, il formato migliore sarà negoziato. Il filtro renderer video precedente, tuttavia, non supporta **VIDEOINFOHEADER2**. Per usare i tipi di formato **VIDEOINFOHEADER2** con il filtro renderer video, è necessario inserire il filtro [Overlay Mixer](overlay-mixer-filter.md) nel grafico.

1.  Enumerare i tipi di supporto preferiti sul pin di output del filtro decodificatore usando il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .
2.  Controllare il primo tipo di supporto nella sequenza di enumerazione.
3.  Se il formato del tipo **è \_ VideoInfo2**, connettere il pin di output al mixer della sovrimpressione. Connettere quindi il mixer della sovrimpressione al renderer video. (Vedere [pin della porta video](video-port-pins.md)).

Se non si è interessati a queste funzionalità, non è necessario usare il mixer overlay. Connettere il decodificatore direttamente al renderer video e si connetterà invece con un formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Uso del mixer overlay in acquisizione video](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



