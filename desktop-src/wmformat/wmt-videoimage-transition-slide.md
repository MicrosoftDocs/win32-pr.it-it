---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl.h)
description: La transizione di scorrimento rivela la nuova immagine scorrendo l'immagine precedente fuori dal frame.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9866706528cab038042adc8d098743ce6588c805
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476337"
---
# <a name="wmt_videoimage_transition_slide"></a>DIAPOSITIVA DI TRANSIZIONE VIDEOIMAGE WMT \_ \_ \_

La transizione di scorrimento rivela la nuova immagine scorrendo l'immagine precedente fuori dal frame.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Distanza | <strong>fEffectPara0</strong> | Distanza, in pixel, in cui l'immagine precedente esce dal frame. | 
| Direzione | <strong>fEffectPara1</strong> | Direzione in cui scorre l'immagine precedente. Impostare su uno dei valori seguenti:<br /><ul><li>0 - Scorrere verso destra.</li><li>1 - Scorrere verso sinistra.</li><li>2 - Scorrere verso l'alto.</li><li>3 - Scorrere verso il basso.</li></ul> | 
| Composizione | <strong>fEffectPara2</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





