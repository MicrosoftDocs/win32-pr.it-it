---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl.h)
description: La transizione di capovolgimento ruota l'immagine precedente su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come la parte posteriore dell'immagine precedente.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a3bfe94e001c6a65256facd5484a015d00f245
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475757"
---
# <a name="wmt_videoimage_transition_flip"></a>CAPOVOLGIMENTO \_ TRANSIZIONE \_ WMT VIDEOIMAGE \_

La transizione di capovolgimento ruota l'immagine precedente su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come la parte posteriore dell'immagine precedente.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Angle | <strong>fEffectPara0</strong> | Angolo della rotazione, da 0,0 a 180,0 gradi. | 
| Composizione | <strong>fEffectPara1</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li></ul> | 




 

## <a name="remarks"></a>Commenti

È possibile visualizzare l'effetto di questa transizione come se entrambe le immagini fossero fotografie fisiche incollate tra loro. La transizione ha lo stesso effetto di tenere due fotografie di questo tipo al centro del bordo inferiore e ruotarle di 180 gradi.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





