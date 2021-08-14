---
title: Elemento Name (networkSettingsType)
description: Contiene il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Nome dell'elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41b92c7e63a820c2a2a34378b041bec3a49f432b52887a732c3f3bfd360b10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758501"
---
# <a name="name-networksettingstype-element"></a>Elemento Name (networkSettingsType)

Contiene il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

**L'elemento** Name è definito dal [**tipo complesso networkSettingsType.**](taskschedulerschema-networksettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                            | Derivato da                                                                       | Descrizione                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete. Il Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **True.**<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà Name di INetworkSettings.**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name)

Per lo sviluppo di script, [**vedere NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





