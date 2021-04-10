---
title: Elemento ID (networkSettingsType)
description: Contiene un valore GUID che identifica un profilo di rete.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Utilità di pianificazione elemento ID
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121563"
---
# <a name="id-networksettingstype-element"></a>Elemento ID (networkSettingsType)

Contiene un valore GUID che identifica un profilo di rete.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

L'elemento **ID** è definito dal tipo complesso [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                            | Derivato da                                                                       | Descrizione                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete. Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà ID di INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Per lo sviluppo di script, vedere [**NetworkSettings.ID**](networksettings-id.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





