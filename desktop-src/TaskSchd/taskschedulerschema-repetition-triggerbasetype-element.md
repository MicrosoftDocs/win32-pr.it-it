---
title: Elemento Repetition (triggerBaseType)
description: Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Elemento di ripetizione Utilità di pianificazione
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477777"
---
# <a name="repetition-triggerbasetype-element"></a>Elemento Repetition (triggerBaseType)

Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

L'elemento di **ripetizione** è definito dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                     | Derivato da                                                                               | Descrizione                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando viene avviato il sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando l'attività è registrata.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando viene attivato il trigger.<br/>             |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                   | Tipo     | Descrizione                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Durata**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | Specifica il tempo di ripetizione del pattern.<br/>                                                              |
| [**Interval**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | Specifica la quantità di tempo tra ogni riavvio dell'attività.<br/>                                           |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean  | Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.<br/> |



## <a name="remarks"></a>Commenti

Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.

Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata cinque volte. Le cinque ripetizioni possono essere definite dal modello seguente.

1.  Un'attività viene avviata all'inizio del primo minuto.
2.  L'attività successiva inizia alla fine del primo minuto.
3.  L'attività successiva inizia alla fine del secondo minuto.
4.  L'attività successiva inizia alla fine del terzo minuto.
5.  L'attività successiva inizia alla fine del quarto minuto.

**Windows Server 2003, Windows XP e windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata quattro volte.

**Windows Vista, Windows 7, Windows server 2008, Windows 8 e Windows server 2012:** In genere, l'impostazione della durata della ripetizione su un multiplo esatto dell'intervallo produce i numeri descritti in precedenza. Tuttavia, in determinate condizioni di carico elevato, è possibile che la durata di timeout venga avviata prima che TaskScheduler possa avviare l'intervallo di attività finale.

Per lo sviluppo di script, il modello di ripetizione viene specificato utilizzando la proprietà [**trigger. ripetition**](trigger-repetition.md) ereditata da tutti gli oggetti trigger.

Per lo sviluppo in C++, il modello di ripetizione viene specificato utilizzando la proprietà [**ITRigger:: ripetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) ereditata da tutte le interfacce del trigger.

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento trigger di avvio che specifica un modello di ripetizione per un trigger.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





