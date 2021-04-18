---
title: Funzioni di pianificazione
description: Le funzioni del servizio Pianificazione gestione rete inviano e gestiscono i processi che vengono eseguiti in un computer specifico in un determinato momento (o volte) in futuro.
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300286"
---
# <a name="schedule-functions"></a>Funzioni di pianificazione

Le funzioni del servizio Pianificazione gestione rete inviano e gestiscono i processi che vengono eseguiti in un computer specifico in un determinato momento (o volte) in futuro. I processi possono includere comandi e programmi. Le funzioni gestiscono i processi nei computer remoti e locali, purché il servizio di pianificazione sia in esecuzione nel computer.

Le funzioni di pianificazione del servizio sono elencate di seguito.



| Funzione                                                                     | Descrizione                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Invia un processo per l'esecuzione in una data e un'ora future specificate.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Annulla un intervallo di processi in coda per l'esecuzione in un computer.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Elenca i processi accodati in un computer specifico.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Restituisce informazioni su un determinato processo accodato in un computer. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Recupera l'oggetto in corrispondenza del nome dell'account del servizio.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Imposta il nome e la password dell'account del servizio.                   |



 

Affinché le funzioni di pianificazione della gestione di rete abbiano esito positivo, un chiamante deve disporre dei privilegi di amministratore nel computer in cui è in esecuzione il servizio di pianificazione. Le funzioni del servizio di pianificazione sono note anche come funzioni "Job" e "AT Command". Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

La [**struttura \_ info**](/windows/desktop/api/Lmat/ns-lmat-at_info) viene utilizzata dalla funzione [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) per specificare le informazioni quando si invia un processo e dalla funzione [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) per recuperare le informazioni su un processo che è stato inviato. La [**struttura \_ enum**](/windows/desktop/api/Lmat/ns-lmat-at_enum) viene utilizzata da [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) per enumerare e restituire informazioni su un'intera coda di processi inviati.

 

 