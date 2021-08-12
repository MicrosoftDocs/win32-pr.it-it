---
title: Tipo complesso taskType (Utilità di pianificazione)
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- Tipo complesso taskType Utilità di pianificazione
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e2465773fb784c87fe560bdc8f6306771578cb22cf9aa26bf79b84867deb61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611058"
---
# <a name="tasktype-complex-type"></a>Tipo complesso taskType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**l'elemento Task.**](taskschedulerschema-task-element.md)

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo                                                                                 | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | Specifica le azioni eseguite dall'attività.<br/>                                                                             |
| [**Dati**](taskschedulerschema-data-tasktype-element.md)                         | [**dataType**](taskschedulerschema-datatype-complextype.md)                         | Specifica i dati di addizione associati all'attività, ma che altrimenti non vengono usati dal Utilità di pianificazione servizio.<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/>                                                 |
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | Specifica i trigger che avviano l'attività.<br/>                                                                              |



## <a name="attributes"></a>Attributi



| Nome    | Tipo                                                              | Descrizione                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| version | [**versionType**](taskschedulerschema-versiontype-simpletype.md) | Specifica la versione dell'attività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





