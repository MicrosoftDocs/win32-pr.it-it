---
title: Condizioni di inattività
description: Un'attività può essere gestita in diversi modi quando il computer entra in uno stato di inattività. Ciò include la definizione di un trigger inattivo o l'impostazione delle condizioni di inattività per l'avvio dell'attività.
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- condizioni di inattività Utilità di pianificazione
- condizioni di inattività Utilità di pianificazione, discussione
- creazione di trigger inattivi Utilità di pianificazione
- trigger inattivi Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501be9b73e3ec355b998697fb5e87c5163224b71
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/19/2020
ms.locfileid: "103734666"
---
# <a name="task-idle-conditions"></a>Condizioni di inattività

Un'attività può essere gestita in diversi modi quando il computer entra in uno stato di inattività. Ciò include la definizione di un trigger inattivo o l'impostazione delle condizioni di inattività per l'avvio dell'attività.

## <a name="detecting-the-idle-state"></a>Rilevamento dello stato di inattività

In Windows 7, il Utilità di pianificazione verifica che il computer si trovi in uno stato di inattività ogni 15 minuti. Utilità di pianificazione verifica lo stato di inattività usando due criteri, ovvero l'assenza dell'utente e il consumo di risorse insufficienti. L'utente viene considerato assente se non è presente alcun input della tastiera o del mouse durante questo periodo di tempo. Il computer è considerato inattivo se tutti i processori e tutti i dischi sono rimasti inattivi per più del 90% dell'ultimo intervallo di rilevamento. Si tratta di un'eccezione per qualsiasi applicazione del tipo di presentazione che imposta gli ES \_ Visualizza il \_ flag obbligatorio. Questo flag forza la pianificazione dell'attività in modo che non consideri il sistema come inattivo, indipendentemente dall'attività dell'utente o dal consumo di risorse.

In Windows 7, Utilità di pianificazione considera inattivo un processore anche quando i thread con priorità bassa (priorità thread < normale) vengono eseguiti.

In Windows 7, quando il Utilità di pianificazione rileva che il computer è inattivo, il servizio attende solo che l'input dell'utente contrassegni la fine dello stato di inattività.

In Windows 8, Utilità di pianificazione esegue gli stessi controlli di utilizzo delle risorse e dell'assenza generale dell'utente. Tuttavia, Utilità di pianificazione si basa sul sottosistema di alimentazione del sistema operativo per rilevare la presenza dell'utente. Per impostazione predefinita, l'utente viene considerato assente dopo quattro minuti senza input della tastiera o del mouse. Il tempo di verifica dell'utilizzo delle risorse viene ridotto a intervalli di 10 minuti quando l'utente è presente. Quando l'utente è distante, il tempo di verifica viene abbreviato a intervalli di 30 secondi. Utilità di pianificazione esegue verifiche aggiuntive sull'utilizzo delle risorse per gli eventi seguenti:

-   Stato di presenza utente modificato
-   Origine alimentazione CA/DC modificata
-   Livello batteria modificato (solo quando sulle batterie)

Quando si verifica uno degli eventi precedenti, Utilità di pianificazione verifica il computer per inattività dopo l'ultimo periodo di verifica. In pratica, questo significa che Utilità di pianificazione possibile dichiarare il sistema come inattivo immediatamente dopo che è stata rilevata l'assenza dell'utente, se le altre condizioni sono state soddisfatte dopo l'ultima ora di verifica.

In Windows 8, le soglie di CPU e IO sono impostate su 80%.

Quando si rileva lo stato di inattività in Windows 8 Server, Utilità di pianificazione non prende in considerazione la presenza o l'assenza dell'utente. Per contrassegnare la fine dello stato di inattività, Utilità di pianificazione rivedere il consumo di risorse una volta in 90 minuti.

## <a name="defining-an-idle-trigger"></a>Definizione di un trigger inattivo

Un'attività può essere avviata quando il computer entra in uno stato di inattività definendo un trigger inattivo.

Un trigger inattivo attiverà un'azione dell'attività solo se il computer entra in uno stato di inattività dopo il limite di inizio del trigger.

Un'applicazione può definire un trigger inattivo tramite l'interfaccia [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

Per la lettura o la scrittura di codice XML, il trigger inattivo viene specificato dall'elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) dello schema utilità di pianificazione.

## <a name="task-settings-for-idle-conditions"></a>Impostazioni attività per le condizioni di inattività

Le impostazioni delle attività possono essere utilizzate per definire il modo in cui il Utilità di pianificazione gestisce l'attività quando il computer entra in uno stato di inattività.

Le illustrazioni seguenti forniscono tre possibili sequenze temporali che mostrano il modo in cui le diverse condizioni di inattività sono correlate tra loro. Tenere presente che le illustrazioni iniziano quando viene attivato il trigger attività o quando l'attività viene avviata su richiesta (senza richiedere di [ignorare i vincoli di attività esistenti](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)).

> [!NOTE]
> Le impostazioni *Duration* e *WaitTimeout* sono deprecate. Sono ancora presenti nel Utilità di pianificazione interfaccia utente e i relativi metodi di interfaccia possono comunque restituire valori validi, ma non vengono più usati.

![sequenza temporale della condizione di inattività](images/idle-conditions2.png)

Nell'elenco seguente vengono descritte le condizioni di inattività.
- Avvio inattivo: ora in cui il computer entra nello stato di inattività.
- Fine inattiva: ora in cui il computer passa dallo stato di inattività. Tenere presente che l'intervallo di tempo in cui il computer è in stato di inattività è indipendente dal tempo di inattività descritto in precedenza.

L'attesa di inattività e la durata inattiva sono state deprecate.
- Idle wait: periodo di tempo durante il quale il Utilità di pianificazione resterà in attesa del verificarsi di uno stato inattivo dopo l'attivazione di un trigger di attività o dopo l'avvio dell'attività su richiesta.
- Durata inattività: periodo di tempo in cui si desidera che il computer sia rimasto inattivo prima di avviare l'attività.

Se, ad esempio, un'attività è impostata per l'avvio solo se il computer è inattivo per 30 minuti e l'attività attende che il computer sia inattivo per 10 minuti, l'attività verrà avviata entro 5 minuti solo se il computer è rimasto inattivo per 25 minuti prima del momento in cui il trigger è stato attivato. L'attività non verrà avviata se il computer entra in uno stato di inattività 5 minuti dopo l'attivazione del trigger.

Per impostazione predefinita, una proprietà [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) dell'attività è impostata su true, il che significa che il servizio di utilità di pianificazione non eseguirà le attività attivate da un trigger inattivo (o un trigger con condizioni di inattività) quando un computer è alimentato a batteria. È possibile modificare questo comportamento impostando la proprietà **DisallowStartIfOnBatteries** su false.

Se un'attività viene attivata da un trigger inattivo, la proprietà [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) dell'interfaccia [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) ([**IdleSettings**](idlesettings.md) per lo scripting) viene ignorata.

Le applicazioni possono controllare le condizioni di inattività impostando le proprietà nelle interfacce [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) e [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

Per la lettura o la scrittura di codice XML, queste condizioni vengono specificate nell'elemento [**Settings**](taskschedulerschema-settings-tasktype-element.md) dello schema utilità di pianificazione.

## <a name="cycling-idle-condition"></a>Condizione di inattività Cycling

Se il computer esegue il ciclo di inattività e lo stato di inattività, è possibile terminare e riavviare l'attività utilizzando le seguenti condizioni di inattività. Per terminare e riavviare un'attività, sia le proprietà che gli elementi devono essere impostati su true:

-   Per terminare l'attività quando la condizione di inattività termina, impostare la proprietà [**StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) o l'elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) su true.
-   Per riavviare l'attività quando il computer esegue di nuovo il ciclo della condizione di inattività, impostare la proprietà [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) o l'elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) su true.
