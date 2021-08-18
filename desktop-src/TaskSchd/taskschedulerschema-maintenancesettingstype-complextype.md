---
title: Tipo complesso maintenanceSettingsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- tipo complesso maintenanceSettingsType Utilità di pianificazione
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0733d16ec929b4e67774fc436c1530b67d70392b2655525b2aaaa642c2ea346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139204"
---
# <a name="maintenancesettingstype-complex-type"></a>Tipo complesso maintenanceSettingsType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**l'elemento MaintenanceSettings.**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)

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
| [**Scadenza**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Specifica l'intervallo di tempo dopo il quale l'Utilità di pianificazione tenterà di avviare l'attività durante la manutenzione automatica di emergenza, se non è stato possibile completarla durante la manutenzione regolare.<br/> |
| **Exclusive**                                                                  | boolean | Se impostato su true, l'attività verrà avviata esclusivamente tra le altre attività di manutenzione.<br/>                                                                                                 |
| [**Periodo**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.<br/>                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>           |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





