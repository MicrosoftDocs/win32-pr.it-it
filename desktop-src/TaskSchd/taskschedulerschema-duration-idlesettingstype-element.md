---
title: Elemento Duration (idleSettingsType)
description: Specifica per quanto tempo il computer deve essere inattivo prima dell'esecuzione dell'attività.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Elemento Duration Utilità di pianificazione
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46523caa10f96d7dd76947540932107106ad0d5c8a4b7f26fc6f6d5bebb40325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356568"
---
# <a name="duration-idlesettingstype-element"></a>Elemento Duration (idleSettingsType)

Specifica per quanto tempo il computer deve essere inattivo prima dell'esecuzione dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Il valore minimo è un minuto. Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
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
```

L'elemento è definito dal tipo [**complesso idleSettingsType.**](taskschedulerschema-idlesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in uno stato di inattività.<br/> |



## <a name="remarks"></a>Commenti

Per la programmazione di script, questa impostazione di inattività viene specificata usando la [**proprietà IdleSettings.IdleDuration.**](idlesettings-idleduration.md)

Per la programmazione C++, questa impostazione di inattività viene specificata usando la [**proprietà IIdleSettings::IdleDuration.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definita un'impostazione di inattività che consente 5 minuti per l'avvio dell'attività.


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





