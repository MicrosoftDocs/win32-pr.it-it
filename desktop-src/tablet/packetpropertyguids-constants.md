---
description: Definisce i valori che specificano le proprietà del pacchetto.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Costanti PacketPropertyGuids (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9eb946b170b1004deea7eb1f2faafeee5bc5dba
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884503"
---
# <a name="packetpropertyguids-constants"></a>Costanti PacketPropertyGuids

Definisce i valori che specificano le proprietà del pacchetto. Tablet PCAPI usa identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in COM sono stringhe costanti.

In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut.h, che si trova nella &lt; directory systemdrive &gt; : Programmi \\ Microsoft \\ SDKs \\ Windows \\ v6.0 \\ Include se l'SDK è stato installato nel percorso predefinito. In C++ queste costanti sono WCHAR, non BSTR. Convertirli in BSTR prima dell'uso. Per altre informazioni sul tipo di dati BSTR, vedere [Uso della libreria COM.](using-the-com-library.md)

Nella tabella seguente sono elencati i campi dell'identificatore univoco globale (GUID) della proprietà del pacchetto disponibili. Usare questi GUID per specificare le proprietà contenute nel pacchetto quando si crea il contesto della tablet. Per determinare l'intervallo e la risoluzione di una proprietà, chiamare il [**metodo GetPropertyMetrics.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) Le costanti nella tabella seguente che iniziano con "STR" sono rappresentazioni di stringa delle costanti binarie corrispondenti \_ visualizzate nella stessa cella della tabella.




| Costante | Descrizione | 
|----------|-------------|
| <span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl><dt><strong>STR_GUID_X o GUID_PACKETPROPERTY_GUID_X</strong></dt></dl> | Coordinata x nello spazio delle coordinate del tablet. Ogni pacchetto contiene questa proprietà per impostazione predefinita. L'origine (0,0) del tablet è l'angolo superiore sinistro.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Coordinata y nello spazio delle coordinate del tablet. Ogni pacchetto contiene questa proprietà per impostazione predefinita. L'origine (0,0) del tablet è l'angolo superiore sinistro.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Coordinata y nello spazio delle coordinate del tablet. Ogni pacchetto contiene questa proprietà per impostazione predefinita. L'origine (0,0) del tablet è l'angolo superiore sinistro.<br /> | 
| <span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl><dt><strong>STR_GUID_Z o GUID_PACKETPROPERTY_GUID_Z</strong></dt></dl> | Coordinata z o distanza della punta della penna dalla superficie del tablet. Il <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>tipo di enumerazione TabletPropertyMetricUnit</strong></a> determina l'unità di misura per questa proprietà.<br /> | 
| <span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl><dt><strong>STR_GUID_PAKETSTATUS o GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt></dl> | Contiene uno o più dei seguenti valori di flag:<br /><ul><li>Il cursore tocca la superficie di disegno (Valore = 1).</li><li>Il cursore è invertito. Ad esempio, l'estremità della gomma della penna punta verso la superficie (Valore = 2).</li><li>Non usato (valore = 4).</li><li>Viene premuto il pulsante a pressione (Valore = 8).</li></ul> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Ora di generazione del pacchetto.<br /> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Ora di generazione del pacchetto.<br /> | 
| <span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl><dt><strong>STR_GUID_SERIALNUMBER o GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt></dl> | Proprietà del pacchetto per l'identificazione del pacchetto.<br /> Si tratta dello stesso valore utilizzato per recuperare il pacchetto dalla coda di pacchetti.<br /> | 
| <span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl><dt><strong>STR_GUID_NORMALPRESSURE o GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt></dl> | Pressione della punta della penna perpendicolare alla superficie del tablet.<br /> Maggiore è la pressione sulla punta della penna, maggiore sarà l'input penna disegnato.<br /> | 
| <span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl><dt><strong>STR_GUID_TANGENTPRESSURE o GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt></dl> | Pressione della punta della penna lungo il piano della superficie del tablet.<br /> | 
| <span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl><dt><strong>STR_GUID_BUTTONPRESSURE o GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt></dl> | Pressione su un pulsante sensibile alla pressione.<br /> | 
| <span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_XTILTORIENTATION o GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt></dl> | Angolo tra il piano y, z e il piano della penna e dell'asse y.<br /> Si applica a un cursore penna.<br /> Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna si trova a destra della perpendicolare.<br /> | 
| <span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_YTILTORIENTATION o GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt></dl> | Angolo tra il piano x, z e il piano della penna e dell'asse x.<br /> Si applica a un cursore penna.<br /> Il valore è 0 quando la penna è perpendicolare alla superficie di disegno ed è positiva quando la penna è verso l'alto o lontano dall'utente.<br /> | 
| <span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl><dt><strong>STR_GUID_AZIMUTHORIENTATION o GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt></dl> | Rotazione in senso orario del cursore intorno all'asse z attraverso un intervallo circolare completo.<br /> | 
| <span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl><dt><strong>STR_GUID_ALTITUDEORIENTATION o GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt></dl> | Angolo tra l'asse della penna e la superficie del tablet.<br /> Il valore è 0 quando la penna è parallela alla superficie e 90 quando la penna è perpendicolare alla superficie.<br /> I valori sono negativi quando la penna è invertita.<br /> | 
| <span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl><dt><strong>STR_GUID_TWISTORIENTATION o GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt></dl> | Rotazione in senso orario del cursore intorno al proprio asse.<br /> | 
| <span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl><dt><strong>STR_GUID_PITCHROTATION o GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt></dl> | Proprietà del pacchetto che indica se la mancia si trova sopra o sotto una linea orizzontale perpendicolare all'area di scrittura.<br /><blockquote>[!Note]<br />Questa operazione richiede un digitalizzatore 3D.</blockquote><br /> Il valore è positivo se la mancia si trova sopra la riga e negativo se si trova sotto la riga. Ad esempio, se si tiene la penna davanti all'utente e si scrive su una barriera immaginaria, il passo è positivo se la mancia si trova sopra una linea che si estende dall'utente alla barriera.<br /> | 
| <span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl><dt><strong>STR_GUID_ROLLROTATION o GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt></dl> | Rotazione in senso orario della penna intorno al proprio asse. <br /><blockquote>[!Note]<br />Questa operazione richiede un digitalizzatore 3D.</blockquote><br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Angolo della penna a sinistra o a destra intorno al centro dell'asse orizzontale quando la penna è orizzontale.<br /><blockquote>[!Note]<br />Questa operazione richiede un digitalizzatore 3D.</blockquote><br /> Se si tiene la penna davanti all'utente e si scrive su una barriera immaginaria, lo sbarramento zero indica che la penna è perpendicolare alla barriera. Il valore è negativo se la mancia è a sinistra di perpendicolare e positiva se la mancia si trova a destra della perpendicolare.<br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Angolo della penna a sinistra o a destra intorno al centro dell'asse orizzontale quando la penna è orizzontale.<br /><blockquote>[!Note]<br />Questa operazione richiede un digitalizzatore 3D.</blockquote><br /> Se si tiene la penna davanti all'utente e si scrive su una barriera immaginaria, lo sbarramento zero indica che la penna è perpendicolare alla barriera. Il valore è negativo se la mancia è a sinistra di perpendicolare e positiva se la mancia si trova a destra della perpendicolare.<br /> | 
| <span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl><dt><strong>STR_GUID_WIDTH o GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt></dl> | Larghezza dell'area di contatto in un digitalizzatore tocco.<br /> | 
| <span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl><dt><strong>STR_GUID_HEIGHT o GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt></dl> | Altezza dell'area di contatto in un digitalizzatore tocco.<br /> | 
| <span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE o GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt></dl> | Livello di attendibilità del contatto del dito su un digitalizzatore tocco.<br /> | 
| <span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl><dt><strong>STR_GUID_DEVICE_CONTACT_ID o GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt></dl> | Identificatore del contatto del dispositivo per un pacchetto.<br /> | 




## <a name="remarks"></a>Commenti

> [!Note]  
> Tutti i valori dei pacchetti provenienti dall'hardware del tablet sono numeri interi a 32 bit.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IsPacketPropertySupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**Metodo GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**Interfaccia IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




