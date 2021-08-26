---
title: Elemento DisallowStartOnRemoteAppSession (settingsType)
description: Specifica che l'attività non verrà avviata se attivata per l'esecuzione in una sessione REMOTE Applications Integrated Locally (RAIL).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Elemento DisallowStartOnRemoteAppSession Utilità di pianificazione
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2f7834ecd57fa10aaaabfa21945f1e908834d535d50f94b4dd21e6ca45c0a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010801"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>Elemento DisallowStartOnRemoteAppSession (settingsType)

Specifica che l'attività non verrà avviata se attivata per l'esecuzione in una sessione REMOTE Applications Integrated Locally (RAIL).

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**L'elemento DisallowStartOnRemoteAppSession** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

L'impostazione predefinita per questo elemento è False.

Per lo sviluppo C++, queste informazioni sono accessibili tramite la proprietà [**ITaskSettings2::D isallowStartOnRemoteAppSession.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento settings che non consente l'avvio dell'attività se l'attività viene attivata per l'esecuzione in una sessione RAIL.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





