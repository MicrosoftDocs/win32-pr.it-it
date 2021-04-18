---
description: L'oggetto SafeWia è un &\# 0034; Safe per lo scripting&\# 0034; punto di ingresso per tutte le funzionalità di scripting Windows Image Acquisition (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Oggetto SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307340"
---
# <a name="safewia-object"></a>Oggetto SafeWia

L'oggetto **SafeWia** è un punto di ingresso "Safe per lo scripting" per tutte le funzionalità di scripting Windows Image Acquisition (WIA). Qualsiasi applicazione che utilizza il modello di scripting WIA deve creare un oggetto **SafeWia** o [**WIA**](-wia-wia.md) . Usare tale oggetto per enumerare e creare i dispositivi e ricevere notifiche di eventi hardware.

## <a name="members"></a>Membri

L'oggetto **SafeWia** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SafeWia** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](-wia-iwia-create.md) | Il metodo [**create**](-wia-iwia-create.md) dell'oggetto [**WIA**](-wia-wia.md) esegue una connessione al dispositivo WIA specificato e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SafeWia** dispone di queste proprietà.



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
| IID<br/>                      | \_SAFEWIA CLSID<br/>                                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WIA**](-wia-wia.md)
</dt> </dl>

 

 




