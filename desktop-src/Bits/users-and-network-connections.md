---
title: Utenti e connessioni di rete
description: BITS trasferisce i file solo quando il proprietario del processo è connesso e viene stabilita una connessione di rete.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- BIT connessioni di rete
- trasferimento di bit del processo, proprietà
- trasferimento di bit del processo, proprietà, account utente
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7f841e3bf92004b62f3bbb576f71a45ac6b4a6bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118347"
---
# <a name="users-and-network-connections"></a>Utenti e connessioni di rete

BITS trasferisce i file solo quando il proprietario del processo è connesso e viene stabilita una connessione di rete. BITS elabora il processo di trasferimento usando il contesto di sicurezza del proprietario del processo. L'utente che ha creato il processo viene considerato il proprietario del processo. Tuttavia, un utente con privilegi di amministratore può [**assumere la proprietà**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) del processo di un altro utente.

BITS sospende un processo quando il proprietario si disconnette o se la connessione di rete va persa (BITS non forza una connessione di rete). BITS riprende il processo quando il proprietario esegue nuovamente l'accesso e viene stabilita una connessione di rete. Una volta stabilita la connessione di rete, è possibile che si verifichi un breve ritardo prima che BITS inizi il trasferimento dei dati.

Se la connessione di rete viene persa, tutti i processi il cui stato è [**BG \_ processo in \_ \_ coda**](/windows/desktop/api/Bits/ne-bits-bg_job_state) o il **\_ \_ \_ trasferimento dello stato del processo BG** vengono spostati nello stato di **\_ \_ \_ \_ errore temporaneo stato processo** BG con un codice di errore di [rete di BG \_ E \_ \_ disconnesso](bits-return-values.md) . Quando viene stabilita una connessione di rete, tutti i processi in uno stato di **\_ \_ \_ \_ errore temporaneo di stato del processo BG** , che può includere qualsiasi codice di errore, vengono spostati nello stato in **\_ \_ \_ coda del processo BG** .

Per bit per rilevare che un utente è connesso, l'utente deve usare una delle opzioni di accesso interattivo seguenti:

-   Accedere alla schermata iniziale.
-   Accedere a un client di [Servizi terminal](../termserv/terminal-services-portal.md) .
-   Utilizzare il [cambio rapido utente](../shell/fast-user-switching.md).
-   A partire da Windows 10, versione 1607, accedere da un altro dispositivo usando PowerShell remoto. Per informazioni dettagliate, vedere [per gestire le sessioni remote di PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md) .

L'esecuzione di un'applicazione come altro utente (tramite il comando **RunAs** ) non è un accesso interattivo. BITS non eseguirà i processi associati all'utente specificato.

Gli account di sistema LocalSystem, LocalService e NetworkService sono sempre connessi. di conseguenza, i processi inviati da un servizio usando questi account vengono sempre eseguiti. Per informazioni e limitazioni sull'utilizzo degli account del servizio, vedere [account del servizio e BITS](service-accounts-and-bits.md).

I proprietari dei processi possono fornire un token Helper da usare in situazioni in cui sono necessari più token per completare un trasferimento, ad esempio per l'autenticazione con un host remoto. Per informazioni dettagliate, vedere [token helper per i processi di trasferimento BITS](helper-tokens-for-bits-transfer-jobs.md) . Nelle versioni precedenti di Windows, il proprietario del processo doveva effettivamente disporre dei privilegi di amministratore per avviare un processo che utilizzava un token helper. In Windows 10, versione 1607, è ora possibile per un proprietario di un processo BITS impostare i token Helper senza essere un amministratore, purché il token Helper non disponga delle funzionalità di amministratore. Si riduce così la vulnerabilità correlata agli strumenti di download o aggiornamento in background, che possono essere eseguiti con l'account NetworkService con minori privilegi anziché con un account con privilegi di amministratore.

Gli utenti con un [token con restrizioni](../secauthz/restricted-tokens.md) , ovvero un token contenente i SID che li limitano, non possono creare o modificare i processi.
 

 