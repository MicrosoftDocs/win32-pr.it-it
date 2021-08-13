---
description: Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti usati dalla struttura PACKET \_ PROPERTY.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb7db9f2d5e05000bdccd5a09b2b799f38aa1bb692fea110ea153a57912cfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449371"
---
# <a name="packetproperty-guids"></a>GUID PacketProperty

Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti usati dalla [**struttura PACKET \_ PROPERTY.**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GUID_ALTITUDE_ORIENTATION<br/></td>
<td>Angolo tra l'asse della penna e la superficie del tablet. Il valore è 0 quando la penna è parallela alla superficie e 90 quando la penna è perpendicolare alla superficie. I valori sono negativi quando la penna viene invertita.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Rotazione in senso orario del cursore intorno all'asse z attraverso un intervallo circolare completo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>GUID utilizzato per recuperare il numero di casella per un'alternativa di riconoscimento input penna quando il riconoscimento funziona in modalità box.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Pressione su un pulsante sensibile alla pressione.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna perpendicolare alla superficie del tablet. Maggiore è la pressione sulla punta della penna, maggiore sarà l'input penna disegnato.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Contiene uno o più dei valori flag seguenti:<br/>
<ul>
<li>Il cursore tocca la superficie di disegno (Valore = 1).</li>
<li>Il cursore viene invertito. Ad esempio, l'estremità della gomma della penna punta verso la superficie (Valore = 2).</li>
<li>Non usato (Valore = 4).</li>
<li>Viene premuto il pulsante a sospensione (Valore = 8).</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>Identificatore del contatto del dispositivo per un pacchetto.<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>Identifica il pacchetto. Si tratta dello stesso valore utilizzato per recuperare il pacchetto dalla coda di pacchetti.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna lungo il piano della superficie del tablet.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Ora in cui è stato generato il pacchetto.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Rotazione in senso orario del cursore intorno al proprio asse.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>Coordinata x nello spazio delle coordinate della compressa. Ogni pacchetto contiene questa proprietà per impostazione predefinita. L'origine (0,0) del tablet è l'angolo superiore sinistro.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>Per un cursore penna, l'orientamento dell'inclinazione x è l'angolo tra il piano y, z e il piano della penna e dell'asse y. Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna si trova a destra della perpendicolare.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>Coordinata y nello spazio delle coordinate della compressa. Ogni pacchetto contiene questa proprietà per impostazione predefinita. L'origine (0,0) del tablet è l'angolo superiore sinistro.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Per un cursore penna, l'orientamento dell'inclinazione y è l'angolo tra il piano x, z e il piano della penna e dell'asse x. Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna è verso l'alto o lontano dall'utente.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>Coordinata z o distanza della punta della penna dalla superficie del tablet. Il <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> di enumerazione determina l'unità di misura per questa proprietà. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Il campo TangentPressure rappresenta la pressione lungo il piano della superficie del tablet; Il campo NormalPressure rappresenta la pressione perpendicolare al piano della superficie della compressa.

 

 

 




