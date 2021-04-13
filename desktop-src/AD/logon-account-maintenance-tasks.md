---
title: Attività di manutenzione dell'account di accesso
description: In questo argomento vengono descritti i problemi relativi alle attività di manutenzione degli account di accesso.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- Attività di manutenzione account di accesso AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0f11f69d9a974fd666871833029eda0e059329
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104398830"
---
# <a name="logon-account-maintenance-tasks"></a>Attività di manutenzione dell'account di accesso

In questo argomento vengono descritti i problemi relativi alle attività di manutenzione degli account di accesso.

Esistono due problemi principali che riguardano le attività di manutenzione degli account di accesso:

-   Aggiornamento della password dell'account per un'istanza del servizio in esecuzione con un account utente. Per ulteriori informazioni, vedere [modifica della password nell'account utente di un servizio](changing-the-password-on-a-serviceampaposs-user-account.md).
-   Gestione delle modifiche apportate all'account di accesso di un'istanza del servizio.

Quest'ultimo è un caso raro, ma può verificarsi. Il sistema fornisce lo strumento di amministrazione Gestione computer che consente di passare a un account di accesso al servizio. Inoltre, altre applicazioni possono utilizzare la funzione [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) per specificare un nuovo account di accesso per un servizio installato. Per impostazione predefinita, i privilegi di amministratore locale sono necessari per modificare un account del servizio. In tal caso, potrebbe influire sul servizio in due modi:

-   Se sono stati registrati nomi dell'entità servizio (SPN), questi verranno registrati nell'account errato.
-   Se si impostano le voci ACE per concedere l'accesso al servizio, ora si concede l'accesso all'account errato.

Un approccio consiste nel fare in modo che il programma di installazione del servizio memorizzi i nomi SPN registrati per ogni istanza del servizio nel registro di sistema nel computer host. È possibile usare la stessa chiave del registro di sistema nel \_ computer locale HKEY \_ usato per archiviare la stringa di binding per il servizio SCP. All'avvio del servizio, viene chiamata la funzione [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) per determinare il relativo account di accesso, quindi viene eseguita una query sul server Active Directory per determinare se gli SPN sono registrati nell'oggetto directory per l'account. Se gli SPN non sono registrati o sono registrati nell'account errato, il servizio rifiuta di avviarsi e visualizza un messaggio che informa che un amministratore di dominio deve eseguire il programma di configurazione del servizio per aggiornare le impostazioni dell'account di accesso. Tenere presente che questa riconfigurazione deve essere completata da un amministratore perché l'account del servizio non deve avere accesso per aggiornare il proprio nome SPN. Tenere inoltre presente che i nomi SPN devono essere rimossi dall'account precedente; in caso contrario, gli SPN saranno inutili per l'autenticazione perché non sono univoci nella foresta.

 

 