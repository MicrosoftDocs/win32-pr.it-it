---
description: L'uso corretto dei criteri di restrizione software può rendere l'azienda più agile perché fornisce un framework proattivo per la prevenzione dei problemi, anziché un framework reattivo che si basa sulla costosa alternativa di ripristino di un sistema dopo che si è verificato un problema. I criteri di restrizione software sono stati introdotti con il rilascio di Microsoft Windows XP per proteggere i sistemi da codice sconosciuto e potenzialmente pericoloso. I criteri di restrizione forniscono un meccanismo in cui solo al codice attendibile viene assegnato l'accesso senza restrizioni ai privilegi di un utente. Il codice sconosciuto, che potrebbe contenere virus o codice in conflitto con i programmi attualmente installati, può essere eseguito solo in un ambiente vincolato (spesso denominato sandbox) in cui non è consentito l'accesso a qualsiasi privilegio utente sensibile alla sicurezza.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Uso dei criteri di restrizione software in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e823d794cccf590ddf9ffd8fcb6f7982eb1543368e400ab3632601ec3a2b96e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304937"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Uso dei criteri di restrizione software in COM+

L'uso corretto dei criteri di restrizione software può rendere l'azienda più agile perché fornisce un framework proattivo per la prevenzione dei problemi, anziché un framework reattivo che si basa sulla costosa alternativa di ripristino di un sistema dopo che si è verificato un problema. I criteri di restrizione software sono stati introdotti con il rilascio di Microsoft Windows XP per proteggere i sistemi da codice sconosciuto e potenzialmente pericoloso. I criteri di restrizione forniscono un meccanismo in cui solo al codice attendibile viene assegnato l'accesso senza restrizioni ai privilegi di un utente. Il codice sconosciuto, che potrebbe contenere virus o codice in conflitto con i programmi attualmente installati, può essere eseguito solo in un ambiente vincolato (spesso denominato *sandbox)* in cui non è consentito l'accesso a qualsiasi privilegio utente sensibile alla sicurezza.

I criteri di restrizione software dipendono dall'assegnazione di livelli di attendibilità al codice che può essere eseguito in un sistema. Attualmente esistono due livelli di attendibilità: Senza restrizioni e Non consentito. Al codice con un livello di attendibilità Senza restrizioni viene assegnato l'accesso senza restrizioni ai privilegi dell'utente, pertanto questo livello di attendibilità deve essere applicato solo al codice completamente attendibile. Al codice con un livello di attendibilità Non consentito non è consentito l'accesso a qualsiasi privilegio utente sensibile alla sicurezza e può essere eseguito solo in una sandbox che impedisce al codice senza restrizioni di caricare il codice non consentito nello spazio indirizzi.

La configurazione dei criteri di restrizione software per un sistema viene eseguita tramite lo strumento amministrativo Criteri di sicurezza locali, mentre la configurazione dei criteri di restrizione delle singole applicazioni COM+ viene eseguita a livello di codice o tramite lo strumento amministrativo Servizi componenti. Se il livello di attendibilità dei criteri di restrizione non è specificato per un'applicazione COM+, verranno usate le impostazioni a livello di sistema per determinare il livello di attendibilità dell'applicazione. Le impostazioni dei criteri di restrizione COM+ devono essere coordinate attentamente con le impostazioni a livello di sistema perché un'applicazione COM+ con un livello di attendibilità Senza restrizioni può caricare solo i componenti con un livello di attendibilità Senza restrizioni. Un'applicazione COM+ non consentita può caricare componenti con qualsiasi livello di attendibilità, ma non può accedere a tutti i privilegi dell'utente.

Oltre ai livelli di attendibilità dei criteri di restrizione software delle singole applicazioni COM+, altre due proprietà determinano come vengono usati i criteri di restrizione per tutte le applicazioni COM+. Se [SRPRunningObjectChecks è](/windows/desktop/com/srprunningobjectchecks) abilitato, i tentativi di connessione agli oggetti in esecuzione verranno verificati per i livelli di attendibilità appropriati. L'oggetto in esecuzione non può avere un livello di attendibilità meno stringente rispetto all'oggetto client. Ad esempio, l'oggetto in esecuzione non può avere un livello di attendibilità Non consentito se l'oggetto client ha un livello di attendibilità Senza restrizioni.

La seconda proprietà determina il modo in cui i criteri di restrizione software gestisce le connessioni activate-as-activator. Se [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) è abilitato, il livello di attendibilità configurato per l'oggetto server viene confrontato con il livello di attendibilità dell'oggetto client e il livello di attendibilità più stringente verrà utilizzato per eseguire l'oggetto server. Se SRPActivateAsActivatorChecks non è abilitato, l'oggetto server verrà eseguito con il livello di attendibilità dell'oggetto client indipendentemente dal livello di attendibilità con cui è stato configurato. Per impostazione predefinita, sia SRPRunningObjectChecks che SRPActivateAsActivatorChecks sono abilitati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Configurazione dei criteri di restrizione software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Sicurezza delle applicazioni della libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni multilivello](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> </dl>

 

 
