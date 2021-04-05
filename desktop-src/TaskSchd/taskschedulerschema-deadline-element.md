---
title: Elemento scadenza
description: Specifica quando l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione automatica.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Utilità di pianificazione elemento scadenza
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740831"
---
# <a name="deadline-element"></a>Elemento scadenza

Specifica quando l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione automatica.

Il formato di questa stringa è *PnYnMnDTnHnMnS*, dove *NY* è il numero di anni, NM è il numero di mesi, *ND* è il numero di giorni, *T* è il separatore di data/ora, *NH* è il numero di ore, *nm* è il numero di minuti e *NS* è il numero di secondi (ad esempio, "PT5M" specifica 5 minuti e "P1M4DT2H5M" specifica un mese, quattro giorni, due ore e cinque minuti). Il valore minimo è di un minuto. Per ulteriori informazioni sul tipo di durata, vedere [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration). La scadenza minima che un'attività può utilizzare è 1 giorno. Il valore dell'elemento **scadenza** deve essere maggiore del valore dell'elemento [**period**](taskschedulerschema-period-element.md) . Se non viene specificata la scadenza, l'attività non verrà avviata durante la manutenzione automatica di emergenza.

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

L'elemento **scadenza** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                          | Derivato da                                                                               | Descrizione                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Specifica le impostazioni dell'attività che l'utilità di pianificazione utilizzerà per avviare l'attività durante la manutenzione automatica.<br/> |



## <a name="remarks"></a>Commenti

Per la programmazione in C++, questa impostazione inattiva viene specificata tramite la proprietà [**IMaintenanceSettings::D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario dei mesi che esegue l'attività a marzo.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
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

 

 





