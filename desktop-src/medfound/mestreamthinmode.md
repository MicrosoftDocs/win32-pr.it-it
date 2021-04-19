---
description: Generato da un flusso multimediale quando inizia o smette di assottigliare il flusso. Per informazioni sull'assottigliamento, vedere informazioni sul controllo della frequenza.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309602"
---
# <a name="mestreamthinmode-event"></a>Evento MEStreamThinMode

Generato da un flusso multimediale quando inizia o smette di assottigliare il flusso. Per informazioni sull' *assottigliamento*, vedere [informazioni sul controllo della frequenza](about-rate-control.md).

Questo evento può essere inviato in risposta al metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue o al metodo [**IMFQualityAdvise:: SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



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
<td>Indica se l'assottigliamento è stato avviato o arrestato.<br/>
<ul>
<li>VARIANT_TRUE: gli esempi recapitati dopo questo evento sono diluiti.</li>
<li>VARIANT_FALSE: gli esempi recapitati dopo questo evento non vengono diluiti.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




