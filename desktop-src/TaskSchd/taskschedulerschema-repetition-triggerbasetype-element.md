---
title: Elemento Repetition (triggerBaseType)
description: Specifica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Elemento Repetition Utilità di pianificazione
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dfcce3e008a9959ca279f64c83a898eb2239d007d8fc32dfb5da5942395055bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959541"
---
# <a name="repetition-triggerbasetype-element"></a>Elemento Repetition (triggerBaseType)

Specifica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

**L'elemento Repetition** è definito dal [**tipo complesso triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                     | Derivato da                                                                               | Descrizione                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività all'avvio del sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Specifica un trigger giornaliero, settimanale, mensile o mensile del giorno della settimana.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando l'attività viene registrata.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il trigger viene attivato.<br/>             |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                   | Tipo     | Descrizione                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Durata**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | Specifica per quanto tempo il criterio viene ripetuto.<br/>                                                              |
| [**Intervallo**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | Specifica l'intervallo di tempo tra ogni riavvio dell'attività.<br/>                                           |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean  | Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.<br/> |



## <a name="remarks"></a>Commenti

Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.

Se si registra un'attività che contiene un trigger con un intervallo di ripetizione pari a un minuto e una durata di ripetizione pari a quattro minuti, l'attività verrà avviata cinque volte. Le cinque ripetizioni possono essere definite nel modello seguente.

1.  Un'attività inizia all'inizio del primo minuto.
2.  L'attività successiva inizia alla fine del primo minuto.
3.  L'attività successiva inizia alla fine del secondo minuto.
4.  L'attività successiva inizia alla fine del terzo minuto.
5.  L'attività successiva inizia alla fine del quarto minuto.

**Windows Server 2003, Windows XP e Windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione pari a un minuto e una durata di ripetizione pari a quattro minuti, l'attività verrà avviata quattro volte.

**Windows Vista, Windows 7, Windows Server 2008, Windows 8 e Windows Server 2012:** In genere, l'impostazione della durata della ripetizione su un multiplo esatto dell'intervallo produce i numeri descritti in precedenza. Tuttavia, in determinate condizioni di carico elevato, è possibile che si sia verificato un timeout per la durata prima che TaskScheduler possa avviare l'intervallo di attività finale.

Per lo sviluppo di script, il modello di ripetizione viene specificato usando [**la proprietà Trigger.Repetition**](trigger-repetition.md) ereditata da tutti gli oggetti trigger.

Per lo sviluppo in C++, il modello di ripetizione viene specificato usando la proprietà [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) ereditata da tutte le interfacce del trigger.

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento trigger di avvio che specifica un modello di ripetizione per un trigger.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
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

 

 





