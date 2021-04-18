---
Descrizione: per accedere ai dati dei contatori in un computer remoto: nel computer remoto deve essere abilitato il servizio Registro di sistema remoto. È necessario selezionare l'eccezione per la condivisione di file e stampanti in Windows Firewall impostazioni. prima di Windows Vista, il servizio Registro di sistema remoto è abilitato per impostazione predefinita.
ms. AssetID: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title: accesso ai dati del contatore remoto ms. Topic: articolo ms. Date: 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Accesso ai dati del contatore remoto

Per accedere ai dati dei contatori in un computer remoto:

- Nel computer remoto deve essere abilitato il servizio Registro di sistema remoto.
- È necessario selezionare l'eccezione di **condivisione file e stampanti** in **Windows firewall impostazioni**.

**Prima di Windows Vista:** Il servizio Registro di sistema remoto è abilitato per impostazione predefinita.

> [!NOTE]
> Gli strumenti e le API dei contatori delle prestazioni di Windows includono supporto limitato per l'accesso ai contatori delle prestazioni da altri computer tramite RPC (per i provider v2) e registro di sistema remoto (per i provider v1). Questo supporto è spesso difficile da usare in termini di controlli di autenticazione (gli strumenti e le API possono autenticarsi solo come utente corrente), oltre che in termini di configurazione del sistema (gli endpoint e i servizi necessari sono disabilitati per impostazione predefinita nella maggior parte dei sistemi). In molti casi, è preferibile accedere ai contatori delle prestazioni dei sistemi remoti tramite [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) anziché tramite il supporto predefinito di accesso remoto.
