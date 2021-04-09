---
title: Elemento StartWhenAvailable (settingsType)
description: Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il relativo orario pianificato.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Utilità di pianificazione elemento StartWhenAvailable
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963914"
---
# <a name="startwhenavailable-settingstype-element"></a>Elemento StartWhenAvailable (settingsType)

Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il relativo orario pianificato.

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L'elemento **StartWhenAvailable** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Questa proprietà si applica solo alle attività temporizzate.

Per lo sviluppo in C++, vedere [**la proprietà StartWhenAvailable di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).

Per lo sviluppo di script, vedere [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento Settings che consente all'Utilità di pianificazione di avviare l'attività quando è disponibile.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





