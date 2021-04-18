---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (Wmsdkidl. h)
description: La transizione del cerchio rivela la nuova immagine in un cerchio.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf3a8eff2ca5a5069fa01c4e61bc0735808fd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333737"
---
# <a name="wmt_videoimage_transition_circle"></a>\_cerchio di \_ transizione \_ VIDEOIMAGE di WMT

La transizione del cerchio rivela la nuova immagine in un cerchio.

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
<td>Centra X</td>
<td><strong>fEffectPara0</strong></td>
<td>Coordinata X, relativa al frame video, del centro del cerchio.</td>
</tr>
<tr class="even">
<td>Centra Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordinata Y, relativa al frame video, del centro del cerchio.</td>
</tr>
<tr class="odd">
<td>Radius</td>
<td><strong>fEffectPara2</strong></td>
<td>Raggio, in pixel, del cerchio.</td>
</tr>
<tr class="even">
<td>Composizione</td>
<td><strong>fEffectPara3</strong></td>
<td>Impostare su uno dei valori seguenti:
<ul>
<li>0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</li>
<li>1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





