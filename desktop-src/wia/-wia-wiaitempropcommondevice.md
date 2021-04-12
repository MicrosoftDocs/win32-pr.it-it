---
description: Oltre alle proprietà delle informazioni sul dispositivo, i dispositivi Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema che le applicazioni leggono e scrivono.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Costanti di proprietà del dispositivo comuni (Wiadef. h)
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
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526400"
---
# <a name="common-device-property-constants"></a>Costanti della proprietà del dispositivo comune

Oltre alle proprietà delle informazioni sul dispositivo, i dispositivi Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema che le applicazioni leggono e scrivono. Sono associati all'oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) . Le proprietà del dispositivo rappresentano informazioni sul dispositivo, ad esempio lo stato della connessione e l'ora del dispositivo. A ogni proprietà del dispositivo è associata una stringa di proprietà del dispositivo.

Le costanti della proprietà del dispositivo elencate di seguito sono comuni alla maggior parte o a tutti i dispositivi hardware WIA.

Il prefisso "WIA \_ DPA \_ " indica una proprietà del dispositivo per tutti i dispositivi e rappresenta la convenzione di denominazione usata in C/C++. Per finalità di scripting queste costanti usano il prefisso "Device" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </dl></td>
<td style="text-align: left;">Stato corrente della connessione per il dispositivo. Minidriver crea e gestisce questa proprietà.<br/> Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> La proprietà può includere i valori possibili seguenti.<br/> 
<table>
<thead>
<tr class="header">
<th>Stato connessione</th>
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
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </dl></td>
<td style="text-align: left;"><p>Ora di clock corrente archiviata nel dispositivo. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Questa proprietà è supportata solo dai dispositivi che hanno un clock interno. Se è possibile impostare l'orologio del dispositivo, questa proprietà è di lettura/scrittura; in caso contrario, è di sola lettura.</p>
<p>I dispositivi WIA segnalano l'ora in una struttura <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td style="text-align: left;"><p>Versione del firmware del dispositivo. Questo valore deve essere un valore stringa, ad esempio &quot; 1.0.4 &quot; o &quot; 1,0 ABC &quot; . Minidriver crea e gestisce questa proprietà. Se il minidriver WIA non fornisce una risorsa di versione, il servizio WIA fornisce il valore &quot; 0.0.0.0 &quot; come valore predefinito. Un'applicazione legge questa proprietà per determinare la versione della DLL di minidriver WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
