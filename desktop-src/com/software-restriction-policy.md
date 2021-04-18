---
title: Criteri di restrizione software
description: Le impostazioni dei criteri di restrizione software (SRP) sono state introdotte con il rilascio di Windows XP per proteggere i sistemi da codice sconosciuto ed eventualmente pericoloso.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97bf42cd949127e9012580ec16379cf36a95353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298001"
---
# <a name="software-restriction-policy"></a>Criteri di restrizione software

Le impostazioni dei criteri di restrizione software (SRP) sono state introdotte con il rilascio di Windows XP per proteggere i sistemi da codice sconosciuto ed eventualmente pericoloso. Il SRP fornisce un meccanismo in cui solo il codice attendibile dispone di accesso illimitato ai privilegi di un utente. Il codice sconosciuto, che può contenere virus o codice che è in conflitto con i programmi attualmente installati, può essere eseguito solo in un ambiente vincolato (spesso denominato *sandbox*) in cui non è consentito l'accesso ai privilegi utente sensibili alla sicurezza. L'uso corretto del sistema SRP può rendere l'azienda più agile perché fornisce un Framework proattivo per prevenire i problemi, anziché un Framework reattivo che si basa sull'alternativa costosa del ripristino di un sistema dopo che si è verificato un problema.

Il SRP dipende dall'assegnazione dei livelli di attendibilità al codice che può essere eseguito in un sistema. Attualmente, esistono due livelli di attendibilità: senza restrizioni e non consentiti. Al codice con un livello di attendibilità illimitato viene concesso l'accesso illimitato ai privilegi dell'utente, pertanto questo livello di attendibilità deve essere applicato solo a codice completamente attendibile. Il codice con un livello di attendibilità non consentito non è consentito ad accedere a privilegi utente sensibili alla sicurezza e può essere eseguito solo in una sandbox, in modo che il codice senza restrizioni non possa caricare il codice non consentito nello spazio degli indirizzi.

La configurazione di criteri di RESTRIzione delle singole applicazioni COM viene eseguita tramite il valore [SRPTrustLevel](srptrustlevel.md) nella chiave [AppID](appid-key.md) dell'applicazione nel registro di sistema. Se per un'applicazione COM non viene specificato il livello di attendibilità SRP, viene utilizzato il valore predefinito non consentito. Un'applicazione COM con un livello di attendibilità senza restrizioni ha accesso illimitato ai privilegi dell'utente, ma può caricare solo i componenti con un livello di attendibilità illimitato, mentre un'applicazione COM non consentita può caricare i componenti con qualsiasi livello di attendibilità, ma non può accedere ai privilegi utente sensibili alla sicurezza.

Oltre ai livelli di attendibilità del rollup delle singole applicazioni COM, altre due proprietà SRP determinano il modo in cui il SRP viene usato per tutte le applicazioni COM. Se [SRPRunningObjectChecks](srprunningobjectchecks.md) è abilitato, i tentativi di connessione agli oggetti in esecuzione verranno controllati per verificare la presenza di livelli di attendibilità SRP appropriati. L'oggetto in esecuzione non può avere un livello di attendibilità del SRP meno rigoroso rispetto all'oggetto client. L'oggetto in esecuzione, ad esempio, non può avere un livello di attendibilità non consentito se l'oggetto client ha un livello di attendibilità senza restrizioni.

La seconda proprietà determina il modo in cui il SRP gestisce le connessioni Activate-As-Activator. Se [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) è abilitato, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità più rigoroso verrà utilizzato per eseguire l'oggetto server. Se **SRPActivateAsActivatorChecks** non è abilitato, l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è stato configurato. Per impostazione predefinita, sono abilitati sia **SRPRunningObjectChecks** che **SRPActivateAsActivatorChecks** .

 

 




