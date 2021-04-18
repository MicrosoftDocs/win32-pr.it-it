---
title: Tipi di trigger
description: I trigger basati sul tempo e sugli eventi descritti di seguito consentono di avviare le attività in diversi modi.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- attiva Utilità di pianificazione, tipi
- Utilità di pianificazione trigger di avvio
- trigger di avvio Utilità di pianificazione, descritto
- Utilità di pianificazione trigger di registrazione
- Utilità di pianificazione trigger di registrazione, descritto
- Utilità di pianificazione trigger calendario
- trigger del calendario Utilità di pianificazione, descritto
- trigger giornaliero Utilità di pianificazione
- trigger giornaliero Utilità di pianificazione, descritto
- Utilità di pianificazione trigger settimanale
- Utilità di pianificazione trigger settimanale, descritto
- trigger mensile Utilità di pianificazione
- trigger mensile Utilità di pianificazione, descritto
- Utilità di pianificazione trigger monthlyDOW
- Utilità di pianificazione trigger monthlyDOW, descritto
- Utilità di pianificazione trigger evento
- Utilità di pianificazione trigger evento, descritto
- Utilità di pianificazione trigger LOGON
- Utilità di pianificazione trigger LOGON, descritto
- Utilità di pianificazione Trigger inattivo
- Trigger inattivo Utilità di pianificazione, descritto
- trigger giorno della settimana Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee1e846e4b2fa8138f675cdd39e926884d2bfae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300200"
---
# <a name="trigger-types"></a>Tipi di trigger

I trigger basati sul tempo e sugli eventi descritti di seguito consentono di avviare le attività in diversi modi.

## <a name="task-scheduler-20-triggers"></a>Trigger Utilità di pianificazione 2,0

I tipi di trigger seguenti sono definiti dall' [**enumerazione \_ \_ tipo2 del trigger di attività**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .

| Trigger                                                                                                                                                                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Trigger di evento (trigger basato su evento) per lo sviluppo di script, vedere [**EventTrigger**](eventtrigger.md).<br/> Per lo sviluppo in C++, vedere [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger).<br/> Per lo sviluppo XML, vedere [**elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Avvia l'attività quando si verifica un evento di sistema specifico.                                                                                                                                         |
| Trigger di ora (trigger basato sul tempo) per lo sviluppo di script, vedere [**TimeTrigger**](timetrigger.md).<br/> Per lo sviluppo in C++, vedere [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger).<br/> Per lo sviluppo XML, vedere [**elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Avvia l'attività in una data e a un'ora specifiche.                                                                                                                                                 |
| Trigger giornaliero (trigger di calendario basato sul tempo) per lo sviluppo di script, vedere [**DailyTrigger**](dailytrigger.md).<br/> Per lo sviluppo in C++, vedere [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger).<br/> Per lo sviluppo XML, vedere [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Avvia l'attività in un momento specifico in base a una pianificazione giornaliera. Ad esempio, l'attività inizia alle 8:00 AM ogni giorno o ogni altro giorno.                                                                |
| Trigger settimanale (trigger di calendario basato sul tempo) per lo sviluppo di script, vedere [**WeeklyTrigger**](weeklytrigger.md).<br/> Per lo sviluppo in C++, vedere [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger).<br/> Per lo sviluppo XML, vedere [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Avvia l'attività in un momento specifico in base a una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 in un giorno specifico della settimana ogni settimana o in un giorno specifico della settimana ogni altra settimana. |
| Trigger mensile (trigger di calendario basato sul tempo) per lo sviluppo di script, vedere [**MonthlyTrigger**](monthlytrigger.md).<br/> Per lo sviluppo in C++, vedere [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger).<br/> Per lo sviluppo XML, vedere [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Avvia l'attività in un momento specifico in base a una pianificazione mensile. Ad esempio, l'attività inizia alle 8:00 in giorni specifici del mese per mesi specifici.                                          |
| Trigger mensile del giorno della settimana (DOW) (trigger di calendario basato sul tempo) per lo sviluppo di script, vedere [**MonthlyDOWTrigger**](monthlydowtrigger.md).<br/> Per lo sviluppo in C++, vedere [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger).<br/> Per lo sviluppo XML, vedere [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Avvia l'attività in un momento specifico in base a una pianificazione mensile del giorno della settimana. Ad esempio, l'attività inizia alle 8:00 in giorni specifici della settimana, settimane del mese e mesi dell'anno.      |
| Trigger inattivo (trigger basato su eventi) per lo sviluppo di script, vedere [**IdleTrigger**](idletrigger.md).<br/> Per lo sviluppo in C++, vedere [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger).<br/> Per lo sviluppo XML, vedere [**elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Avvia l'attività quando il computer entra in uno stato di inattività.                                                                                                                                      |
| Trigger di registrazione (trigger basato su eventi) per lo sviluppo di script, vedere [**RegistrationTrigger**](registrationtrigger.md).<br/> Per lo sviluppo in C++, vedere [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger).<br/> Per lo sviluppo XML, vedere [**elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Avvia l'attività quando l'attività viene registrata o aggiornata.                                                                                                                                      |
| Trigger di avvio (trigger basato su eventi) per lo sviluppo di script, vedere [**BootTrigger**](boottrigger.md).<br/> Per lo sviluppo in C++, vedere [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger).<br/> Per lo sviluppo XML, vedere [**elemento BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Avvia l'attività quando viene avviato il sistema.                                                                                                                                                   |
| Trigger LOGON (trigger basato su eventi) per lo sviluppo di script, vedere [**LogonTrigger**](logontrigger.md).<br/> Per lo sviluppo in C++, vedere [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger).<br/> Per lo sviluppo XML, vedere [**elemento LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Avvia l'attività quando un utente esegue l'accesso.                                                                                                                                                         |
| Trigger di modifica dello stato della sessione (trigger basato su eventi) per lo sviluppo di script, vedere [**SessionStateChangeTrigger**](sessionstatechangetrigger.md).<br/> Per lo sviluppo in C++, vedere [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger).<br/> Per lo sviluppo XML, vedere [**elemento SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Avvia l'attività quando una sessione di Terminal Server modifica lo stato.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Trigger Utilità di pianificazione 1,0

I tipi di trigger seguenti sono definiti dall'enumerazione del [**\_ \_ tipo di trigger dell'attività**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) . Per implementare uno dei trigger seguenti, vedere la struttura [**del \_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .

-   Once trigger: avvia l'attività una sola volta.
-   Trigger giornaliero: avvia l'attività su un intervallo giornaliero.
-   Trigger settimanale: avvia l'attività in base a una pianificazione settimanale.
-   Trigger mensile: avvia l'attività in base a una pianificazione mensile.
-   Trigger DOW mensile: avvia l'attività in base a una pianificazione mensile del giorno della settimana.
-   On Idle trigger: avvia l'attività quando il computer si trova in uno stato di inattività.
-   Trigger di avvio del sistema: avvia l'attività quando il computer viene avviato.
-   Logon Trigger: avvia l'attività quando un utente specifico accede.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger attività](task-triggers.md)
</dt> <dt>

[Interfacce trigger](trigger-interfaces.md)
</dt> <dt>

[Strutture trigger](trigger-structures.md)
</dt> </dl>

 

