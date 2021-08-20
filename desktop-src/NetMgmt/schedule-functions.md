---
title: Funzioni di pianificazione
description: Le funzioni del servizio di pianificazione della gestione della rete inviano e gestiscono i processi eseguiti in un computer specifico in un determinato momento (o in orari) in futuro.
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d6ee895dd4e62d555db977c9689bd5ab172bf2bf2a88744e3bbb09d2ca61df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796807"
---
# <a name="schedule-functions"></a>Funzioni di pianificazione

Le funzioni del servizio di pianificazione della gestione della rete inviano e gestiscono i processi eseguiti in un computer specifico in un determinato momento (o in orari) in futuro. I processi possono includere comandi e programmi. Le funzioni gestiscono i processi nei computer remoti e locali, a condizione che il servizio di pianificazione sia in esecuzione nel computer.

Le funzioni del servizio di pianificazione sono elencate di seguito.



| Funzione                                                                     | Descrizione                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Invia un processo da eseguire in una data e un'ora future specificate.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Annulla un intervallo di processi accodati per l'esecuzione in un computer.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Elenca i processi accodati in un computer specificato.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Restituisce informazioni su un processo specifico accodato in un computer. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Recupera il nome dell'account del servizio AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Imposta il nome e la password dell'account del servizio AT.                   |



 

Per il funzionamento delle funzioni di pianificazione della gestione della rete, un chiamante deve disporre dei privilegi di amministratore nel computer in cui è in esecuzione il servizio di pianificazione. Le funzioni del servizio di pianificazione sono note anche come funzioni "Job" e "AT command". Per altre informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [Esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

La struttura [**AT \_ INFO**](/windows/desktop/api/Lmat/ns-lmat-at_info) viene usata dalla funzione [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) per specificare le informazioni durante l'invio di un processo e dalla funzione [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) per recuperare informazioni su un processo inviato. La [**struttura \_ AT ENUM**](/windows/desktop/api/Lmat/ns-lmat-at_enum) viene usata da [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) per enumerare e restituire informazioni su un'intera coda di processi inviati.

 

 