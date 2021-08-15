---
title: Attività di manutenzione dell'account di accesso
description: Questo argomento descrive i problemi relativi alle attività di manutenzione dell'account di accesso.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- Attività di manutenzione dell'account di accesso AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d026f37ad81d71691ac418ea49b1b0fda5e1d09fb3e4b6e2259083eb80ada9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186633"
---
# <a name="logon-account-maintenance-tasks"></a>Attività di manutenzione dell'account di accesso

Questo argomento descrive i problemi relativi alle attività di manutenzione dell'account di accesso.

Esistono due problemi principali che riguardano le attività di manutenzione dell'account di accesso:

-   Aggiornamento della password dell'account per un'istanza del servizio eseguita con un account utente. Per altre informazioni, vedere [Modifica della password nell'account](changing-the-password-on-a-serviceampaposs-user-account.md)utente di un servizio.
-   Gestione delle modifiche all'account di accesso di un'istanza del servizio.

Quest'ultimo è un caso raro, ma può verificarsi. Il sistema fornisce lo strumento amministrativo Gestione computer che consente di passare a un account di accesso al servizio. Inoltre, altre applicazioni possono usare la [**funzione ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) per specificare un nuovo account di accesso per un servizio installato. Per impostazione predefinita, per modificare un account del servizio sono necessari privilegi di amministratore locale. In questo caso, potrebbe influire sul servizio in due modi:

-   Se sono stati registrati nomi dell'entità servizio (SPN), questi verranno registrati nell'account errato.
-   Se si impostano le voci ACE per concedere l'accesso al servizio, l'accesso verrà concesso all'account errato.

Un approccio consiste nel fare in modo che il programma di installazione del servizio archivi i nomi SPN registrati per ogni istanza del servizio nel Registro di sistema nel computer host. È possibile usare la stessa chiave del Registro di sistema in HKEY LOCAL MACHINE usata per archiviare la stringa \_ di associazione per il servizio \_ SCP. All'avvio del servizio, chiama la [**funzione QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) per determinare il relativo account di accesso e quindi esegue una query sul server Active Directory per determinare se i nomi SPN sono registrati nell'oggetto directory per tale account. Se i nomi SPN non sono registrati o sono registrati nell'account errato, il servizio si rifiuta di avviare e visualizza un messaggio che indica che un amministratore di dominio deve eseguire il programma di configurazione del servizio per aggiornare le impostazioni dell'account di accesso. Tenere presente che questa riconfigurazione deve essere completata da un amministratore perché l'account del servizio non deve avere accesso per aggiornare il proprio nome SPN. Tenere inoltre presente che i nomi SPN devono essere rimossi dall'account precedente, altrimenti i nomi SPN saranno inutili per l'autenticazione perché non sono univoci nella foresta.

 

 