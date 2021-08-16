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
ms.openlocfilehash: 2f815e0bb1fc7e8e1cba277f68b7950af2b20395092b69b2c07ebb7ac51367da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843790"
---
# <a name="wmt_videoimage_transition_inset"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ INSET

La transizione inset rivela la nuova immagine in un rettangolo proveniente da un angolo del frame.

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
<td>Larghezza</td>
<td><strong>fEffectPara0</strong></td>
<td>Larghezza dell'oggetto inset in pixel.</td>
</tr>
<tr class="even">
<td>Altezza</td>
<td><strong>fEffectPara1</strong></td>
<td>Altezza dell'oggetto inset in pixel.</td>
</tr>
<tr class="odd">
<td>Direzione</td>
<td><strong>fEffectPara2</strong></td>
<td>Angolo da cui ha origine l'oggetto inset. Impostare su uno dei valori seguenti:<br/>
<ul>
<li>0 - In basso a sinistra</li>
<li>1 - In basso a destra</li>
<li>2 - In alto a sinistra</li>
<li>3 - In alto a destra</li>
</ul></td>
</tr>
<tr class="even">
<td>Composizione</td>
<td><strong>fEffectPara3</strong></td>
<td>Impostare su uno dei valori seguenti:
<ul>
<li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li>
<li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Transizioni di immagini video**](video-image-transitions.md)
</dt> </dl>

 

 





