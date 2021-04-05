---
title: Utilità di pianificazione per gli sviluppatori
description: Il Utilità di pianificazione consente di eseguire automaticamente le attività di routine in un computer scelto. Utilità di pianificazione esegue questa operazione monitorando qualsiasi criterio scelto (denominato trigger) e quindi eseguendo le attività quando questi criteri vengono soddisfatti.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Utilità di pianificazione per gli sviluppatori
- Utilità di pianificazione per lo sviluppo
- Sviluppo con Utilità di pianificazione
- Utilità di pianificazione, pagina del portale
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2019
ms.locfileid: "104116941"
---
# <a name="task-scheduler-for-developers"></a>Utilità di pianificazione per gli sviluppatori

> [!IMPORTANT]
> Questo argomento e gli altri argomenti di questa sezione sono destinati a un pubblico di sviluppatori. Se si desidera utilizzare il componente Utilità di pianificazione nella propria capacità di amministratore o di un professionista IT, vedere [utilità di pianificazione](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).

## <a name="about-the-task-scheduler"></a>Informazioni sul Utilità di pianificazione

Il Utilità di pianificazione consente di eseguire automaticamente le attività di routine in un computer scelto. Utilità di pianificazione esegue questa operazione monitorando qualsiasi criterio scelto (denominato trigger) e quindi eseguendo le attività quando questi criteri vengono soddisfatti.

È possibile utilizzare il Utilità di pianificazione per eseguire attività quali l'avvio di un'applicazione, l'invio di un messaggio di posta elettronica o la visualizzazione di una finestra di messaggio. È possibile pianificare l'esecuzione delle attività in risposta a questi eventi o trigger. 

- Quando si verifica un evento di sistema specifico.
- In un momento specifico.
- A un'ora specifica in base a una pianificazione giornaliera.
- A un orario specifico in base a una pianificazione settimanale.
- A un orario specifico in base a una pianificazione mensile.
- In un momento specifico, in base a una pianificazione mensile giornaliera della settimana.
- Quando il computer entra in uno stato di inattività.
- Quando l'attività è registrata.
- Quando viene avviato il sistema.
- Quando un utente esegue l'accesso.
- Quando una sessione di Terminal Server cambia stato.

## <a name="developers"></a>Sviluppatori

Il Utilità di pianificazione fornisce le API in questi formati.

- Utilità di pianificazione 2,0: le interfacce e gli oggetti vengono forniti rispettivamente per C++ e per lo sviluppo di script.
- Utilità di pianificazione 1,0: le interfacce sono fornite per lo sviluppo in C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

Il Utilità di pianificazione richiede i sistemi operativi seguenti.

- Utilità di pianificazione 2,0: il client richiede Windows Vista o versione successiva. Il server richiede Windows Server 2008 o versione successiva.
- Utilità di pianificazione 1,0: il client richiede Windows Vista o Windows XP. Il server richiede Windows Server 2008 o Windows Server 2003.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Novità di Utilità di pianificazione](what-s-new-in-task-scheduler.md) | Riepilogo delle nuove funzionalità introdotte dal Utilità di pianificazione. |
| [Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md) | Informazioni concettuali generali sull'API Utilità di pianificazione. |
| [Uso della Utilità di pianificazione](using-the-task-scheduler.md) | Esempi di codice che illustrano come usare le API Utilità di pianificazione. |
| [Riferimento Utilità di pianificazione](task-scheduler-reference.md) | Informazioni di riferimento dettagliate per le API Utilità di pianificazione e lo schema di Utilità di pianificazione. |