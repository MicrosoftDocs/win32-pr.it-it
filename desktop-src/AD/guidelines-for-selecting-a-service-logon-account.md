---
title: Linee guida per la selezione di un account di accesso al servizio
description: Un servizio basato su Win32 può essere eseguito nel contesto di sicurezza di un account utente locale, di un account utente di dominio o dell'account LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Linee guida per la selezione di un account di accesso al servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044110"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Linee guida per la selezione di un account di accesso al servizio

Un servizio basato su Win32 può essere eseguito nel contesto di sicurezza di un account utente locale, di un account utente di dominio o dell'account LocalSystem. Per decidere quale account usare, un amministratore deve installare il servizio con il set minimo di autorizzazioni necessarie per eseguire le operazioni del servizio. In un tipico servizio abilitato per la directory, questo significa che il programma di installazione del servizio deve creare un account utente di dominio per il servizio e concedere all'account i diritti di accesso e i privilegi specifici richiesti dal servizio in fase di esecuzione. Un servizio deve essere eseguito solo con l'account LocalSystem se il servizio richiede privilegi amministrativi o deve agire come parte del sistema operativo nel computer locale.

Tenere presente che, per impostazione predefinita, il programma di installazione del servizio configura il servizio per l'esecuzione con un account utente di dominio. Per eseguire il servizio con l'account LocalSystem, il programma di installazione del servizio deve eseguire una query sull'amministratore per ottenere le autorizzazioni necessarie.

Per ulteriori informazioni sulle descrizioni, i vantaggi e gli svantaggi di ogni tipo di conto, vedere:

-   [Account utente locali](local-user-accounts.md).
-   [Account utente di dominio](domain-user-accounts.md).
-   [Account LocalSystem](the-localsystem-account.md).

 

 




