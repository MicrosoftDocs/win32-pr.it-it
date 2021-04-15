---
description: Il corretto uso dei criteri di restrizione software può rendere l'azienda più agile perché fornisce un Framework proattivo per prevenire i problemi, anziché un Framework reattivo che si basa sull'alternativa costosa del ripristino di un sistema dopo che si è verificato un problema. I criteri di restrizione software sono stati introdotti con il rilascio di Microsoft Windows XP per aiutare a proteggere i sistemi da codice sconosciuto e potenzialmente pericoloso. I criteri di restrizione forniscono un meccanismo in cui solo il codice attendibile dispone di accesso illimitato ai privilegi di un utente. Il codice sconosciuto, che può contenere virus o codice che è in conflitto con i programmi attualmente installati, può essere eseguito solo in un ambiente vincolato (spesso denominato sandbox) in cui non è consentito l'accesso ai privilegi utente sensibili alla sicurezza.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Uso dei criteri di restrizione software in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3620aba8cce2859d76ba07c2fa9655dd9036bdbb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483405"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Uso dei criteri di restrizione software in COM+

Il corretto uso dei criteri di restrizione software può rendere l'azienda più agile perché fornisce un Framework proattivo per prevenire i problemi, anziché un Framework reattivo che si basa sull'alternativa costosa del ripristino di un sistema dopo che si è verificato un problema. I criteri di restrizione software sono stati introdotti con il rilascio di Microsoft Windows XP per aiutare a proteggere i sistemi da codice sconosciuto e potenzialmente pericoloso. I criteri di restrizione forniscono un meccanismo in cui solo il codice attendibile dispone di accesso illimitato ai privilegi di un utente. Il codice sconosciuto, che può contenere virus o codice che è in conflitto con i programmi attualmente installati, può essere eseguito solo in un ambiente vincolato (spesso denominato *sandbox*) in cui non è consentito l'accesso ai privilegi utente sensibili alla sicurezza.

I criteri di restrizione software dipendono dall'assegnazione dei livelli di attendibilità al codice che può essere eseguito in un sistema. Attualmente, esistono due livelli di attendibilità: senza restrizioni e non consentiti. Al codice con un livello di attendibilità illimitato viene concesso l'accesso illimitato ai privilegi dell'utente, pertanto questo livello di attendibilità deve essere applicato solo a codice completamente attendibile. Il codice con un livello di attendibilità non consentito non è consentito ad accedere a privilegi utente sensibili alla sicurezza e può essere eseguito solo in una sandbox che consente di impedire al codice senza restrizioni di caricare il codice non consentito nello spazio degli indirizzi.

La configurazione dei criteri di restrizione software per un sistema viene eseguita tramite lo strumento di amministrazione Criteri di sicurezza locali, mentre la configurazione dei criteri di restrizione delle singole applicazioni COM+ viene eseguita a livello di codice o tramite lo strumento di amministrazione Servizi componenti. Se il livello di attendibilità dei criteri di restrizione non è specificato per un'applicazione COM+, le impostazioni a livello verranno utilizzate per determinare il livello di attendibilità dell'applicazione. È necessario coordinare attentamente le impostazioni dei criteri di restrizione COM+ con le impostazioni di a livello perché un'applicazione COM+ con un livello di attendibilità senza restrizioni può caricare solo i componenti con un livello di attendibilità senza restrizioni; un'applicazione COM+ non consentita può caricare componenti con qualsiasi livello di attendibilità, ma non può accedere a tutti i privilegi dell'utente.

Oltre ai livelli di attendibilità dei criteri di restrizione software delle singole applicazioni COM+, altre due proprietà determinano il modo in cui i criteri di restrizione vengono utilizzati per tutte le applicazioni COM+. Se [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) è abilitato, i tentativi di connessione agli oggetti in esecuzione verranno controllati per i livelli di attendibilità appropriati. L'oggetto in esecuzione non può avere un livello di attendibilità meno rigoroso rispetto all'oggetto client. L'oggetto in esecuzione, ad esempio, non può avere un livello di attendibilità non consentito se l'oggetto client ha un livello di attendibilità senza restrizioni.

La seconda proprietà determina il modo in cui il criterio di restrizione software gestisce le connessioni Activate-As-Activator. Se [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) è abilitato, il livello di attendibilità configurato per l'oggetto server viene confrontato con il livello di attendibilità dell'oggetto client e il livello di attendibilità più rigoroso verrà utilizzato per eseguire l'oggetto server. Se SRPActivateAsActivatorChecks non è abilitato, l'oggetto server verrà eseguito con il livello di attendibilità dell'oggetto client indipendentemente dal livello di attendibilità con cui è stato configurato. Per impostazione predefinita, sono abilitati sia SRPRunningObjectChecks che SRPActivateAsActivatorChecks.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Configurazione dei criteri di restrizione software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Sicurezza delle applicazioni di libreria](library-application-security.md)
</dt> <dt>

[Sicurezza delle applicazioni a più livelli](multi-tier-application-security.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> </dl>

 

 
