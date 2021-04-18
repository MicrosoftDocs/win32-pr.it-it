---
title: Tipo complesso timeTriggerType
description: Definisce il tipo di base per l'elemento TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- Utilità di pianificazione di tipo complesso timeTriggerType
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301146"
---
# <a name="timetriggertype-complex-type"></a>Tipo complesso timeTriggerType

Definisce il tipo di base per l'elemento [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                        | Tipo     | Descrizione                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-timetriggertype-element.md) | duration | Specifica il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> S (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi). <br/> |



## <a name="remarks"></a>Commenti

Si noti che questo elemento non aggiunge elementi figlio a quelli definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





