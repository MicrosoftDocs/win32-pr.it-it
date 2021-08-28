---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl.h)
description: La transizione di roll-page trasforma l'immagine precedente con un effetto di capovolgimento della pagina, rivelando la nuova immagine sottostante.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfa69988f5b5414eac3e27b3371bca0e0a28810
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474977"
---
# <a name="wmt_videoimage_transition_page_roll"></a>ROLL DELLA PAGINA DI \_ TRANSIZIONE \_ DI WMT VIDEOIMAGE \_ \_

La transizione di roll-page trasforma l'immagine precedente con un effetto di capovolgimento della pagina, rivelando la nuova immagine sottostante.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Radius | <strong>fEffectPara0</strong> | Raggio del rullo nell'effetto di roll-roll della pagina. | 
| Distanza | <strong>fEffectPara1</strong> | Quantità in pixel della nuova immagine rivelata dall'effetto di roll-roll della pagina. | 
| Direzione | <strong>fEffectPara2</strong> | Angolo o lato del frame video, da cui ha origine il roll-roll della pagina. Impostare su uno dei valori seguenti:<br /><ul><li>0 - Lato sinistro</li><li>1 - Lato destro</li><li>2 - In basso</li><li>3 - In alto</li><li>4 - Angolo inferiore sinistro</li><li>5 - Angolo inferiore destro</li><li>6 - Angolo superiore sinistro</li><li>7 - Angolo superiore destro</li></ul> | 
| Composizione | <strong>fEffectPara3</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





