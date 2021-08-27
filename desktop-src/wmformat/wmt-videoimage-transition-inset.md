---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl.h)
description: La transizione inset rivela la nuova immagine in un rettangolo proveniente da un angolo del frame.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47d53de99d3c6f6144755934989ca3958d28a23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476782"
---
# <a name="wmt_videoimage_transition_inset"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ INSET

La transizione inset rivela la nuova immagine in un rettangolo proveniente da un angolo del frame.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Larghezza | <strong>fEffectPara0</strong> | Larghezza dell'oggetto inset in pixel. | 
| Altezza | <strong>fEffectPara1</strong> | Altezza dell'oggetto inset in pixel. | 
| Direzione | <strong>fEffectPara2</strong> | Angolo da cui ha origine l'oggetto inset. Impostare su uno dei valori seguenti:<br /><ul><li>0 - In basso a sinistra</li><li>1 - In basso a destra</li><li>2 - In alto a sinistra</li><li>3 - In alto a destra</li></ul> | 
| Composizione | <strong>fEffectPara3</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





