---
title: Utilità di pianificazione per sviluppatori
description: Il Utilità di pianificazione consente di eseguire automaticamente attività di routine in un computer scelto. Utilità di pianificazione esegue questa operazione monitorando i criteri selezionati (definiti trigger) e quindi eseguendo le attività quando tali criteri vengono soddisfatti.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Utilità di pianificazione per sviluppatori
- Utilità di pianificazione per lo sviluppo
- Sviluppo con Utilità di pianificazione
- Utilità di pianificazione, pagina del portale
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: 05edababae87c760f5506d8a40d18ef8dcc59ab35fa78b692cc76b5ad3b46579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357744"
---
# <a name="task-scheduler-for-developers"></a>Utilità di pianificazione per sviluppatori

> [!IMPORTANT]
> Questo argomento e gli altri argomenti di questa sezione sono per un pubblico di sviluppatori. Se si vuole usare il componente Utilità di pianificazione nella capacità come amministratore o come Professional IT, vedere Utilità di pianificazione [.](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler)

## <a name="about-the-task-scheduler"></a>Informazioni sulla Utilità di pianificazione

Il Utilità di pianificazione consente di eseguire automaticamente attività di routine in un computer scelto. Utilità di pianificazione esegue questa operazione monitorando i criteri selezionati (definiti trigger) e quindi eseguendo le attività quando tali criteri vengono soddisfatti.

È possibile usare il Utilità di pianificazione per eseguire attività quali l'avvio di un'applicazione, l'invio di un messaggio di posta elettronica o la visualizzazione di una finestra di messaggio. Le attività possono essere pianificate per l'esecuzione in risposta a questi eventi o trigger. 

- Quando si verifica un evento di sistema specifico.
- In un momento specifico.
- A un'ora specifica in una pianificazione giornaliera.
- A un orario specifico in base a una pianificazione settimanale.
- A un orario specifico in base a una pianificazione mensile.
- A un'ora specifica in una pianificazione mensile del giorno della settimana.
- Quando il computer entra in uno stato di inattività.
- Quando l'attività viene registrata.
- Quando il sistema viene avviato.
- Quando un utente accede.
- Quando una sessione di Terminal Server cambia stato.

## <a name="developers"></a>Sviluppatori

Il Utilità di pianificazione fornisce API in questi moduli.

- Utilità di pianificazione 2.0: interfacce e oggetti vengono forniti rispettivamente per C++ e per lo sviluppo di script.
- Utilità di pianificazione 1.0: le interfacce vengono fornite per lo sviluppo C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

Il Utilità di pianificazione richiede i sistemi operativi seguenti.

- Utilità di pianificazione 2.0: il client richiede Windows Vista o versione precedente. Server richiede Windows Server 2008 o versione precedente.
- Utilità di pianificazione 1.0: il client richiede Windows Vista o Windows XP. Server richiede Windows Server 2008 o Windows Server 2003.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Novità di Utilità di pianificazione](what-s-new-in-task-scheduler.md) | Riepilogo delle nuove funzionalità introdotte dal Utilità di pianificazione. |
| [Informazioni sulla Utilità di pianificazione](about-the-task-scheduler.md) | Informazioni concettuali generali sull'API Utilità di pianificazione. |
| [Uso del Utilità di pianificazione](using-the-task-scheduler.md) | Esempi di codice che illustrano come usare Utilità di pianificazione API. |
| [Utilità di pianificazione riferimento](task-scheduler-reference.md) | Informazioni di riferimento dettagliate per Utilità di pianificazione API e lo schema Utilità di pianificazione dati. |