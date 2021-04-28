---
description: "Costanti delle proprietà relative alle informazioni sul dispositivo : le proprietà relative alle informazioni sul dispositivo sono proprietà che descrivono la configurazione e l'installazione del dispositivo."
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Costanti della proprietà Device Information (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aec37ae84eed6b15bc10a4e979a5d95d21be3423
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097239"
---
# <a name="device-information-property-constants"></a>Costanti delle proprietà relative alle informazioni sul dispositivo

Le proprietà relative alle informazioni sul dispositivo sono proprietà che descrivono la configurazione e l'installazione del dispositivo. Queste proprietà sono disponibili tramite le [**interfacce IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) e anche tramite l'elemento radice. Le proprietà relative alle informazioni sul dispositivo sono precedute dal prefisso "WIA DIP" (proprietà Device Information) e vengono fornite da \_ \_ Windows Image Acquisition (WIA). A scopo di scripting, queste costanti usano il prefisso "DeviceInfo" e fanno parte del tipo [enumerato WiaDeviceInfoPropertyId.](-wia-wiadeviceinfopropertyid.md) Il nome del membro corrispondente dell'enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



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
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </dl></td>
<td style="text-align: left;">Stringa ID dispositivo per il minidriver WIA. Il servizio WIA crea e gestisce questa proprietà.<br/> Tipo: VT_BSTR, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </dl></td>
<td style="text-align: left;">Stringa di descrizione del fornitore per il minidriver WIA. La descrizione del fornitore viene ottenuta dal file INF. Un'applicazione legge questa proprietà per ottenere una descrizione del fornitore del dispositivo. Il servizio WIA crea e gestisce questa proprietà.<br/> Tipo: VT_BSTR, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </dl></td>
<td style="text-align: left;">Stringa di descrizione del dispositivo per il minidriver WIA. Il servizio WIA crea e gestisce questa proprietà. La stringa di descrizione del dispositivo contenuta in questa proprietà viene ottenuta dal file INF. Un'applicazione legge questa proprietà per ottenere una descrizione del dispositivo.<br/> Tipo: VT_BSTR, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </dl></td>
<td style="text-align: left;">Tipo di dispositivo e sottotipo di dispositivo. Il servizio WIA crea e gestisce questa proprietà. Usare la macro GET_STIDEVICE_TYPE per ottenere il tipo di dispositivo. Il tipo di dispositivo e il sottotipo vengono ottenuti dal file INF. Un'applicazione legge questa proprietà per determinare se usa uno scanner, una fotocamera o un dispositivo video.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Attualmente, i tipi di dispositivo sono definiti come indicato di seguito. L'asterisco * indica che il tipo di dispositivo non è supportato da Windows Vista e versioni successive. Il doppio asterisco ** indica che il tipo di dispositivo non è supportato da Windows Server 2003, Windows Vista o versioni successive. <br/> 
<table>
<thead>
<tr class="header">
<th>Type</th>
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>StiDeviceTypeDefault</td>
<td>0x0000</td>
<td>Dispositivo predefinito</td>
</tr>
<tr class="even">
<td>StiDeviceTypeScanner</td>
<td>0x0001</td>
<td>Dispositivo scanner (vedere il <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> per determinare se lo scanner è a schermo piatto o alimentato a fogli).</td>
</tr>
<tr class="odd">
<td>StiDeviceTypeDigitalCamera*</td>
<td>0x0002</td>
<td>Dispositivo fotocamera</td>
</tr>
<tr class="even">
<td>StiDeviceTypeStreamingVideo**</td>
<td>0x0003</td>
<td>Dispositivo video</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </dl></td>
<td style="text-align: left;"><p>Nome della porta del dispositivo installato, assegnato dal driver in modalità kernel che gestisce il dispositivo. Il servizio WIA crea e gestisce questa proprietà. Un'applicazione legge questa proprietà per determinare il nome della porta.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </dl></td>
<td style="text-align: left;"><p>Nome del dispositivo. Il servizio WIA crea e gestisce questa proprietà. Il nome del dispositivo contenuto in questa proprietà viene ottenuto dal file INF. Un'applicazione legge questa proprietà per ottenere il nome del dispositivo.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </dl></td>
<td style="text-align: left;"><p>Nome del server in cui è in esecuzione il minidriver WIA. Questa proprietà è facoltativa per Windows XP e versioni successive.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </dl></td>
<td style="text-align: left;"><p>ID del dispositivo WIA installato in un computer remoto. Il servizio WIA crea e gestisce questa proprietà. Viene usato solo internamente dal servizio WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </dl></td>
<td style="text-align: left;"><p>CLSID fornito dal fornitore per qualsiasi oggetto COM dell'estensione dell'interfaccia utente installato con il minidriver WIA. Il servizio WIA crea e gestisce questa proprietà. Il valore CLSID dell'interfaccia utente contenuto in questa proprietà viene ottenuto dal file INF. Se non viene specificato alcun CLSID dell'interfaccia utente, il servizio WIA fornisce un valore predefinito. Questa proprietà viene usata solo internamente dal servizio WIA quando viene visualizzata l'interfaccia utente.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </dl></td>
<td style="text-align: left;"><p>Tipo di connessione utilizzato dal dispositivo. Il servizio WIA crea e gestisce questa proprietà e solo il servizio WIA può modificarla.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La proprietà può avere i valori possibili seguenti.</p>

<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Dispositivo WDM generico</td>
</tr>
<tr class="even">
<td>2</td>
<td>Dispositivo SCSI</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Dispositivo USB</td>
</tr>
<tr class="even">
<td>8</td>
<td>Dispositivo seriale</td>
</tr>
<tr class="odd">
<td>16</td>
<td>Dispositivo parallelo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </dl></td>
<td style="text-align: left;"><p>Impostazione corrente della velocità in baud per il dispositivo. Il servizio WIA crea e gestisce questa proprietà. Il valore deve essere &quot; Vuoto se il dispositivo non è connesso tramite un cavo &quot; seriale.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </dl></td>
<td style="text-align: left;"><p>Funzionalità sti generiche per il dispositivo ottenute dal file INF. Il servizio WIA crea e gestisce questa proprietà. Un'applicazione legge questa proprietà per determinare le funzionalità STI generiche del dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </dl></td>
<td style="text-align: left;"><p>Numero (come stringa) della versione wi-fi corrente installata nel sistema. Un'applicazione legge questa proprietà per determinare la versione di WIA installata nel sistema. Il servizio WIA crea e gestisce questa proprietà. Questa proprietà è disponibile in Windows XP e versioni successive.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>Versione DLL corrente del minidriver WIA. Il servizio WIA crea e gestisce questa proprietà. Questa proprietà è disponibile in Windows XP e versioni successive.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </dl></td>
<td style="text-align: left;"><p>ID PnP corrente per il dispositivo. Il servizio WIA crea e gestisce questa proprietà. Questa proprietà è disponibile in Windows Vista e versioni successive.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>Versione generica del driver STI. Il servizio WIA crea e gestisce questa proprietà. Un'applicazione legge questa proprietà per determinare la versione generica del driver STI. Questa proprietà è disponibile in Windows Vista e versioni successive.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




