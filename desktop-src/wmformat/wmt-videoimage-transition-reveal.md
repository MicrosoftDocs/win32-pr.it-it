---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl.h)
description: La transizione reveal rivela la nuova immagine lungo una linea retta che ha origine da un lato del frame.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140271d365d9673c948c4ff6f540e9bef33e8006
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469318"
---
# <a name="wmt_videoimage_transition_reveal"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ REVEAL

La transizione reveal rivela la nuova immagine lungo una linea retta che ha origine da un lato del frame.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Distanza | <strong>fEffectPara0</strong> | Quantità della nuova immagine rivelata, in pixel. Questo valore è relativo al lato di origine del frame. | 
| Direzione | <strong>fEffectPara1</strong> | Direzione dell'oggetto revealing. Impostare su uno dei valori seguenti:<br /><ul><li>0 - Reveal a destra; hanno origine dal lato sinistro del frame.</li><li>1 - Reveal a sinistra; hanno origine dal lato destro del frame.</li><li>2 - Rivelare verso l'alto; hanno origine dalla parte inferiore del frame.</li><li>3 - Rivelare verso il basso; hanno origine dalla parte superiore del frame.</li></ul> | 
| Composizione | <strong>fEffectPara2</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





