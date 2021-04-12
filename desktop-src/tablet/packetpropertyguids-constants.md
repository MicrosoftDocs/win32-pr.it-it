---
description: Definisce i valori che specificano le proprietà del pacchetto.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Costanti PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233863"
---
# <a name="packetpropertyguids-constants"></a>Costanti PacketPropertyGuids

Definisce i valori che specificano le proprietà del pacchetto. Il tablet PCAPI usa identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in COM sono stringhe costanti.

In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut. h, che si trova nella <systemdrive> \\ Directory: programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include directory se è stato installato l'SDK nel percorso predefinito. In C++, queste costanti sono WCHAR, non BSTR. Convertirli in BSTR prima di usarli. Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).

La tabella seguente elenca i campi GUID (Globally Unique Identifier) delle proprietà dei pacchetti disponibili. Usare questi GUID per specificare le proprietà contenute nel pacchetto quando si crea il contesto della tavoletta. Per determinare l'intervallo e la risoluzione di una proprietà, chiamare il metodo [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) . Le costanti della tabella seguente che iniziano con "STR \_ " sono rappresentazioni di stringa delle costanti binarie corrispondenti mostrate nella stessa cella della tabella.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <dt><strong>STR_GUID_X o GUID_PACKETPROPERTY_GUID_X</strong></dt> </dl></td>
<td style="text-align: left;">Coordinata x nello spazio delle coordinate della tavoletta. Per impostazione predefinita, ogni pacchetto contiene questa proprietà. L'origine (0, 0) del tablet è l'angolo superiore sinistro.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </dl></td>
<td style="text-align: left;">Coordinata y nello spazio delle coordinate della tavoletta. Per impostazione predefinita, ogni pacchetto contiene questa proprietà. L'origine (0, 0) del tablet è l'angolo superiore sinistro.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </dl></td>
<td style="text-align: left;">Coordinata y nello spazio delle coordinate della tavoletta. Per impostazione predefinita, ogni pacchetto contiene questa proprietà. L'origine (0, 0) del tablet è l'angolo superiore sinistro.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <dt><strong>STR_GUID_Z o GUID_PACKETPROPERTY_GUID_Z</strong></dt> </dl></td>
<td style="text-align: left;">Coordinata z o distanza della punta della penna dalla superficie del tablet. Il tipo di enumerazione <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> determina l'unità di misura per questa proprietà.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <dt><strong>STR_GUID_PAKETSTATUS o GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </dl></td>
<td style="text-align: left;">Contiene uno o più dei seguenti valori di flag:<br/>
<ul>
<li>Il cursore sta toccando la superficie di disegno (valore = 1).</li>
<li>Il cursore viene invertito. Ad esempio, l'estremità della gomma della penna è rivolta verso la superficie (valore = 2).</li>
<li>Non usato (valore = 4).</li>
<li>Il pulsante a barilotto è premuto (valore = 8).</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </dl></td>
<td style="text-align: left;">Ora di generazione del pacchetto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </dl></td>
<td style="text-align: left;">Ora di generazione del pacchetto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <dt><strong>STR_GUID_SERIALNUMBER o GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Proprietà del pacchetto per l'identificazione del pacchetto.<br/> Si tratta dello stesso valore usato per recuperare il pacchetto dalla coda di pacchetti.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <dt><strong>STR_GUID_NORMALPRESSURE o GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Pressione della punta della penna perpendicolare alla superficie del tablet.<br/> Maggiore è la pressione sulla punta della penna, maggiore è l'input penna disegnato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <dt><strong>STR_GUID_TANGENTPRESSURE o GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Pressione della punta della penna lungo il piano della superficie della tavoletta.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <dt><strong>STR_GUID_BUTTONPRESSURE o GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Pressione su un pulsante sensibile alla pressione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <dt><strong>STR_GUID_XTILTORIENTATION o GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Angolo tra le y, il piano z e il piano dell'asse y e della penna.<br/> Si applica a un cursore della penna.<br/> Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positivo quando la penna è a destra di perpendicolare.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <dt><strong>STR_GUID_YTILTORIENTATION o GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Angolo tra le x, il piano z e il piano dell'asse x e della penna.<br/> Si applica a un cursore della penna.<br/> Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna è verso l'alto o verso il basso dall'utente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <dt><strong>STR_GUID_AZIMUTHORIENTATION o GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Rotazione in senso orario del cursore sull'asse z tramite un intervallo circolare completo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <dt><strong>STR_GUID_ALTITUDEORIENTATION o GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Angolo tra l'asse della penna e la superficie della tavoletta.<br/> Il valore è 0 quando la penna è parallela alla superficie e 90 quando la penna è perpendicolare alla superficie.<br/> I valori sono negativi quando la penna è invertita.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <dt><strong>STR_GUID_TWISTORIENTATION o GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Rotazione in senso orario del cursore sul relativo asse.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <dt><strong>STR_GUID_PITCHROTATION o GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Proprietà del pacchetto che indica se il suggerimento si trova al di sopra o al di sotto di una linea orizzontale perpendicolare alla superficie di scrittura.<br/>
<blockquote>
[!Note]<br />
Questa operazione richiede un digitalizzatore 3D.
</blockquote>
<br/> Il valore è positivo se il suggerimento si trova sopra la linea e negativo se è sotto la linea. Se, ad esempio, si tiene la penna davanti all'utente e si scrive su una parete immaginaria, il pitch è positivo se il suggerimento si trova sopra una riga che si estende dall'utente alla parete.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <dt><strong>STR_GUID_ROLLROTATION o GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Rotazione in senso orario della penna intorno al proprio asse. <br/>
<blockquote>
[!Note]<br />
Questa operazione richiede un digitalizzatore 3D.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Angolo della penna a sinistra o a destra intorno al centro dell'asse orizzontale quando la penna è orizzontale.<br/>
<blockquote>
[!Note]<br />
Questa operazione richiede un digitalizzatore 3D.
</blockquote>
<br/> Se si tiene la penna davanti all'utente e si scrive su una parete immaginaria, l'imbardata zero indica che la penna è perpendicolare alla parete. Il valore è negativo se il suggerimento si trova a sinistra della perpendicolare e positivo se il suggerimento è a destra di perpendicolare.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Angolo della penna a sinistra o a destra intorno al centro dell'asse orizzontale quando la penna è orizzontale.<br/>
<blockquote>
[!Note]<br />
Questa operazione richiede un digitalizzatore 3D.
</blockquote>
<br/> Se si tiene la penna davanti all'utente e si scrive su una parete immaginaria, l'imbardata zero indica che la penna è perpendicolare alla parete. Il valore è negativo se il suggerimento si trova a sinistra della perpendicolare e positivo se il suggerimento è a destra di perpendicolare.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <dt><strong>STR_GUID_WIDTH o GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </dl></td>
<td style="text-align: left;">Larghezza dell'area di contatto in un digitalizzatore Touch.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <dt><strong>STR_GUID_HEIGHT o GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Altezza dell'area di contatto in un digitalizzatore Touch.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE o GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </dl></td>
<td style="text-align: left;">Livello di confidenza del contatto del dito su un digitalizzatore Touch.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <dt><strong>STR_GUID_DEVICE_CONTACT_ID o GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore del contatto del dispositivo per un pacchetto.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

> [!Note]  
> Tutti i valori dei pacchetti provenienti dall'hardware del tablet sono numeri interi a 32 bit.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IsPacketPropertySupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**Metodo GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**Interfaccia IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




