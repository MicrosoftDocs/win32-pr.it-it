---
title: Utenti e connessioni di rete
description: BITS trasferisce i file solo quando il proprietario del processo è connesso e viene stabilita una connessione di rete.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- connessioni di rete BITS
- trasferimento del processo BITS, proprietà
- trasferire il processo BITS, proprietà, account utente
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 54e346590cac90b8d896a9a45c86aee5ae241d7d299bb055cf9ff55db88b8668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679883"
---
# <a name="users-and-network-connections"></a>Utenti e connessioni di rete

BITS trasferisce i file solo quando il proprietario del processo è connesso e viene stabilita una connessione di rete. BITS elabora il processo di trasferimento usando il contesto di sicurezza del proprietario del processo. L'utente che ha creato il processo è considerato il proprietario del processo. Tuttavia, un utente con privilegi di amministratore può [**assumere la proprietà**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) del processo di un altro utente.

BITS sospende un processo quando il proprietario si disconnette o se la connessione di rete viene persa (BITS non forza una connessione di rete). BITS riprende il processo quando il proprietario esegue nuovamente l'accesso e viene stabilita una connessione di rete. Dopo aver stabilito la connessione di rete, è possibile che si verifichi un breve ritardo prima che BITS inizi a trasferire i dati.

Se la connessione di rete viene persa, tutti i processi il cui stato è [**BG \_ JOB STATE \_ \_ QUEUED**](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **BG JOB STATE \_ \_ \_ TRANSFERRING** vengono spostati nello stato **BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR** con un codice di errore [BG E NETWORK \_ \_ \_ DISCONNECTED.](bits-return-values.md) Quando viene stabilita una connessione di rete, tutti i processi in uno stato **BG \_ JOB STATE TRANSIENT \_ \_ \_ ERROR,** che può includere qualsiasi codice di errore, vengono spostati nello stato **BG JOB STATE \_ \_ \_ QUEUED.**

Perché BITS rilevi che un utente è connesso, l'utente deve usare una delle opzioni di accesso interattive seguenti:

-   Accedere tramite il schermata iniziale.
-   Accedere a un client [del servizio terminal.](../termserv/terminal-services-portal.md)
-   Usare [il cambio rapido dell'utente.](../shell/fast-user-switching.md)
-   A partire da Windows 10 versione 1607, accedere da un altro dispositivo usando PowerShell remoto. Per informazioni dettagliate, vedere Per gestire [le sessioni remote di PowerShell.](using-windows-powershell-to-create-bits-transfer-jobs.md)

L'esecuzione di un'applicazione come altro utente (tramite il **comando RunAs)** non è un accesso interattivo. BITS non eseguirà processi associati all'utente specificato.

Gli account di sistema LocalSystem, LocalService e NetworkService sono sempre connessi. Pertanto, i processi inviati da un servizio che usano questi account vengono sempre eseguiti. Per informazioni e limitazioni sull'uso degli account del servizio, vedere [Account del servizio e BITS.](service-accounts-and-bits.md)

I proprietari dei processi possono fornire un token helper da usare in situazioni in cui sono necessari più token per completare un trasferimento, ad esempio per l'autenticazione con un host remoto. Per [informazioni dettagliate, vedere Token helper per i processi di trasferimento BITS.](helper-tokens-for-bits-transfer-jobs.md) Nelle versioni precedenti di Windows, il proprietario del processo doveva effettivamente disporre dei privilegi di amministratore per avviare un processo che usava un token helper. In Windows 10 versione 1607, è ora possibile che il proprietario di un processo BITS imposta i token helper senza essere un amministratore, purché il token helper non abbia funzionalità di amministratore. Si riduce così la vulnerabilità correlata agli strumenti di download o aggiornamento in background, che possono essere eseguiti con l'account NetworkService con minori privilegi anziché con un account con privilegi di amministratore.

Gli utenti con un [token con restrizioni](../secauthz/restricted-tokens.md) (un token che contiene SID limitati) non possono creare o modificare processi.
 

 