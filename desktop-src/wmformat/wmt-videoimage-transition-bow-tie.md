---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl. h)
description: La transizione del Papillon Mostra la nuova immagine in un set di triangoli sui lati opposti del frame.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324449"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>WMT \_ VIDEOIMAGE \_ Transition \_ Papillon \_

La transizione del Papillon Mostra la nuova immagine in un set di triangoli sui lati opposti del frame.

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
<td>Larghezza di ogni lato triangolare del Papillon.</td>
</tr>
<tr class="even">
<td>Altezza</td>
<td><strong>fEffectPara1</strong></td>
<td>Altezza di ogni lato triangolare del Papillon.</td>
</tr>
<tr class="odd">
<td>Direzione</td>
<td><strong>fEffectPara2</strong></td>
<td>Impostare su uno dei valori seguenti:
<ul>
<li>0: specifica l'effetto di curvatura orizzontale, in cui i triangoli vengono immessi dai lati destro e sinistro del frame.</li>
<li>1-specifica l'effetto di curvatura verticale, in cui i triangoli vengono immessi dalla parte superiore e inferiore del frame.</li>
</ul></td>
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

 

 





