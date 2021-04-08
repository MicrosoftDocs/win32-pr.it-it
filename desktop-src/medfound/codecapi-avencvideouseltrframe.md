---
description: Specifica che il frame corrente è codificato utilizzando uno o più frame LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: Proprietà CODECAPI_AVEncVideoUseLTRFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749354"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>Proprietà AVEncVideoUseLTRFrame di codecapi \_

Specifica che il frame corrente è codificato utilizzando uno o più frame LTR.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Valore proprietà

Il valore di questo controllo include due campi, in cui ogni campo dispone di 16 bit.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>Il primo campo</strong></dt> <dt>bits [0.. 15]</dt> </dl></td>
<td>Indica i frame LTR consentiti per la codifica del frame corrente. <br/> <strong>Codificatori H. 264/AVC:</strong><br/> Si tratta di una bitmap che indica i frame LTR che possono essere usati come riferimento per il frame. Il bit meno significativo corrisponde a LTR index 0, il secondo bit meno significativo corrisponde a LTR index 1 e così via.<br/> Il valore non deve essere 0.<br/> L'indice più alto specificato da questo valore non deve essere maggiore del numero massimo di frame LTR specificati nella proprietà <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> meno uno.<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Il secondo bit di campo</strong></dt> <dt>[16.. 31]</dt> </dl></td>
<td>Flag che indica se sono necessarie limitazioni aggiuntive per la codifica dei frame successivi. <br/> <strong>Codificatori H. 264/AVC:</strong><br/> 1 è l'unico valore valido per questo campo. Tutti gli altri valori non sono validi e sono riservati per un uso futuro.<br/> Quando il flag è 1, il codificatore deve codificare i frame successivi nell'ordine di codifica in base ai vincoli seguenti:<br/>
<ul>
<li>Non utilizzerà frame di riferimento a breve termine nell'ordine di codifica anteriore al frame corrente o alla codifica futura nell'ordine di codifica.</li>
<li>Non deve usare i frame LTR non descritti dal controllo CODECAPI_AVEncVideoUseLTRFrame più recente.</li>
<li>Può usare i frame LTR aggiornati dopo il frame corrente.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

**Codificatori H. 264/AVC:**

Questa proprietà non deve essere chiamata se una chiamata in sospeso per l'utilizzo di un frame LTR è stata eseguita utilizzando la \_ Proprietà codecapi AVEncVideoUseLTRFrame e il codificatore non ha ancora generato un frame in cui è stato utilizzato il valore ltr. In altre parole, il codificatore non deve accodare le richieste AVEncVideoUseLTRFrame di codecapis \_ .

Se viene inviata una richiesta AVEncVideoUseLTRFrame di codecapite \_ mentre un'altra \_ richiesta AVEncVideoUseLTRFrame di codecapites è ancora in sospeso, la richiesta precedente deve essere eliminata.

La chiamata a codecapit \_ AVEncVideoUseLTRFrame su un frame del livello non di base è valida e deve essere applicata al frame del livello non di base, senza ritardo in un frame del livello di base.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                   |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




