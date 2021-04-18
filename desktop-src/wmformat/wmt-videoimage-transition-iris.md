---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl. h)
description: La transizione Iris rivela la nuova immagine lungo un asse x e un asse y. L'effetto visivo di questa transizione consiste nel fatto che la nuova immagine viene visualizzata in un incrocio incrociato che raggiunge tutti i lati del frame.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329897"
---
# <a name="wmt_videoimage_transition_iris"></a>\_ \_ Iris transizione VIDEOIMAGE \_ WMT

La transizione Iris rivela la nuova immagine lungo un asse x e un asse y. L'effetto visivo di questa transizione consiste nel fatto che la nuova immagine viene visualizzata in un incrocio incrociato che raggiunge tutti i lati del frame.

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
<td>Coordinata X, relativa al frame video, del centro dell'effetto Iris.</td>
</tr>
<tr class="even">
<td>Centra Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordinata Y, relativa al frame video, del centro dell'effetto Iris.</td>
</tr>
<tr class="odd">
<td>Larghezza</td>
<td><strong>fEffectPara2</strong></td>
<td>Larghezza della linea verticale che rivela la nuova immagine, in pixel.</td>
</tr>
<tr class="even">
<td>Altezza</td>
<td><strong>fEffectPara3</strong></td>
<td>Altezza della linea orizzontale che rivela la nuova immagine, in pixel.</td>
</tr>
<tr class="odd">
<td>Composizione</td>
<td><strong>fEffectPara4</strong></td>
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

 

 





