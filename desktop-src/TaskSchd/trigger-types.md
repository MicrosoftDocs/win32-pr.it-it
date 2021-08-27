---
title: Tipi di trigger
description: I trigger basati sul tempo e sugli eventi descritti di seguito consentono di avviare le attività in diversi modi.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- trigger Utilità di pianificazione tipi ,
- trigger di avvio Utilità di pianificazione
- trigger di avvio Utilità di pianificazione , descritto
- Trigger di registrazione Utilità di pianificazione
- trigger di registrazione Utilità di pianificazione , descritto
- Trigger di calendario Utilità di pianificazione
- calendar trigger Utilità di pianificazione , descritto
- trigger giornalieri Utilità di pianificazione
- daily trigger Utilità di pianificazione , descritto
- trigger settimanale Utilità di pianificazione
- trigger settimanale Utilità di pianificazione , descritto
- trigger mensile Utilità di pianificazione
- trigger mensile Utilità di pianificazione , descritto
- Trigger monthlyDOW Utilità di pianificazione
- Descrizione del trigger monthlyDOW Utilità di pianificazione
- trigger di evento Utilità di pianificazione
- trigger di evento Utilità di pianificazione , descritto
- Trigger logon Utilità di pianificazione
- trigger logon Utilità di pianificazione , descritto
- trigger inattivo Utilità di pianificazione
- trigger inattivo Utilità di pianificazione , descritto
- Trigger giorno della settimana Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0e09b6ecc1ac3c817f374e70c6756fa09afc78ccaac7e549f3f04ad074c8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099691"
---
# <a name="trigger-types"></a>Tipi di trigger

I trigger basati sul tempo e sugli eventi descritti di seguito consentono di avviare le attività in diversi modi.

## <a name="task-scheduler-20-triggers"></a>Utilità di pianificazione 2.0

I tipi di trigger seguenti sono definiti [**dall'enumerazione TASK \_ TRIGGER \_ TYPE2.**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)

| Trigger                                                                                                                                                                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Trigger di evento (trigger basato su eventi) Per lo sviluppo di script, vedere [**EventTrigger.**](eventtrigger.md)<br/> Per lo sviluppo in C++, [**vedere IEventTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)<br/> Per lo sviluppo XML, vedere [**Elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Avvia l'attività quando si verifica un evento di sistema specifico.                                                                                                                                         |
| Trigger temporale (trigger basato sul tempo)Per lo sviluppo di script, vedere [**TimeTrigger.**](timetrigger.md)<br/> Per lo sviluppo in C++, [**vedere ITimeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)<br/> Per lo sviluppo XML, vedere [**Elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Avvia l'attività in una data e un'ora specifiche.                                                                                                                                                 |
| Trigger giornaliero (trigger di calendario basato sul tempo)Per lo sviluppo di script, vedere [**DailyTrigger.**](dailytrigger.md)<br/> Per lo sviluppo in C++, [**vedere IDailyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)<br/> Per lo sviluppo XML, vedere [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Avvia l'attività a un'ora specifica in base a una pianificazione giornaliera. Ad esempio, l'attività inizia alle 8:00 ogni giorno o ogni altro giorno.                                                                |
| Trigger settimanale (trigger di calendario basato sul tempo)Per lo sviluppo di script, vedere [**WeeklyTrigger.**](weeklytrigger.md)<br/> Per lo sviluppo in C++, vedere [**IWeeklyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)<br/> Per lo sviluppo XML, vedere [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Avvia l'attività a un'ora specifica in base a una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 di un giorno specifico della settimana ogni settimana o in un giorno specifico della settimana ogni altra settimana. |
| Trigger mensile (trigger di calendario basato sul tempo)Per lo sviluppo di script, vedere [**MonthlyTrigger.**](monthlytrigger.md)<br/> Per lo sviluppo in C++, vedere [**IMonthlyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)<br/> Per lo sviluppo XML, vedere [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Avvia l'attività a un'ora specifica in base a una pianificazione mensile. Ad esempio, l'attività inizia alle 8:00 in giorni specifici del mese in mesi specifici.                                          |
| Trigger dow mensile (trigger di calendario basato sul tempo)Per lo sviluppo di script, vedere [**MonthlyDOWTrigger.**](monthlydowtrigger.md)<br/> Per lo sviluppo in C++, vedere [**IMonthlyDOWTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)<br/> Per lo sviluppo XML, vedere [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Avvia l'attività a un'ora specifica in base a una pianificazione mensile del giorno della settimana. Ad esempio, l'attività inizia alle 8:00 in giorni specifici della settimana, settimane del mese e mesi dell'anno.      |
| Trigger inattivo (trigger basato su eventi)Per lo sviluppo di script, vedere [**IdleTrigger.**](idletrigger.md)<br/> Per lo sviluppo in C++, vedere [**IIdleTrigger.**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)<br/> Per lo sviluppo XML, vedere [**Elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Avvia l'attività quando il computer entra in uno stato di inattività.                                                                                                                                      |
| Trigger di registrazione (trigger basato su eventi)Per lo sviluppo di script, vedere [**RegistrationTrigger.**](registrationtrigger.md)<br/> Per lo sviluppo in C++, [**vedere IRegistrationTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)<br/> Per lo sviluppo XML, vedere [**Elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Avvia l'attività quando l'attività viene registrata o aggiornata.                                                                                                                                      |
| Trigger di avvio (trigger basato su eventi)Per lo sviluppo di script, [**vedere BootTrigger.**](boottrigger.md)<br/> Per lo sviluppo in C++, [**vedere IBootTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)<br/> Per lo sviluppo XML, vedere [**Elemento BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Avvia l'attività all'avvio del sistema.                                                                                                                                                   |
| Trigger logon (trigger basato su eventi)Per lo sviluppo di script, vedere [**LogonTrigger.**](logontrigger.md)<br/> Per lo sviluppo in C++, [**vedere ILogonTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)<br/> Per lo sviluppo XML, vedere [**Elemento LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Avvia l'attività quando un utente esegue l'accesso.                                                                                                                                                         |
| Trigger di modifica dello stato della sessione (trigger basato su eventi)Per lo sviluppo di script, vedere [**SessionStateChangeTrigger.**](sessionstatechangetrigger.md)<br/> Per lo sviluppo in C++, vedere [**ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger)<br/> Per lo sviluppo XML, vedere [**Elemento SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Avvia l'attività quando viene modificato lo stato di una sessione di Terminal Server.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>trigger Utilità di pianificazione 1.0

I tipi di trigger seguenti sono definiti [**dall'enumerazione TASK \_ TRIGGER \_ TYPE.**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) Per implementare uno dei trigger seguenti, vedere la struttura [**TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)

-   Una volta attivato: avvia l'attività una sola volta.
-   Trigger giornaliero: avvia l'attività a intervalli giornalieri.
-   Trigger settimanale: avvia l'attività in base a una pianificazione settimanale.
-   Trigger mensile: avvia l'attività in base a una pianificazione mensile.
-   Trigger DOW mensile: avvia l'attività in base a una pianificazione mensile del giorno della settimana.
-   In caso di trigger inattivo: avvia l'attività quando il computer è in uno stato di inattività.
-   Trigger di avvio del sistema: avvia l'attività all'avvio del computer.
-   Trigger di accesso: avvia l'attività quando un utente specifico esegue l'accesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger di attività](task-triggers.md)
</dt> <dt>

[Interfacce di trigger](trigger-interfaces.md)
</dt> <dt>

[Strutture dei trigger](trigger-structures.md)
</dt> </dl>

 

