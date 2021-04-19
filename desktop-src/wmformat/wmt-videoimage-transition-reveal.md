---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: La transizione Reveal Mostra la nuova immagine lungo una linea retta originata da un lato del frame.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL formato Windows Media
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
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331688"
---
# <a name="wmt_videoimage_transition_reveal"></a>WMT \_ VIDEOIMAGE \_ transizione \_

La transizione Reveal Mostra la nuova immagine lungo una linea retta originata da un lato del frame.

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
<td>Distanza</td>
<td><strong>fEffectPara0</strong></td>
<td>Quantità della nuova immagine rivelata, in pixel. Questo valore è relativo al lato di origine del frame.</td>
</tr>
<tr class="even">
<td>Direzione</td>
<td><strong>fEffectPara1</strong></td>
<td>Direzione della rivelazione. Impostare su uno dei valori seguenti:<br/>
<ul>
<li>0: rivela a destra; originano dal lato sinistro del frame.</li>
<li>1: rivela a sinistra; ha origine dal lato destro del frame.</li>
<li>2-rivela verso l'alto; originano dalla parte inferiore del frame.</li>
<li>3-rivelare verso il basso; originano dalla parte superiore del frame.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composizione</td>
<td><strong>fEffectPara2</strong></td>
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

 

 





