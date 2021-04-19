---
title: Tipo complesso idleSettingsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento IdleSettings (settingsType).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- Utilità di pianificazione di tipo complesso idleSettingsType
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301332"
---
# <a name="idlesettingstype-complex-type"></a>Tipo complesso idleSettingsType

Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) .

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="WaitTimeout"
            default="PT1H"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                  | Tipo    | Descrizione                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)                |         | Specifica la quantità di tempo consentita per l'avvio dell'attività in una condizione di inattività.<br/>                                                                                                                     |
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean | L'attività viene riavviata non appena viene avviata una condizione di inattività.<br/>                                                                                                                                             |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean | Specifica che l'attività viene terminata se la condizione di inattività termina prima del superamento della durata di inattività.<br/>                                                                                                 |
| [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | Specifica la quantità di tempo di attesa per l'avvio di una condizione di inattività. Se per questo elemento non viene specificato alcun valore, il servizio di Utilità di pianificazione attenderà per un periodo di tempo indefinito che si verifichi una condizione di inattività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





