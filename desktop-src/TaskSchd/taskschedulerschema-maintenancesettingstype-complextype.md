---
title: Tipo complesso maintenanceSettingsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- Utilità di pianificazione di tipo complesso maintenanceSettingsType
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742762"
---
# <a name="maintenancesettingstype-complex-type"></a>Tipo complesso maintenanceSettingsType

Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                        | Tipo    | Descrizione                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Scadenza**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Specifica il periodo di tempo dopo il quale l'utilità di pianificazione tenterà di avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione.<br/> |
| **Exclusive**                                                                  | boolean | Se è impostato su true, l'attività verrà avviata esclusivamente tra le altre attività di manutenzione.<br/>                                                                                                 |
| [**Periodo**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.<br/>                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





