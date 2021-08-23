---
title: Interfacce di trigger
description: Le API usate per gestire i trigger variano a seconda della versione del Utilità di pianificazione. Tuttavia, in entrambi i casi queste API consentono di creare nuovi trigger, recuperare e aggiornare i trigger esistenti ed eliminare i trigger che non sono più necessari.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- trigger Utilità di pianificazione interfacce ,
- trigger Utilità di pianificazione , interfacce, descritte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5515f2b1e2f5b4a7694dec28bb8831c690da0d303cda53338714c1b0e03ddaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002189"
---
# <a name="trigger-interfaces"></a>Interfacce di trigger

Le API usate per gestire i trigger variano a seconda della versione del Utilità di pianificazione. Tuttavia, in entrambi i casi queste API consentono di creare nuovi trigger, recuperare e aggiornare i trigger esistenti ed eliminare i trigger che non sono più necessari.


Le applicazioni sviluppate con Utilità di pianificazione 2.0 possono usare oggetti e interfacce per creare, recuperare, modificare ed eliminare i trigger per un'attività.

Nella figura seguente un'attività specifica una raccolta di trigger usando la relativa proprietà Triggers. Questa raccolta contiene una o più API trigger singole con ogni API che specifica un tipo di trigger specifico. Ad esempio, nella figura seguente la raccolta di trigger contiene un trigger di avvio, un trigger logon e un trigger giornaliero.

![Interfacce trigger dell'Utilità di pianificazione 2.0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>API di oggetti per lo sviluppo di script

Per altre informazioni sui metodi e sulle proprietà degli oggetti usati per specificare i trigger, vedere:

-   [**TaskDefinition**](taskdefinition.md)
-   [**Triggercollection**](triggercollection.md)
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

### <a name="interfaces-apis-for-c-development"></a>API di interfacce per lo sviluppo C++

Per altre informazioni sui metodi e sulle proprietà delle interfacce usate per specificare i trigger, vedere:

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

## <a name="task-scheduler-10-trigger-interfaces"></a>Utilità di pianificazione trigger di Utilità di pianificazione 1.0

Le applicazioni esistenti sviluppate con Utilità di pianificazione 1.0 possono usare i metodi disponibili dalle interfacce di Utilità di pianificazione 1.0 per creare, recuperare, modificare ed eliminare i trigger per un elemento di [*lavoro*](w.md). Si noti tuttavia che tutte le Utilità di pianificazione 1.0, le enumerazioni e le strutture sono obsolete e non devono essere usate per lo sviluppo di nuove applicazioni.

Le due interfacce utilizzate per eseguire questa operazione sono illustrate nella figura seguente. [**L'interfaccia IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) viene usata per gestire tutti i trigger associati a un elemento di lavoro ( tale gestione include la creazione di un nuovo trigger per l'elemento di lavoro). [**L'interfaccia ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) viene usata per gestire un trigger specifico.

![Interfacce trigger dell'Utilità di pianificazione 1.0](images/tsktri2.png)

L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce metodi per la creazione di un nuovo trigger per un elemento di lavoro, il recupero del numero di trigger associati a un elemento di lavoro, il recupero delle strutture dei [*trigger*](t.md) associate all'elemento di lavoro, il recupero delle stringhe [*di trigger*](t.md) associate all'elemento di lavoro e l'eliminazione dei trigger.

Quando l'oggetto trigger è disponibile, è possibile usare l'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) per recuperare la struttura del trigger e la stringa del trigger e impostare i criteri usati per attivare il trigger. Questa interfaccia viene utilizzata solo quando si utilizza un oggetto [*trigger di attività*](t.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger di attività](task-triggers.md)
</dt> <dt>

[Tipi di trigger](trigger-types.md)
</dt> <dt>

[Strutture dei trigger](trigger-structures.md)
</dt> </dl>

 

 