---
title: Elemento Name (networkSettingsType)
description: Contiene il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Utilità di pianificazione elemento Name
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518070"
---
# <a name="name-networksettingstype-element"></a>Elemento Name (networkSettingsType)

Contiene il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

L'elemento **Name** è definito dal tipo complesso [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                            | Derivato da                                                                       | Descrizione                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**proprietà Name di INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Per lo sviluppo di script, vedere [**NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





