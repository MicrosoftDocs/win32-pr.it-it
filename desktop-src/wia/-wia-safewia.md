---
description: L'oggetto SafeWia è un &0034; sicuro per la creazione di \# script&0034; punto di ingresso per tutte le funzionalità di \# scripting di Windows Image Acquisition (WIA).
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
ms.openlocfilehash: ef324934abee38e2581b6e05c0fdac92145e4f43
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473847"
---
# <a name="safewia-object"></a>Oggetto SafeWia

**L'oggetto SafeWia** è un punto di ingresso "sicuro per lo scripting" per tutte le Windows di scripting wia (Image Acquisition). Qualsiasi applicazione che usa il modello di scripting WIA deve creare un **oggetto SafeWia** [**o Wia.**](-wia-wia.md) Usare tale oggetto per enumerare e creare dispositivi e ricevere notifiche di eventi hardware.

## <a name="members"></a>Membri

**L'oggetto SafeWia** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SafeWia** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](-wia-iwia-create.md) | Il [**metodo Create**](-wia-iwia-create.md) dell'oggetto [**Wia**](-wia-wia.md) crea una connessione al dispositivo WIA specificato e restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto SafeWia** ha queste proprietà.




| Proprietà | Tipo di accesso | Descrizione | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Dispositivi</strong></a><br /> | Sola lettura<br /> | Raccolta di <a href="-wia-deviceinfo.md"><strong>oggetti DeviceInfo</strong></a> che rappresenta tutti i dispositivi installati nel computer. Di sola lettura. <br /><blockquote>[!Note]<br />Questa raccolta è basata su 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Wia**](-wia-wia.md)
</dt> </dl>

 

 




