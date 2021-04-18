---
description: L'oggetto DeviceInfo fornisce l'accesso alle proprietà di un dispositivo hardware Windows Image Acquisition (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Oggetto DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312440"
---
# <a name="deviceinfo-object"></a>Oggetto DeviceInfo

L'oggetto **deviceInfo** fornisce l'accesso alle proprietà di un dispositivo hardware Windows Image Acquisition (WIA). Inoltre, tramite il metodo [**create**](-wia-iwiadeviceinfo-create.md) , fornisce un modo per l'applicazione o lo script per la connessione al dispositivo e per ottenere un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo. Usare il metodo [**Devices**](-wia-iwia-devices.md) per ottenere una raccolta di oggetti **deviceInfo** .

## <a name="members"></a>Membri

L'oggetto **deviceInfo** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **deviceInfo** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](-wia-iwiadeviceinfo-create.md)           | Il metodo [**create**](-wia-iwiadeviceinfo-create.md) dell'oggetto **deviceInfo** esegue una connessione al dispositivo WIA specificato dall'oggetto **deviceInfo** e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | Il metodo [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) dell'oggetto **DEVICEINFO** usa l'ID di una proprietà del dispositivo per restituirne il valore.<br/>                                                                                               |



 

### <a name="properties"></a>Proprietà

L'oggetto **deviceInfo** dispone di queste proprietà.



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
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-id.md"><strong>ID</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Recupera l'ID del dispositivo hardware WIA. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Produttore</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Recupera il nome del produttore del dispositivo hardware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-name.md"><strong>Nome</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Nome del dispositivo hardware WIA così come appare nell'interfaccia utente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-port.md"><strong>Porta</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Recupera la porta a cui è connessa la periferica hardware WIA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Recupera il tipo di dispositivo hardware WIA. I valori possibili sono: <br/>
<ul>
<li>DigitalCamera</li>
<li>Scanner</li>
<li>StreamingVideo</li>
<li>Predefinito</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Recupera l'ID di classe dell'interfaccia utente fornita dal produttore per questo dispositivo hardware WIA. Il valore è una rappresentazione in forma di stringa di un GUID. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




