---
description: L'oggetto WIA è il punto di ingresso per tutte le funzionalità di scripting di Windows Image Acquisition (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: WIA (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129379"
---
# <a name="wia-object"></a>WIA (oggetto)

L'oggetto **WIA** è il punto di ingresso per tutte le funzionalità di scripting di Windows Image Acquisition (WIA). Qualsiasi applicazione che utilizza il modello di scripting WIA deve creare un oggetto [**SafeWia**](-wia-safewia.md) o **WIA** . Usare tale oggetto per enumerare e creare i dispositivi e ricevere notifiche di eventi hardware.

> [!Note]  
> Questo oggetto non è sicuro per lo scripting. Per una versione di questo oggetto sicura per gli script, vedere [**SafeWia**](-wia-safewia.md).

 

## <a name="members"></a>Membri

L'oggetto **WIA** presenta questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

L'oggetto **WIA** presenta questi eventi.



| Event                                                                 | Descrizione                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Evento che si verifica quando si connette un nuovo dispositivo hardware WIA.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Evento che si verifica quando un nuovo dispositivo hardware WIA viene disconnesso.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Evento che si verifica quando un trasferimento dei dati viene completato correttamente.<br/> |



 

### <a name="methods"></a>Metodi

L'oggetto **WIA** presenta questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](-wia-iwia-create.md) | Il metodo [**create**](-wia-iwia-create.md) dell'oggetto **WIA** esegue una connessione al dispositivo WIA specificato e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **WIA** dispone di queste proprietà.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Proprietà</th>
<th style="text-align: left;">Tipo di accesso</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Dispositivi</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Raccolta di oggetti <a href="-wia-deviceinfo.md"><strong>deviceInfo</strong></a> che rappresenta tutti i dispositivi installati nel computer. Di sola lettura. <br/>
<blockquote>
[!Note]<br />
Questa raccolta è in base 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |
| IID<br/>                      | \_WIA CLSID<br/>                                                                                         |



 

 




