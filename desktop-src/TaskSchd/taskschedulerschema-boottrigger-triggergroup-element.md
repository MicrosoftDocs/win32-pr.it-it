---
title: Elemento BootTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando viene avviato il sistema.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- trigger di avvio Utilità di pianificazione, elemento XML
- Utilità di pianificazione elemento BootTrigger
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340952"
---
# <a name="boottrigger-triggergroup-element"></a>Elemento BootTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando viene avviato il sistema.

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

L'elemento **BootTrigger** è definito dal tipo complesso [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                        | Tipo                                                                     | Descrizione                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo (bootTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                           | duration                                                                 | Specifica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.<br/>                            |
| [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Specifica che il trigger è abilitato.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.<br/>                                   |
| [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Specifica la data e l'ora di attivazione del trigger.<br/>                                                              |



## <a name="attributes"></a>Attributi



| Nome | Tipo       | Descrizione                               |
|------|------------|-------------------------------------------|
| Id   | **string** | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, un trigger di avvio viene definito dall'oggetto [**BootTrigger**](boottrigger.md) .

Per lo sviluppo in C++, un trigger di avvio viene definito dall'oggetto [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) .

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger di avvio, vedere [esempio di trigger di avvio (XML)](boot-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





