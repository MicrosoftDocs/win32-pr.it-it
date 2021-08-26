---
description: Attualmente, le credenziali di nome utente e password sono le credenziali più comuni usate per l'autenticazione.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Gestione delle password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99aaf133d23390a6f4efce97940c5116fddf91b45776dfd6847b2712b15b74ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035471"
---
# <a name="handling-passwords"></a>Gestione delle password

Attualmente, le credenziali di nome utente e password sono le credenziali più comuni usate per l'autenticazione. Anche se altri tipi di credenziali, ad esempio certificati e biometria, iniziano a essere individuati nel mondo dei sistemi e delle reti, spesso sono sottoposti a backup da password. E, anche quando vengono usati i certificati, le relative chiavi di crittografia devono essere protette. Pertanto, i nomi utente e le password continueranno a essere usati per le credenziali nel prossimo futuro.

Dato che le password e le chiavi di crittografia saranno disponibili per un periodo di tempo, è importante che i sistemi software le usino in modo sicuro. Se una rete o un sistema di computer deve rimanere protetto, le password devono essere protette da intrusi. Questo potrebbe sembrare all'inizio semplice. Tuttavia, il sistema dopo il sistema e la rete dopo la rete sono stati compromessi perché un utente malintenzionato è stato in grado di eseguire l'analisi delle password degli utenti. I problemi vanno dagli utenti che condividono le password con un utente, al software che può essere danneggiato da un utente malintenzionato.

Non è possibile archiviare le informazioni segrete nel software in modo completamente sicuro. Poiché l'archiviazione di password e chiavi di crittografia in un sistema software non può mai essere completamente sicura, è consigliabile non archiviare le password in un sistema software.

Tuttavia, quando le password devono essere archiviate in un sistema software, come avviene in genere, è possibile adottare alcune precauzioni. La precauzione principale è rendere il più difficile possibile l'individuazione di una password da parte di un intruso. Proprio come bloccare le porte di una casa, se qualcuno è determinato a infrangersi, è quasi impossibile impedirgli di farlo. Ma si dovrebbe avere aumentato il livello di difficoltà in modo tale che l'intruso possa trovare più facilmente le predisporre.

Esistono diversi modi per rendere più difficile l'individuazione delle password da parte di un utente malintenzionato. Tuttavia, l'entità di ciò che si può effettivamente fare è in genere un compromesso con ciò che gli utenti della rete o del sistema sono disposti a convivere. Si consideri ad esempio il caso in cui non viene usato "Single Sign-On" e all'utente viene richiesta una password ogni volta che viene avviata un'applicazione. Nella maggior parte dei casi, ciò creerebbe un carico significativo per gli utenti e probabilmente si lamenterebbe. Non solo, ma la mancanza di un accesso Single Sign-On è inefficiente e ridurrebbe la produttività degli utenti. Quindi, in pratica, una password in genere non viene raccolta da un utente se non al momento dell'accesso.

Dato che le password devono essere in genere archiviate nel sistema software, diventa importante assicurarsi che le password siano il più sicure possibile e che gli utenti siano più pratici. Per altre informazioni, vedere i seguenti argomenti:

-   [Valutazione delle minacce per le password](password-threat-assessment.md)
-   [Tecniche di mitigazione delle minacce](threat-mitigation-techniques.md)

> [!Note]  
> Dopo aver terminato di usare le password nelle applicazioni, cancellare le informazioni riservate dalla memoria chiamando la [**funzione SecureZeroMemory.**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85))

 

 

 
