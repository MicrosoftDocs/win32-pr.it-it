---
description: Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti utilizzati dalla struttura di proprietà del pacchetto \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID di PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885573"
---
# <a name="packetproperty-guids"></a>GUID di PacketProperty

Nella tabella seguente sono elencati i GUID delle proprietà dei pacchetti utilizzati dalla struttura di [**\_ proprietà del pacchetto**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .



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
<td>Angolo tra l'asse della penna e la superficie della tavoletta. Il valore è 0 quando la penna è parallela alla superficie e 90 quando la penna è perpendicolare alla superficie. I valori sono negativi quando la penna è invertita.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Rotazione in senso orario del cursore intorno all'asse z tramite un intervallo circolare completo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>GUID utilizzato per recuperare il numero di casella per un riconoscimento dell'input penna alternativo quando il riconoscimento funziona in modalità Box.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Pressione su un pulsante sensibile alla pressione.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna perpendicolare alla superficie del tablet. Maggiore è la pressione applicata alla punta della penna, più l'input penna disegnato.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Contiene uno o più dei seguenti valori di flag:<br/>
<ul>
<li>Il cursore sta toccando la superficie di disegno (valore = 1).</li>
<li>Il cursore viene invertito. Ad esempio, l'estremità della gomma della penna è rivolta verso la superficie (valore = 2).</li>
<li>Non usato (valore = 4).</li>
<li>Il pulsante a barilotto è premuto (valore = 8).</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>Identificatore del contatto del dispositivo per un pacchetto.<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>Identifica il pacchetto. Si tratta dello stesso valore usato per recuperare il pacchetto dalla coda di pacchetti.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>GUID per l'oggetto PacketProperty che rappresenta la pressione della punta della penna lungo il piano della superficie della tavoletta.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Ora di generazione del pacchetto.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Rotazione in senso orario del cursore intorno al proprio asse.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>Coordinata x nello spazio delle coordinate della tavoletta. Per impostazione predefinita, ogni pacchetto contiene questa proprietà. L'origine (0, 0) del tablet è l'angolo superiore sinistro.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>Per un cursore penna, l'orientamento x-Tilt è l'angolo tra il piano y, z e il piano dell'asse y e della penna. Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positivo quando la penna è a destra di perpendicolare.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>Coordinata y nello spazio delle coordinate della tavoletta. Per impostazione predefinita, ogni pacchetto contiene questa proprietà. L'origine (0, 0) del tablet è l'angolo superiore sinistro.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Per un cursore penna, l'orientamento y è l'angolo tra il piano x, z e il piano dell'asse x e della penna. Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna è verso l'alto o fuori dall'utente.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>Coordinata z o distanza della punta della penna dalla superficie del tablet. Il tipo di enumerazione <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> determina l'unità di misura per questa proprietà. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Il campo TangentPressure rappresenta la pressione lungo il piano della superficie del Tablet; il campo NormalPressure rappresenta la pressione perpendicolare al piano della superficie della tavoletta.

 

 

 




