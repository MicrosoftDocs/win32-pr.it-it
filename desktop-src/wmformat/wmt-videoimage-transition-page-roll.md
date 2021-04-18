---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: La transizione del rullo di pagina trasforma l'immagine precedente con un effetto di capovolgimento della pagina, mostrando la nuova immagine sotto.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325527"
---
# <a name="wmt_videoimage_transition_page_roll"></a>\_ \_ \_ Roll pagina transizione VIDEOIMAGE \_ di WMT

La transizione del rullo di pagina trasforma l'immagine precedente con un effetto di capovolgimento della pagina, mostrando la nuova immagine sotto.

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
<td>Radius</td>
<td><strong>fEffectPara0</strong></td>
<td>Raggio del rullo nell'effetto del rullo della pagina.</td>
</tr>
<tr class="even">
<td>Distanza</td>
<td><strong>fEffectPara1</strong></td>
<td>Quantità della nuova immagine rivelata dall'effetto di roll page, in pixel.</td>
</tr>
<tr class="odd">
<td>Direzione</td>
<td><strong>fEffectPara2</strong></td>
<td>Angolo o lato del fotogramma video da cui ha origine il rullo di pagina. Impostare su uno dei valori seguenti:<br/>
<ul>
<li>0-lato sinistro</li>
<li>1-lato destro</li>
<li>2-inferiore</li>
<li>3-inizio</li>
<li>4-angolo inferiore sinistro</li>
<li>5-angolo inferiore destro</li>
<li>6-angolo superiore sinistro</li>
<li>7-angolo superiore destro</li>
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

 

 





