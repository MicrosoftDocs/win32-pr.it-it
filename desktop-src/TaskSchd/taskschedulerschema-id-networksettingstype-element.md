---
title: Elemento Id (networkSettingsType)
description: Contiene un valore GUID che identifica un profilo di rete.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Elemento Id Utilità di pianificazione
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06196710b9db9d39d45a24b78bccabf479ef210a97f3cea1fd19286b76f2fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125841"
---
# <a name="id-networksettingstype-element"></a>Elemento Id (networkSettingsType)

Contiene un valore GUID che identifica un profilo di rete.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

**L'elemento Id** è definito dal [**tipo complesso networkSettingsType.**](taskschedulerschema-networksettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                            | Derivato da                                                                       | Descrizione                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete. Il Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **True.**<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, [**vedere Proprietà Id di INetworkSettings.**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id)

Per lo sviluppo di script, [**vedere NetworkSettings.Id**](networksettings-id.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





