---
description: Generato da un flusso multimediale all'avvio o all'arresto del flusso. Per informazioni sul thinning, vedere Informazioni sul controllo della frequenza.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 371c628498356f64918d42ffe6af94aef95af34005250ba3a4a891b6b76f6dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013561"
---
# <a name="mestreamthinmode-event"></a>EVENTO MEStreamThinMode

Generato da un flusso multimediale all'avvio o all'arresto del flusso. Per informazioni sul *thinning,* vedere [About Rate Control](about-rate-control.md).

Questo evento può essere inviato in risposta al [**metodo IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) o [**al metodo IMFQualityAdvise::SetDropMode.**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode)

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>VARTYPE</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VT_BOOL<br/></td>
<td>Indica se il thinning è stato avviato o arrestato.<br/>
<ul>
<li>VARIANT_TRUE: gli esempi recapitati dopo questo evento vengono dilutti.</li>
<li>VARIANT_FALSE: gli esempi recapitati dopo questo evento non vengono dilutti.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




