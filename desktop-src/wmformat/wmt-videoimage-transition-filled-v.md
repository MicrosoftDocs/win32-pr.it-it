---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl.h)
description: La transizione V piena rivela la nuova immagine in un triangolo proveniente da un lato del frame.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbf032700959dd21a560b879357de2800ac657b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466158"
---
# <a name="wmt_videoimage_transition_filled_v"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ FILLED \_ V

La transizione V piena rivela la nuova immagine in un triangolo proveniente da un lato del frame.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Larghezza | <strong>fEffectPara0</strong> | Larghezza della V riempita in pixel. | 
| Altezza | <strong>fEffectPara1</strong> | Altezza della V riempita in pixel. | 
| Direzione | <strong>fEffectPara2</strong> | Direzione da cui ha origine la V riempita. Impostare su uno dei valori seguenti:<br /><ul><li>0 : immette dal lato sinistro del frame.</li><li>1 - Immette dal lato destro del frame.</li><li>2 - Immette dalla parte inferiore del frame.</li><li>3 - Immette dalla parte superiore del frame.</li></ul> | 
| Composizione | <strong>fEffectPara3</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





