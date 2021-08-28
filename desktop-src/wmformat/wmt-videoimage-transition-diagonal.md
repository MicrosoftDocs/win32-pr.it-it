---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl.h)
description: La transizione diagonale visualizza la nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea028777580f7414a834a0aa3e73e18db607eccd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471987"
---
# <a name="wmt_videoimage_transition_diagonal"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAGONAL

La transizione diagonale visualizza la nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.




| Parametro | Membro della struttura | Descrizione | 
|-----------|------------------|-------------|
| Larghezza | <strong>fEffectPara0</strong> | Larghezza della sezione diagonale in pixel. | 
| Altezza | <strong>fEffectPara1</strong> | Altezza della sezione diagonale in pixel. | 
| Direzione | <strong>fEffectPara2</strong> | Determina l'angolo da cui ha origine la transizione. Impostare su uno dei valori seguenti:<br /><ul><li>0 - In alto a destra</li><li>1 - In alto a sinistra</li><li>2 - In basso a destra</li><li>3 - In basso a sinistra</li></ul> | 
| Composizione | <strong>fEffectPara3</strong> | Impostare su uno dei valori seguenti:<ul><li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li><li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano.</li></ul> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





