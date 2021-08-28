---
description: Oltre alle proprietà relative alle informazioni sul dispositivo, i dispositivi wi-Windows (WIA) hanno valori di proprietà archiviati nel Registro di sistema che le applicazioni leggono e scrivono.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Costanti comuni delle proprietà dei dispositivi (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c5eda1266c8c99f1125e03dfbacc3eb325a69d1d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632179"
---
# <a name="common-device-property-constants"></a>Costanti comuni delle proprietà dei dispositivi

Oltre alle proprietà relative alle informazioni sul dispositivo, i dispositivi wi-Windows (WIA) hanno valori di proprietà archiviati nel Registro di sistema che le applicazioni leggono e scrivono. Sono associati all'oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**all'oggetto IWiaItem2.**](-wia-iwiaitem2.md) Le proprietà del dispositivo rappresentano informazioni sul dispositivo, ad esempio lo stato della connessione e l'ora del dispositivo. A ogni proprietà del dispositivo è associata una stringa di proprietà del dispositivo.

Le costanti delle proprietà del dispositivo elencate di seguito sono comuni alla maggior parte o a tutti i dispositivi hardware WIA.

Il prefisso "WIA DPA" indica una proprietà del dispositivo per tutti i dispositivi ed è la convenzione di denominazione \_ \_ usata in C/C++. A scopo di scripting, queste costanti usano il prefisso "Device" e fanno parte del [tipo enumerato WiaItemPropertyId.](-wia-wiaitempropertyid.md) Il nome del membro corrispondente dell'enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Costante/valore</th>
<th >Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </dl></td>
<td >Stato corrente della connessione per il dispositivo. Il minidriver crea e gestisce questa proprietà.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> La proprietà può avere i valori possibili seguenti.<br/> 
<table>
<thead>
<tr class="header">
<th>Connessione Stato</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DEVICE_NOT_CONNECTED</td>
<td>Il dispositivo non è connesso.</td>
</tr>
<tr class="even">
<td>WIA_DEVICE_CONNECTED</td>
<td>Il dispositivo è connesso e operativo.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </dl></td>
<td ><p>Ora dell'orologio corrente archiviata nel dispositivo. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Accesso: Lettura/Scrittura o Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Questa proprietà è supportata solo dai dispositivi con un orologio interno. Se è possibile impostare l'orologio del dispositivo, questa proprietà è di lettura/scrittura. in caso contrario, è di sola lettura.</p>
<p>I dispositivi WIA segnalano l'ora in <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">una struttura SYSTEMTIME.</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td ><p>Versione del firmware del dispositivo. Questo valore deve essere un valore stringa, ad esempio &quot; 1.0.4 &quot; o &quot; 1.0abc. &quot; Il minidriver crea e gestisce questa proprietà. Se il minidriver WIA non fornisce una risorsa versione, il servizio WIA fornisce il valore &quot; 0.0.0.0 &quot; come valore predefinito. Un'applicazione legge questa proprietà per determinare la versione della DLL del minidriver WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
