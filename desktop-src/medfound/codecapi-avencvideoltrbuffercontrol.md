---
description: Specifica il numero massimo di frame di riferimento a lungo termine (LTR) controllati dall'applicazione.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Proprietà CODECAPI_AVEncVideoLTRBufferControl (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524633"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>Proprietà AVEncVideoLTRBufferControl di codecapi \_

Specifica il numero massimo di frame di riferimento a lungo termine (LTR) controllati dall'applicazione.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoLTRBufferControl**

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
<td>Numero di fotogrammi LTR controllati dall'applicazione.<br/> <strong>Codificatori H. 264/AVC:</strong><br/> Supponendo che il valore sia N e N sia un valore diverso da zero, in ogni frame IDR il codificatore deve contrassegnare automaticamente i frame che seguono il frame IDR (e includere il frame IDR) come frame LTR purché siano applicabili tutti i 3 degli elementi seguenti:
<ul>
<li>Il frame non è già impostato per essere contrassegnato come frame di riferimento a lungo termine.</li>
<li>Il frame è un frame del livello di base. Ad esempio, l'elemento Syntax <strong>temporal_id</strong> uguale a 0.</li>
<li>Il numero di frame attualmente contrassegnati come LTR è inferiore a N.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Il secondo bit di campo</strong></dt> <dt>[16.. 31]</dt> </dl></td>
<td>Modalità di attendibilità del controllo LTR.<br/> <strong>Codificatori H. 264/AVC:</strong><br/> 1 (trust fino a) significa che il codificatore può usare un frame LTR, a meno che l'app non lo invalidi in modo esplicito tramite il controllo <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> . <br/> Altri valori non sono validi e sono riservati per un uso futuro.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Si tratta di un'API statica.

Il valore predefinito deve essere 0

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

 

 




