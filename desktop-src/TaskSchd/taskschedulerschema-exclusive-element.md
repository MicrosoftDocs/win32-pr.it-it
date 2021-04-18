---
title: Elemento Exclusive
description: Indica se l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica in modalità esclusiva.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Elemento esclusivo Utilità di pianificazione
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301152"
---
# <a name="exclusive-element"></a>Elemento Exclusive

Indica se l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica in modalità esclusiva.

L'esclusività è garantita solo tra altre attività di manutenzione e non concede alcuna priorità di ordinamento dell'attività. Se l'esclusività non è specificata, l'attività viene avviata in parallelo con altre attività di manutenzione.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

L'elemento **Exclusive** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                          | Derivato da                                                                               | Descrizione                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Specifica le impostazioni dell'attività che l'utilità di pianificazione utilizzerà per avviare l'attività durante la manutenzione automatica.<br/> |



## <a name="remarks"></a>Commenti

Per la programmazione in C++, questa impostazione di inattività viene specificata tramite la proprietà [**IMaintenanceSettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce l'attività di manutenzione con requisito di scadenza impostato su 15 giorni.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





