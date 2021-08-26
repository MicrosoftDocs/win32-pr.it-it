---
title: Elemento Exclusive
description: Indica se l'Utilità di pianificazione deve avviare l'attività durante la manutenzione automatica in modalità esclusiva.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Elementi esclusivi Utilità di pianificazione
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab796abfdcad67a348b6d42186732d402bbe8eeeb359ac772588fe809dbf73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991331"
---
# <a name="exclusive-element"></a>Elemento Exclusive

Indica se l'Utilità di pianificazione deve avviare l'attività durante la manutenzione automatica in modalità esclusiva.

L'esclusività è garantita solo tra altre attività di manutenzione e non concede alcuna priorità di ordinamento dell'attività. Se l'esclusività non è specificata, l'attività viene avviata in parallelo con altre attività di manutenzione.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

**L'elemento Exclusive** è definito dal [**tipo complesso maintenanceSettingsType.**](taskschedulerschema-maintenancesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                          | Derivato da                                                                               | Descrizione                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Specifica le impostazioni dell'attività che verranno usate dall'Utilità di pianificazione per avviare l'attività durante la manutenzione automatica.<br/> |



## <a name="remarks"></a>Commenti

Per la programmazione C++, questa impostazione inattiva viene specificata usando la [**proprietà IMaintenanceSettings::Exclusive.**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definita l'attività di manutenzione con un requisito di scadenza impostato su 15 giorni.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>           |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





