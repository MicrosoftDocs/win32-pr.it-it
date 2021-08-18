---
title: Elemento NetworkSettings (settingsType)
description: Contiene le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete. Il Utilità di pianificazione verifica la disponibilità di questa rete quando l'elemento RunOnlyIfNetworkAvailable è impostato su True.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Elemento NetworkSettings Utilità di pianificazione
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b81e1ff2a9f03646d124f5fd2d3aae27f18069f4b32631f9f8d9e66a193ac3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758481"
---
# <a name="networksettings-settingstype-element"></a>Elemento NetworkSettings (settingsType)

Contiene le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete. Il Utilità di pianificazione verifica la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **True.**

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

**L'elemento NetworkSettings** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                      | Derivato da                                                         | Descrizione                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Impostazioni (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere [**Proprietà NetworkSettings di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Per lo sviluppo di script, vedere [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





