---
title: Interfacce trigger
description: Le API usate per gestire i trigger variano a seconda della versione del Utilità di pianificazione. In entrambi i casi, tuttavia, queste API consentono di creare nuovi trigger, recuperare e aggiornare i trigger esistenti ed eliminare i trigger che non sono più necessari.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- trigger Utilità di pianificazione, interfacce
- attiva Utilità di pianificazione, interfacce, descritte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339714"
---
# <a name="trigger-interfaces"></a>Interfacce trigger

Le API usate per gestire i trigger variano a seconda della versione del Utilità di pianificazione. In entrambi i casi, tuttavia, queste API consentono di creare nuovi trigger, recuperare e aggiornare i trigger esistenti ed eliminare i trigger che non sono più necessari.


Le applicazioni sviluppate con Utilità di pianificazione 2,0 possono usare oggetti e interfacce per creare, recuperare, modificare ed eliminare i trigger per un'attività.

Nell'illustrazione seguente un'attività specifica una raccolta di trigger usando la relativa proprietà Triggers. Questa raccolta contiene una o più API di trigger singole con ogni API che specifica un tipo di trigger specifico. Nell'illustrazione seguente, ad esempio, la raccolta di trigger contiene un trigger di avvio, un trigger LOGON e un trigger giornaliero.

![interfacce del trigger dell'utilità di pianificazione 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>API oggetto per lo sviluppo di script

Per ulteriori informazioni sui metodi e sulle proprietà degli oggetti utilizzati per specificare i trigger, vedere:

-   [**TaskDefinition**](taskdefinition.md)
-   [**TriggerCollection**](triggercollection.md)
-   [**Trigger**](trigger.md)
-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>Interfacce API per lo sviluppo in C++

Per ulteriori informazioni sui metodi e sulle proprietà delle interfacce utilizzate per specificare i trigger, vedere:

-   [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**ITrigger**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>Interfacce del trigger Utilità di pianificazione 1,0

Le applicazioni esistenti sviluppate con Utilità di pianificazione 1,0 possono usare i metodi disponibili dalle interfacce Utilità di pianificazione 1,0 per creare, recuperare, modificare ed eliminare i trigger per un [*elemento di lavoro*](w.md). Si noti, tuttavia, che tutte le interfacce, le enumerazioni e le strutture Utilità di pianificazione 1,0 sono obsolete e non devono essere utilizzate per lo sviluppo di nuove applicazioni.

Le due interfacce usate per eseguire questa operazione sono illustrate nella figura seguente. L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) viene utilizzata per gestire tutti i trigger associati a un elemento di lavoro. tale gestione include la creazione di un nuovo trigger per l'elemento di lavoro. L'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) viene utilizzata per gestire un trigger specifico.

![interfacce del trigger dell'utilità di pianificazione 1,0](images/tsktri2.png)

L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce metodi per la creazione di un nuovo trigger per un elemento di lavoro, il recupero del numero di trigger associati a un elemento di lavoro, il recupero delle [*strutture di trigger*](t.md) associate all'elemento di lavoro, il recupero delle stringhe del [*trigger*](t.md) associate all'elemento di lavoro e l'eliminazione dei trigger.

Una volta che l'oggetto trigger è disponibile, è possibile usare l'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) per recuperare la struttura del trigger e la stringa del trigger e per impostare i criteri usati per attivare il trigger. Questa interfaccia viene utilizzata solo quando si utilizza un [*oggetto trigger di attività*](t.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger attività](task-triggers.md)
</dt> <dt>

[Tipi di trigger](trigger-types.md)
</dt> <dt>

[Strutture trigger](trigger-structures.md)
</dt> </dl>

 

 