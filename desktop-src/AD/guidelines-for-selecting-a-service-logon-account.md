---
title: Linee guida per la selezione di un account di accesso al servizio
description: Un servizio basato su Win32 può essere eseguito nel contesto di sicurezza di un account utente locale, di un account utente di dominio o dell'account LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Linee guida per la selezione di un account di accesso al servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a976927130a3585be2e6130dbb71b37fa0c69660b6ae953e28909fad3db570f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188675"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Linee guida per la selezione di un account di accesso al servizio

Un servizio basato su Win32 può essere eseguito nel contesto di sicurezza di un account utente locale, di un account utente di dominio o dell'account LocalSystem. Per decidere quale account usare, un amministratore deve installare il servizio con il set minimo di autorizzazioni necessarie per eseguire le operazioni del servizio. In un tipico servizio abilitato per la directory, questo significa che il programma di installazione del servizio deve creare un account utente di dominio per il servizio e concedere a tale account i diritti di accesso e i privilegi specifici richiesti dal servizio in fase di esecuzione. Un servizio deve essere eseguito con l'account LocalSystem solo se il servizio richiede privilegi amministrativi o deve fungere da parte del sistema operativo nel computer locale.

Tenere presente che il programma di installazione del servizio deve, per impostazione predefinita, configurare il servizio per l'esecuzione con un account utente di dominio. Per eseguire il servizio con l'account LocalSystem, il programma di installazione del servizio deve eseguire una query sull'amministratore per ottenere l'autorizzazione necessaria.

Per altre informazioni su descrizioni, vantaggi e svantaggi di ogni tipo di account, vedere:

-   [Account utente locali](local-user-accounts.md).
-   [Account utente di dominio](domain-user-accounts.md).
-   [Account LocalSystem](the-localsystem-account.md).

 

 




