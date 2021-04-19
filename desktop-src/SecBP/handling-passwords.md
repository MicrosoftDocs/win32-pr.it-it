---
description: Attualmente, le credenziali del nome utente e della password sono le credenziali più comuni usate per l'autenticazione.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Gestione delle password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3a5ab2bc034500159adb25dab02b47eb43bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317740"
---
# <a name="handling-passwords"></a>Gestione delle password

Attualmente, le credenziali del nome utente e della password sono le credenziali più comuni usate per l'autenticazione. Sebbene altri tipi di credenziali, ad esempio i certificati e la biometria, stiano iniziando a trovare il mondo dei sistemi e delle reti, spesso vengono sottoposti a backup tramite password. Inoltre, anche in caso di utilizzo dei certificati, le chiavi di crittografia devono essere protette. Quindi, i nomi utente e le password continueranno a essere usati per le credenziali nel futuro prevedibile.

Dato che le password e le chiavi di crittografia rientrano tra qualche minuto, è importante che i sistemi software le usino in modo sicuro. Se una rete o un sistema di computer deve rimanere protetto, le password devono essere protette da intrusi. In primo luogo potrebbe sembrare semplice. Tuttavia, dopo che la rete è stata compromessa, il sistema dopo la rete è stato compromesso perché un utente malintenzionato è stato in grado di sniffare le password degli utenti. I problemi variano dagli utenti che condividono le proprie password con un utente, al software che può essere penetrato da un utente malintenzionato.

È Impossibile archiviare le informazioni segrete nel software in modo completamente protetto. Poiché l'archiviazione delle password e delle chiavi di crittografia in un sistema software non può mai essere completamente sicura, è consigliabile non archiviarle in un sistema software.

Tuttavia, quando le password devono essere archiviate in un sistema software, che è in genere il caso, è possibile adottare alcune precauzioni. La precauzione principale consiste nel rendere il più difficile possibile l'individuazione di una password da parte di un intruso. Proprio come il blocco delle porte domestiche, se qualcuno è deciso di interrompere l'operazione, è quasi impossibile impedirne l'esecuzione. Tuttavia, si spera che il livello di difficoltà sia stato sufficientemente elevato da comportare una preda più semplice.

Esistono diversi modi per fare in modo che un utente malintenzionato riesca a individuare le password più difficile. Tuttavia, la portata di ciò che si può effettivamente eseguire è in genere un compromesso con ciò che gli utenti della rete o del sistema sono disposti a vivere. Ad esempio, nel caso in cui non venga usato "Single Sign-on" e all'utente viene richiesta una password ogni volta che viene avviata un'applicazione. Nella maggior parte dei casi, ciò creerebbe un carico significativo per gli utenti, che probabilmente si lamentavano. Non solo, ma la mancanza di un Single Sign-on non è efficiente e potrebbe compromettere la produttività degli utenti. Quindi, in pratica, una password non viene in genere raccolta da un utente tranne al momento dell'accesso.

Dato che le password devono essere in genere archiviate nel sistema software, è importante assicurarsi che le password vengano mantenute nel modo più sicuro possibile e che la convenienza per gli utenti venga mantenuta. Per altre informazioni, vedere i seguenti argomenti:

-   [Valutazione delle minacce per la password](password-threat-assessment.md)
-   [Tecniche di mitigazione delle minacce](threat-mitigation-techniques.md)

> [!Note]  
> Al termine dell'utilizzo delle password nelle applicazioni, deselezionare le informazioni riservate dalla memoria chiamando la funzione [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .

 

 

 
