---
description: Tipo di formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo di formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a820ea6a53c457d2d000be8b4c0e8966213c1aeeb2b5f55a780c4801a4182907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071925"
---
# <a name="videoinfo2-format-type"></a>Tipo di formato VideoInfo2

Il tipo di supporto preferito di un segnaposto di anteprima potrebbe essere un tipo con [**formato VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Questa struttura di formato supporta funzionalità speciali, ad esempio le proporzioni di video e immagini interlacciate.

VMR-7 e VMR-9 supportano entrambi [**direttamente VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Quando si connette la macchina virtuale al decodificatore, negozierà il formato migliore. Il filtro del renderer video precedente, tuttavia, non supporta **VIDEOINFOHEADER2.** Per usare **i tipi di formato VIDEOINFOHEADER2** con il filtro Renderer video, è necessario inserire il filtro Overlay [Mixer](overlay-mixer-filter.md) nel grafico.

1.  Enumerare i tipi di supporti preferiti sul pin di output del filtro decodificatore usando il [**metodo IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)
2.  Controllare il primo tipo di supporto nella sequenza di enumerazione.
3.  Se il tipo di formato è **FORMAT \_ VideoInfo2,** connettere il segnaposto di output al segnaposto overlay Mixer. Connettere quindi il Mixer overlay al renderer video. Vedere [Pin della porta](video-port-pins.md)video.

Se queste funzionalità non sono importanti, non è necessario usare la funzionalità Di sovrimpressione Mixer. Connessione il decodificatore direttamente al renderer video e si connetterà con un [**formato VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati sull'acquisizione](advanced-capture-topics.md)
</dt> <dt>

[Uso della sovrimpressione Mixer'acquisizione video](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



