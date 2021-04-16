---
title: Elemento period
description: Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Utilità di pianificazione elemento period
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479229"
---
# <a name="period-element"></a>Elemento period

Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.

Il formato di questa stringa è *PnYnMnDTnHnMnS*, dove *NY* è il numero di anni, NM è il numero di mesi, *ND* è il numero di giorni, *T* è il separatore di data/ora, *NH* è il numero di ore, *nm* è il numero di minuti e *NS* è il numero di secondi (ad esempio, "PT5M" specifica 5 minuti e "P1M4DT2H5M" specifica un mese, quattro giorni, due ore e cinque minuti). Il valore minimo è di un minuto. Per ulteriori informazioni sul tipo di durata, vedere [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

L'elemento **period** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                          | Derivato da                                                                               | Descrizione                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Specifica le impostazioni dell'attività che l'utilità di pianificazione utilizzerà per avviare l'attività durante la manutenzione automatica.<br/> |



## <a name="remarks"></a>Commenti

Per la programmazione in C++, questa impostazione inattiva viene specificata tramite la proprietà [**IMaintenanceSettings::P dere**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce l'attività di manutenzione con requisiti di periodicità impostati su 5 giorni.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
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

 

 





