---
description: per accedere ai dati dei contatori in un computer remoto: nel computer remoto deve essere abilitato il servizio Registro di sistema remoto. L'eccezione Condivisione file e stampa deve essere selezionata in Windows Firewall Impostazioni. Prima di Windows Vista: il servizio Registro di sistema remoto è abilitato per impostazione predefinita.
ms.assetid: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title: Accessing Remote Counter Data ms.topic: article ms.date: 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Accesso ai dati dei contatori remoti

Per accedere ai dati dei contatori in un computer remoto:

- Nel computer remoto deve essere abilitato il servizio Registro di sistema remoto.
- **L'eccezione Condivisione file e** stampa deve essere selezionata in Windows Firewall **Impostazioni**.

**Prima di Windows Vista:** Il servizio Registro di sistema remoto è abilitato per impostazione predefinita.

> [!NOTE]
> Windows Gli strumenti e le API dei contatori delle prestazioni includono un supporto limitato per l'accesso ai contatori delle prestazioni da altri computer tramite RPC (per i provider V2) e Registro di sistema remoto (per i provider V1). Questo supporto è spesso difficile da usare in termini di controlli di autenticazione (gli strumenti e le API possono eseguire l'autenticazione solo come utente corrente) e in termini di configurazione del sistema (gli endpoint e i servizi necessari sono disabilitati per impostazione predefinita nella maggior parte dei sistemi). In molti casi, è meglio accedere ai contatori delle prestazioni dei sistemi remoti tramite [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) anziché tramite il supporto di accesso remoto incorporato.
