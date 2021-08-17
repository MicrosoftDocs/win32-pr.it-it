---
title: Criteri di restrizione software
description: Le impostazioni dei criteri di restrizione software sono state introdotte con il rilascio di Windows XP per proteggere i sistemi da codice sconosciuto e potenzialmente pericoloso.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23176b23be5fcf4dc45f040f53e5d8f9dfbcdf05a8aee87feabd125d05c5372d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129803"
---
# <a name="software-restriction-policy"></a>Criteri di restrizione software

Le impostazioni dei criteri di restrizione software sono state introdotte con il rilascio di Windows XP per proteggere i sistemi da codice sconosciuto e potenzialmente pericoloso. Il provider di servizi di configurazione fornisce un meccanismo in cui solo al codice attendibile viene assegnato l'accesso senza restrizioni ai privilegi di un utente. Il codice sconosciuto, che potrebbe contenere virus o codice in conflitto con i programmi attualmente installati, può essere eseguito solo in un ambiente vincolato (spesso denominato *sandbox)* in cui non è consentito l'accesso a qualsiasi privilegio utente sensibile alla sicurezza. L'uso corretto di SRP può rendere l'azienda più agile perché fornisce un framework proattivo per la prevenzione dei problemi, anziché un framework reattivo che si basa sulla costosa alternativa di ripristino di un sistema dopo che si è verificato un problema.

Il punto di distribuzione dipende dall'assegnazione di livelli di attendibilità al codice che può essere eseguito in un sistema. Attualmente esistono due livelli di attendibilità: Senza restrizioni e Non consentito. Al codice con un livello di attendibilità Senza restrizioni viene assegnato l'accesso senza restrizioni ai privilegi dell'utente, pertanto questo livello di attendibilità deve essere applicato solo al codice completamente attendibile. Al codice con un livello di attendibilità Non consentito non è consentito l'accesso a qualsiasi privilegio utente sensibile alla sicurezza e può essere eseguito solo in una sandbox, in modo che il codice senza restrizioni non possa caricare il codice non consentito nello spazio indirizzi.

La configurazione SRP delle singole applicazioni COM viene eseguita tramite il [valore SRPTrustLevel](srptrustlevel.md) nella chiave [AppID](appid-key.md) dell'applicazione nel Registro di sistema. Se il livello di attendibilità SRP non è specificato per un'applicazione COM, viene usato il valore predefinito Non consentito. Un'applicazione COM con un livello di attendibilità Senza restrizioni ha accesso illimitato ai privilegi dell'utente, ma può caricare solo i componenti con un livello di attendibilità Senza restrizioni, mentre un'applicazione COM non consentita può caricare componenti con qualsiasi livello di attendibilità, ma non può accedere ad alcun privilegio utente sensibile alla sicurezza.

Oltre ai livelli di attendibilità SRP delle singole applicazioni COM, altre due proprietà SRP determinano il modo in cui il componente SRP viene usato per tutte le applicazioni COM. Se [L'opzione SRPRunningObjectChecks è](srprunningobjectchecks.md) abilitata, i tentativi di connessione agli oggetti in esecuzione verranno verificati per i livelli di attendibilità SRP appropriati. L'oggetto in esecuzione non può avere un livello di attendibilità SRP meno stringente rispetto all'oggetto client. Ad esempio, l'oggetto in esecuzione non può avere un livello di attendibilità Non consentito se l'oggetto client ha un livello di attendibilità Senza restrizioni.

La seconda proprietà determina il modo in cui il punto di connessione del punto di attivazione gestisce le connessioni activate-as-activator. Se [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) è abilitato, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità più stringente verrà usato per eseguire l'oggetto server. Se **SRPActivateAsActivatorChecks** non è abilitato, l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è stato configurato. Per impostazione predefinita, **sia SRPRunningObjectChecks** che **SRPActivateAsActivatorChecks** sono abilitati.

 

 




