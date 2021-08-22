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
ms.openlocfilehash: a194067fd8a5bb34569723245b68996163d0cd9a2eef332e6f42fceb8187eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590651"
---
# <a name="wmt_videoimage_transition_flip"></a>CAPOVOLGIMENTO \_ TRANSIZIONE \_ WMT VIDEOIMAGE \_

La transizione di capovolgimento ruota l'immagine precedente su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come la parte posteriore dell'immagine precedente.

## <a name="parameters"></a>Parametri

La tabella seguente descrive i parametri usati da questa transizione ed elenca i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.



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
<li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li>
<li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

È possibile visualizzare l'effetto di questa transizione come se entrambe le immagini fossero fotografie fisiche incollate tra loro. La transizione ha lo stesso effetto di tenere due fotografie di questo tipo al centro del bordo inferiore e ruotarle di 180 gradi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





