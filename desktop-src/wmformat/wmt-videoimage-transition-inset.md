---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl. h)
description: La transizione Insert Mostra la nuova immagine in un rettangolo originato da un angolo del frame.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET formato Windows Media
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
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326871"
---
# <a name="wmt_videoimage_transition_inset"></a>\_Insert WMT VIDEOIMAGE \_ Transition \_

La transizione Insert Mostra la nuova immagine in un rettangolo originato da un angolo del frame.

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
<td>Larghezza</td>
<td><strong>fEffectPara0</strong></td>
<td>Larghezza dell'inserto in pixel.</td>
</tr>
<tr class="even">
<td>Altezza</td>
<td><strong>fEffectPara1</strong></td>
<td>Altezza dell'inserto in pixel.</td>
</tr>
<tr class="odd">
<td>Direzione</td>
<td><strong>fEffectPara2</strong></td>
<td>Angolo da cui ha origine l'inserimento. Impostare su uno dei valori seguenti:<br/>
<ul>
<li>0-in basso a sinistra</li>
<li>1-in basso a destra</li>
<li>2-in alto a sinistra</li>
<li>3-in alto a destra</li>
</ul></td>
</tr>
<tr class="even">
<td>Composizione</td>
<td><strong>fEffectPara3</strong></td>
<td>Impostare su uno dei valori seguenti:
<ul>
<li>0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</li>
<li>1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</li>
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

 

 





