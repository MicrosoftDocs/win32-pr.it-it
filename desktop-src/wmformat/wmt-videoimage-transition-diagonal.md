---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl.h)
description: La transizione diagonale rivela la nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.
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
ms.openlocfilehash: 6b1a356d7325dd01de2ad055750a062d5591fd4aa983fdb21e39e9543a3d26e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658131"
---
# <a name="wmt_videoimage_transition_diagonal"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAGONAL

La transizione diagonale rivela la nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.

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
<td>Larghezza della sezione diagonale in pixel.</td>
</tr>
<tr class="even">
<td>Altezza</td>
<td><strong>fEffectPara1</strong></td>
<td>Altezza della sezione diagonale in pixel.</td>
</tr>
<tr class="odd">
<td>Direzione</td>
<td><strong>fEffectPara2</strong></td>
<td>Determina l'angolo da cui ha origine la transizione. Impostare su uno dei valori seguenti:<br/>
<ul>
<li>0 - In alto a destra</li>
<li>1 - In alto a sinistra</li>
<li>2 - In basso a destra</li>
<li>3 - In basso a sinistra</li>
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

 

 





