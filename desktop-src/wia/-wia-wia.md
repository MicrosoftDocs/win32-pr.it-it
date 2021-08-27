---
description: L'oggetto Wia è il punto di ingresso per tutte le Windows di scripting WIA (Image Acquisition).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Oggetto Wia
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
ms.openlocfilehash: 38dc5f7ac4440320827e009a7fd38dd6554ceb70
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469618"
---
# <a name="wia-object"></a>Oggetto Wia

**L'oggetto Wia** è il punto di ingresso per tutte le Windows di scripting WIA (Image Acquisition). Qualsiasi applicazione che usa il modello di scripting WIA deve creare un [**oggetto SafeWia**](-wia-safewia.md) **o Wia.** Usare tale oggetto per enumerare e creare dispositivi e per ricevere notifiche di eventi hardware.

> [!Note]  
> Questo oggetto non è sicuro per lo scripting. Per una versione di questo oggetto sicura per lo scripting, vedere [**SafeWia.**](-wia-safewia.md)

 

## <a name="members"></a>Membri

**L'oggetto Wia** ha questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

**L'oggetto Wia** include questi eventi.



| Event                                                                 | Descrizione                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Evento che si verifica quando viene connesso un nuovo dispositivo hardware WIA.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Evento che si verifica quando un nuovo dispositivo hardware WIA viene disconnesso.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Evento che si verifica quando un trasferimento dei dati viene completato correttamente.<br/> |



 

### <a name="methods"></a>Metodi

**L'oggetto Wia** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](-wia-iwia-create.md) | Il [**metodo Create**](-wia-iwia-create.md) dell'oggetto **Wia** effettua una connessione al dispositivo WIA specificato e restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto Wia** ha queste proprietà.




| Proprietà | Tipo di accesso | Descrizione | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Dispositivi</strong></a><br /> | Sola lettura<br /> | Raccolta di <a href="-wia-deviceinfo.md"><strong>oggetti DeviceInfo</strong></a> che rappresenta tutti i dispositivi installati nel computer. Di sola lettura. <br /><blockquote>[!Note]<br />Questa raccolta è in base 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |
| IID<br/>                      | CLSID \_ Wia<br/>                                                                                         |



 

 




