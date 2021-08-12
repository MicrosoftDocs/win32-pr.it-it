---
title: Elemento WaitTimeout (idleSettingsType)
description: Specifica il periodo di tempo in cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- Elemento WaitTimeout Utilità di pianificazione
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d078acecf39f9bd4848cabaa8b203787049ca8a66e565e6183b8b1998389ad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610396"
---
# <a name="waittimeout-idlesettingstype-element"></a>Elemento WaitTimeout (idleSettingsType)

Specifica il periodo di tempo in cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività. Se per questo elemento non viene specificato alcun valore, il servizio Utilità di pianificazione attenderà per un tempo indefinito che si verifichi una condizione di inattività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> . Il tempo minimo consentito è 1 minuto.

``` syntax
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
```

L'elemento è definito dal tipo complesso [**idleSettingsType.**](taskschedulerschema-idlesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in stato di inattività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, questa impostazione inattiva viene specificata tramite la [**proprietà IdleSettings.WaitTimeout.**](idlesettings-waittimeout.md)

Per lo sviluppo C++, questa impostazione inattiva viene specificata usando la [**proprietà IIdleSettings::WaitTimeout.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un'impostazione di inattività che attende 24 ore per il verificarsi di una condizione di inattività.


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





