---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl.h)
description: La transizione arco rivela la nuova immagine in un set di triangoli sui lati opposti della cornice.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE windows Media Format
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
ms.openlocfilehash: 6f77cd2782bad6e4f83b5a4d1e719b0c21d704fefd2d4cccacfc0690a4fb0fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843952"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>ARCO DI TRANSIZIONE DI WMT \_ VIDEOIMAGE \_ \_ \_

La transizione arco rivela la nuova immagine in un set di triangoli sui lati opposti della cornice.

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
<td>Larghezza di ogni lato triangolare dell'arco.</td>
</tr>
<tr class="even">
<td>Altezza</td>
<td><strong>fEffectPara1</strong></td>
<td>Altezza di ogni lato triangolare dell'arco.</td>
</tr>
<tr class="odd">
<td>Direzione</td>
<td><strong>fEffectPara2</strong></td>
<td>Impostare su uno dei valori seguenti:
<ul>
<li>0 - Specifica l'effetto arco orizzontale, in cui i triangoli entrano dai lati destro e sinistro della cornice.</li>
<li>1 - Specifica l'effetto arco verticale, in cui i triangoli entrano dalla parte superiore e inferiore del frame.</li>
</ul></td>
</tr>
<tr class="even">
<td>Composizione</td>
<td><strong>fEffectPara3</strong></td>
<td>Impostare su uno dei valori seguenti:
<ul>
<li>0 : specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è in primo piano.</li>
<li>1 : specifica la composizione inversa, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è in primo piano.</li>
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

 

 





