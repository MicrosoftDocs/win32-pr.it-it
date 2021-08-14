---
description: Sviluppare app desktop più sicure usando Windows API e servizi.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Sicurezza e Identity
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ff19c113340af314177b821bfd8294036d752d90218a5255eb6a429e9b6312ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226336"
---
# <a name="security-and-identity"></a>Sicurezza e Identity

Sviluppare app desktop più sicure usando Windows API e servizi. Queste API forniscono:

- Autenticazione
- Autorizzazione
- Crittografia
- Servizi di directory, identità e accesso
- Controllo genitori
- Rights Management

Questa sezione fornisce anche procedure consigliate e altri articoli sulla sicurezza.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
| ----- | ----------- |
| [Interfaccia di analisi antimalware](./amsi/antimalware-scan-interface-portal.md) | Antimalware Scan Interface (AMSI) è uno standard di interfaccia generica che consente l'integrazione di applicazioni e servizi con qualsiasi prodotto antimalware presente in un computer. Offre una protezione avanzata da malware per gli utenti e i relativi dati, applicazioni e carichi di lavoro. |
| [autenticazione](./secauthn/authentication-portal.md) | L'autenticazione è il processo tramite il quale il sistema convalida le informazioni di accesso di un utente. Il nome e la password di un utente vengono confrontati con un elenco autorizzato e se il sistema rileva una corrispondenza, l'accesso viene concesso nella misura specificata nell'elenco di autorizzazioni per tale utente. |
| [Autorizzazione](./secauthz/authorization-portal.md) | L'autorizzazione è il diritto concesso a un utente di usare il sistema e i dati archiviati in esso. L'autorizzazione viene in genere impostata da un amministratore di sistema e verificata dal computer in base a una forma di identificazione utente, ad esempio un numero di codice o una password. |
| [Procedure consigliate per le API di sicurezza](./secbp/best-practices-for-the-security-apis.md) | Fornisce le procedure consigliate per lo sviluppo di applicazioni più sicure. |
| [API di registrazione certificato](./seccertenroll/certenroll-portal.md) | L'API di registrazione certificati può essere usata per creare un'applicazione client per richiedere un certificato e installare una risposta del certificato. |
| [Control Flow Guard (CFG)](./secbp/control-flow-guard.md) | Control Flow Guard (CFG) è una funzionalità di sicurezza della piattaforma altamente ottimizzata creata per contrastare le vulnerabilità di danneggiamento della memoria. |
| [Crittografia](./seccrypto/cryptography-portal.md) | La crittografia è l'uso di codici per convertire i dati in modo che solo un destinatario specifico possa leggerli usando una chiave. CryptoAPI consente agli utenti di creare e scambiare documenti e altri dati in un ambiente sicuro, in particolare su supporti non sicuri come Internet. |
| [API di crittografia: nuova generazione](./seccng/cng-portal.md) | API di crittografia: CNG (Next Generation) consente agli utenti di creare e scambiare documenti e altri dati in un ambiente sicuro, in particolare su supporti non sicuri come Internet. |
| [Estendibilità dinamica degli sviluppatori di Controllo di accesso dinamico](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | Lo scenario dynamic access control (DAC), fornito in Windows Server 2012, offre una vasta gamma di punti di estendibilità per gli sviluppatori che aggiungono potenzialità di personalizzazione per lo sviluppo di applicazioni. |
| [Directory, identità e Access Services](./srvnodes/directory--identity--and-access-services.md) | Gli amministratori di rete possono usare i servizi directory per automatizzare le attività amministrative comuni, ad esempio l'aggiunta di utenti e gruppi, la gestione delle stampanti e l'impostazione delle autorizzazioni per le risorse di rete.<br/> I fornitori di software indipendenti e gli sviluppatori degli utenti finali possono usare i servizi directory per abilitare i prodotti e le applicazioni per la directory. I servizi possono pubblicarsi in una directory, i client possono usare la directory per trovare i servizi ed entrambi possono usare la directory per trovare e modificare altri oggetti.<br/> Forefront Identity Manager (FIM) offre una soluzione integrata e completa per la gestione dell'intero ciclo di vita delle identità utente e delle credenziali associate.<br/> Identity Lifecycle Manager (ILM) consente alle organizzazioni IT di ridurre i costi di gestione del ciclo di vita delle identità e degli accessi fornendo un'unica visualizzazione dell'identità di un utente nell'intera azienda eterogenea e tramite l'automazione delle attività comuni.<br/> Active Directory Servizio federativo (AD FS) consente la gestione delle identità e degli accessi federati condividendo in modo sicuro i diritti di identità e diritti digitali tra i limiti di sicurezza e aziendali. |
| [Extensible Authentication Protocol](./eap/extensible-authentication-protocol-reference.md) | Extensible Authentication Protocol (EAP) è uno standard supportato da diversi componenti di sistema. EAP è fondamentale per proteggere la sicurezza delle reti LAN cablate, remote e private virtuali (802.1X) e wireless (802.1X). |
| [Host del protocollo di autenticazione estendibile](./eaphost/about-eap-host.md) | EAPHost è un componente di rete di Microsoft Windows che fornisce un'infrastruttura EAP (Extensible Authentication Protocol) per l'autenticazione di implementazioni del protocollo "supplicant", ad esempio 802.1X e PPP (Point-to-Point). |
| [Password MS-CHAP API Gestione](/previous-versions/windows/desktop/mschap/portal) | È possibile usare la password MS-CHAP API Gestione creare applicazioni per modificare le password degli utenti in rete nelle workstation remote. |
| [Protezione accesso alla rete](./nap/network-access-protection-start-page.md) | Protezione accesso alla rete è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private. La piattaforma Protezione accesso alla rete offre un modo integrato per valutare lo stato di integrità del sistema di un client di rete che sta tentando di connettersi o comunicare in una rete e di limitare l'accesso del client di rete fino a quando non vengono soddisfatti i requisiti dei criteri di integrità. |
| [Server dei criteri di rete](./nps/portal.md) | Server dei criteri di rete è l'implementazione Microsoft di un server RADIUS (Remote Authentication Dial-in User Service) e di un proxy. È il successore del servizio di autenticazione Internet (IAS). |
| [Controllo genitori](./parcon/parental-controls-portal.md) | La tecnologia Controllo genitori in Windows è progettata per aiutare genitori o tutori diligenti a garantire l'accesso ai materiali appropriati in base all'età o al livello di maturità per coloro che sono sotto la loro tutela. Fornisce un'infrastruttura estendibile oltre alle funzionalità incorporate. |
| [Rights Management](./srvnodes/rights-management.md) | Sono ora disponibili tre generazioni Rights Management SDK, oltre a una roadmap a livello generale per gli esempi di codice e gli strumenti di sviluppo RMS forniti da Microsoft in tutti i sistemi operativi supportati. Android, iOS/OS X, Windows Phone e Windows Desktop. |
| [Security Development Lifecycle (SDL) - Linee guida per i processi](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft Security Development Lifecycle (SDL) è un processo di software security assurance leader del settore. Un'iniziativa a livello di Microsoft e un criterio obbligatorio dal 2004, SDL ha svolto un ruolo fondamentale nell'incorporamento della sicurezza e della privacy nel software e nella cultura Microsoft. Combinando un approccio olistico e pratico, SDL introduce la sicurezza e la privacy in anticipo e in tutte le fasi del processo di sviluppo. |
| [Gestione della sicurezza](./secmgmt/management-portal.md) | Le tecnologie di gestione della sicurezza possono essere usate per gestire i criteri dell'autorità di sicurezza locale (LSA) e i criteri di filtro delle password, eseguire query sulla capacità dei programmi provenienti da origini esterne e per gli allegati del servizio che estendono le funzionalità dello strumento Di configurazione della sicurezza. |
| [Provider WMI di sicurezza](./secprov/secprov-portal.md) | I provider WMI di sicurezza consentono ad amministratori e programmatori di configurare Crittografia unità BitLocker (BDE) e Trusted Platform Module (TPM) usando strumentazione di gestione Windows (WMI). |
| [Glossario della sicurezza](./secgloss/security-glossary.md) | Fornisce un glossario delle condizioni di sicurezza. |
| [Servizi di base TPM](./tbs/tpm-base-services-portal.md) | La Trusted Platform Module (TPM) Base Services (TBS) centralizza l'accesso TPM tra le applicazioni. La funzionalità TBS usa le priorità specificate chiamando le applicazioni per pianificare in modo cooperativo l'accesso TPM. |
| [Windows Biometric Framework API](./secbiomet/biometric-service-api-portal.md) | È possibile usare l'API Windows Biometric Framework per creare applicazioni client che acquisiscono, salvano e confrontano in modo sicuro le informazioni biometriche dell'utente finale. |
| [Articoli tecnici sulla sicurezza](https://msdn.microsoft.com/library/hh322936.aspx) | Articoli su sicurezza e crittografia. |



 

 

 