---
title: Elemento Deadline
description: Specifica quando l'Utilità di pianificazione deve avviare l'attività durante la manutenzione automatica di emergenza, se non è stato possibile completarla durante la manutenzione automatica normale.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Elemento Deadline Utilità di pianificazione
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19d5560b57cfaa2a3fd3fa5167d13fa1722fe3f7dd736f19742e2efc895e15e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857311"
---
# <a name="deadline-element"></a>Elemento Deadline

Specifica quando l'Utilità di pianificazione deve avviare l'attività durante la manutenzione automatica di emergenza, se non è stato possibile completarla durante la manutenzione automatica normale.

Il formato di questa stringa è *PnYnMnDTnHnMnS,* dove *nY* è il numero di anni, nM è il numero di mesi, *nD* è il numero di giorni, *T* è il separatore di data/ora, *nH* è il numero di ore, *nM* è il numero di minuti e *nS* è il numero di secondi (ad esempio, "PT5M" specifica 5 minuti e "P1M4DT2H5M" specifica un mese, quattro giorni, due ore e cinque minuti). Il valore minimo è un minuto. Per altre informazioni sul tipo di durata, vedere [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration). Scadenza minima che un'attività può usare è di 1 giorno. Il valore **dell'elemento Deadline** deve essere maggiore del valore dell'elemento Period. [](taskschedulerschema-period-element.md) Se non viene specificata la scadenza, l'attività non verrà avviata durante la manutenzione automatica di emergenza.

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento Deadline** è definito dal [**tipo complesso maintenanceSettingsType.**](taskschedulerschema-maintenancesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                          | Derivato da                                                                               | Descrizione                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Specifica le impostazioni dell'attività che verranno usate dall'Utilità di pianificazione per avviare l'attività durante la manutenzione automatica.<br/> |



## <a name="remarks"></a>Commenti

Per la programmazione C++, questa impostazione di inattività viene specificata usando la proprietà [**IMaintenanceSettings::D eadline.**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività nel mese di marzo.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
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

 

 





