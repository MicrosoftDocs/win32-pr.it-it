---
title: Elemento NetworkSettings (settingsType)
description: Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento RunOnlyIfNetworkAvailable è impostato su true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Utilità di pianificazione elemento NetworkSettings
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477464"
---
# <a name="networksettings-settingstype-element"></a>Elemento NetworkSettings (settingsType)

Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

L'elemento **NetworkSettings** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                      | Derivato da                                                         | Descrizione                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Impostazioni (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà NetworkSettings di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Per lo sviluppo di script, vedere [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





