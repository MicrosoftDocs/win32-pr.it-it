---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl. h)
description: La transizione Flip ruota l'immagine precedente su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come parte posteriore dell'immagine precedente.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP formato Windows Media
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
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333529"
---
# <a name="wmt_videoimage_transition_flip"></a>WMT \_ VIDEOIMAGE \_ transizione \_ Flip

La transizione Flip ruota l'immagine precedente su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come parte posteriore dell'immagine precedente.

## <a name="parameters"></a>Parametri

Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametro</th>
<th>Membro della struttura</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Angle</td>
<td><strong>fEffectPara0</strong></td>
<td>Angolo della rotazione, da 0,0 a 180,0 gradi.</td>
</tr>
<tr class="even">
<td>Composizione</td>
<td><strong>fEffectPara1</strong></td>
<td>Impostare su uno dei valori seguenti:
<ul>
<li>0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</li>
<li>1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

È possibile visualizzare l'effetto di questa transizione come se entrambe le immagini fossero fotografie fisiche associate insieme a back-to-back. La transizione ha lo stesso effetto di tenere due fotografie di questo tipo al centro del bordo inferiore e di ruotarle 180 gradi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





