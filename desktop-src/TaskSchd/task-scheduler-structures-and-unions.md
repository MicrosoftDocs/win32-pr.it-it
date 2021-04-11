---
title: Strutture e unioni Utilità di pianificazione
description: Elenca le strutture e le unioni usate dalle API Utilità di pianificazione 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Utilità di pianificazione Utilità di pianificazione, riferimento, strutture e unioni
- attiva Utilità di pianificazione, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221043"
---
# <a name="task-scheduler-structures-and-unions"></a>Strutture e unioni Utilità di pianificazione

In questa sezione vengono descritte le strutture e le unioni utilizzate dalle API di Utilità di pianificazione.

Tutte le strutture e le unioni seguenti vengono usate da Utilità di pianificazione 1,0.



| Nome                                               | Descrizione                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**GIORNALIERA**](/windows/desktop/api/Mstask/ns-mstask-daily)                             | Definisce l'intervallo, in giorni, in cui viene eseguita un'attività.                                                                          |
| [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | Definisce il giorno del mese in cui l'attività viene eseguita.                                                                                 |
| [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | Definisce la data o le date in cui l'attività viene eseguita per mese, settimana e giorno della settimana.                                                     |
| [**\_trigger attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | Definisce gli orari per l'esecuzione di un [*elemento di lavoro*](w.md)pianificato.                                                  |
| [**\_Unione del tipo di trigger \_**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | Definisce la pianificazione della chiamata del trigger all'interno del membro del **tipo** di una struttura di [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . |
| [**SETTIMANALE**](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | Definisce l'intervallo, in settimane, tra le chiamate di un'attività.                                                                  |



 

 

 




