---
description: Sviluppare app desktop più sicure usando le API e i servizi di Windows.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Sicurezza e Identity
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5b8fccc4039794fe76dabb34d88fa6d475a3b22a
ms.sourcegitcommit: 7f0c005e444c17f69b5ead403c43814f3bbe047a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/10/2020
ms.locfileid: "104399989"
---
# <a name="security-and-identity"></a>Sicurezza e Identity

Sviluppare app desktop più sicure usando le API e i servizi di Windows. Queste API forniscono:

- Authentication
- Autorizzazione
- Crittografia
- Servizi di directory, identità e accesso
- Controlli padre
- Rights Management

In questa sezione vengono inoltre fornite procedure consigliate e altri articoli sulla sicurezza.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
| ----- | ----------- |
| [Interfaccia di analisi antimalware](./amsi/antimalware-scan-interface-portal.md) | L'interfaccia di analisi antimalware (AMSI) è uno standard di interfaccia generica che consente alle applicazioni e ai servizi di integrarsi con qualsiasi prodotto antimalware presente in un computer. Offre protezione da malware avanzata per gli utenti e i relativi dati, applicazioni e carichi di lavoro. |
| [autenticazione](./secauthn/authentication-portal.md) | L'autenticazione è il processo mediante il quale il sistema convalida le informazioni di accesso di un utente. Il nome e la password di un utente vengono confrontati con un elenco autorizzato e se il sistema rileva una corrispondenza, viene concesso l'accesso all'extent specificato nell'elenco di autorizzazioni per tale utente. |
| [Autorizzazione](./secauthz/authorization-portal.md) | L'autorizzazione è il diritto concesso a un utente per l'utilizzo del sistema e dei dati archiviati. L'autorizzazione viene in genere configurata da un amministratore di sistema e verificata dal computer in base a una forma di identificazione utente, ad esempio un numero di codice o una password. |
| [Procedure consigliate per le API di sicurezza](./secbp/best-practices-for-the-security-apis.md) | Fornisce le procedure consigliate per lo sviluppo di applicazioni più sicure. |
| [API di registrazione certificato](./seccertenroll/certenroll-portal.md) | L'API di registrazione certificati può essere usata per creare un'applicazione client per richiedere un certificato e installare una risposta del certificato. |
| [Guard flusso di controllo (CFG)](./secbp/control-flow-guard.md) | Il controllo del flusso di controllo (CFG) è una funzionalità di sicurezza della piattaforma altamente ottimizzata che è stata creata per combattere le vulnerabilità di danneggiamento della memoria. |
| [Crittografia](./seccrypto/cryptography-portal.md) | La crittografia prevede l'uso di codici per la conversione dei dati in modo che solo un destinatario specifico possa leggerlo, usando una chiave. CryptoAPI consente agli utenti di creare e scambiare documenti e altri dati in un ambiente protetto, soprattutto su supporti non protetti, ad esempio Internet. |
| [API di crittografia: prossima generazione](./seccng/cng-portal.md) | Cryptography API: Next Generation (CNG) consente agli utenti di creare e scambiare documenti e altri dati in un ambiente protetto, soprattutto su supporti non protetti, ad esempio Internet. |
| [Estendibilità degli sviluppatori per il controllo dinamico degli accessi](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | Lo scenario controllo dinamico degli accessi (DAC), fornito in Windows Server 2012, dispone di un'ampia gamma di punti di estendibilità per sviluppatori che aggiungono il potenziale di personalizzazione per lo sviluppo di applicazioni. |
| [Servizi di directory, identità e accesso](./srvnodes/directory--identity--and-access-services.md) | Gli amministratori di rete possono utilizzare i servizi directory per automatizzare le attività amministrative comuni, ad esempio l'aggiunta di utenti e gruppi, la gestione delle stampanti e l'impostazione delle autorizzazioni per le risorse di rete.<br/> I fornitori di software indipendenti e gli sviluppatori di utenti finali possono usare i servizi directory per abilitare la directory di prodotti e applicazioni. I servizi possono essere pubblicati in una directory, i client possono utilizzare la directory per trovare i servizi ed entrambi possono utilizzare la directory per individuare e modificare altri oggetti.<br/> Forefront Identity Manager (FIM) fornisce una soluzione integrata e completa per la gestione dell'intero ciclo di vita delle identità degli utenti e delle credenziali associate.<br/> Identity Lifecycle Manager (ILM) consente alle organizzazioni IT di ridurre i costi di gestione del ciclo di vita delle identità e dell'accesso fornendo una visualizzazione unica dell'identità di un utente nell'azienda eterogenea e tramite l'automazione delle attività comuni.<br/> Active Directory Servizio federativo (AD FS) consente la gestione delle identità e degli accessi federativi condividendo in modo sicuro l'identità digitale e i diritti sui diritti per i confini aziendali e di sicurezza. |
| [Extensible Authentication Protocol](./eap/extensible-authentication-protocol-reference.md) | Extensible Authentication Protocol (EAP) è uno standard supportato da diversi componenti di sistema. EAP è essenziale per la protezione della sicurezza di reti wireless (802.1 X) e LAN cablate, di connessione remota e di reti private virtuali (VPN). |
| [Host del protocollo di autenticazione estendibile](./eaphost/about-eap-host.md) | EAPHost è un componente di rete di Microsoft Windows che fornisce un'infrastruttura EAP (Extensible Authentication Protocol) per l'autenticazione di implementazioni del protocollo "supplicant", ad esempio 802.1 X e Point-to-Point (PPP). |
| [API di gestione delle password MS-CHAP](/previous-versions/windows/desktop/mschap/portal) | È possibile usare l'API di gestione delle password MS-CHAP per creare applicazioni per modificare le password degli utenti in rete nelle workstation remote. |
| [Protezione accesso alla rete](./nap/network-access-protection-start-page.md) | Protezione accesso alla rete (NAP) è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private. La piattaforma NAP fornisce un modo integrato per valutare lo stato di integrità del sistema di un client di rete che tenta di connettersi a una rete o di comunicare in una rete e di limitare l'accesso del client di rete fino a quando non sono stati soddisfatti i requisiti dei criteri di integrità. |
| [Server dei criteri di rete](./nps/portal.md) | Server dei criteri di rete è l'implementazione Microsoft di un server e un proxy RADIUS (Remote Authentication Dial-in User Service). È il successore del servizio di autenticazione Internet (IAS). |
| [Controlli padre](./parcon/parental-controls-portal.md) | La tecnologia di controllo parentale di Windows è concepita per aiutare i genitori assidui o tutori a garantire l'accesso ai materiali appropriati in base all'età o al livello di maturità per i soggetti interessati. Fornisce un'infrastruttura estendibile oltre alle funzionalità predefinite. |
| [Rights Management](./srvnodes/rights-management.md) | Sono ora disponibili tre generazioni di Rights Management SDK, oltre a una roadmap all-up per gli esempi di codice RMS e gli strumenti di sviluppo forniti da Microsoft in tutti i sistemi operativi supportati. Android, iOS/OS X, Windows Phone e desktop di Windows. |
| [Security Development Lifecycle (SDL)-linee guida per il processo](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft Security Development Lifecycle (SDL) è un processo di controllo della sicurezza software leader del settore. Un'iniziativa a livello di Microsoft e un criterio obbligatorio a partire da 2004, il processo SDL ha svolto un ruolo fondamentale nell'incorporare la sicurezza e la privacy nel software e nelle impostazioni cultura Microsoft. Combinando un approccio olistico e pratico, il processo SDL introduce la sicurezza e la privacy in anticipo e in tutte le fasi del processo di sviluppo. |
| [Gestione della sicurezza](./secmgmt/management-portal.md) | Le tecnologie di gestione della sicurezza possono essere utilizzate per gestire i criteri dell'autorità di sicurezza locale (LSA) e i criteri di filtro delle password, eseguire una query sulla capacità dei programmi da origini esterne e gli allegati dei servizi che estendono la funzionalità dello strumento di configurazione della sicurezza. |
| [Provider WMI per la sicurezza](./secprov/secprov-portal.md) | I provider WMI per la sicurezza consentono agli amministratori e ai programmatori di configurare Crittografia unità BitLocker (BDE) e il Trusted Platform Module (TPM) utilizzando Strumentazione gestione Windows (WMI). |
| [Glossario sulla sicurezza](./secgloss/security-glossary.md) | Fornisce un glossario dei termini di sicurezza. |
| [Servizi di base TPM](./tbs/tpm-base-services-portal.md) | La funzionalità dei servizi di base Trusted Platform Module (TPM) centralizza l'accesso TPM tra le applicazioni. La funzionalità TBS usa le priorità specificate chiamando le applicazioni per pianificare in modo cooperativo l'accesso a TPM. |
| [API Windows Biometric Framework](./secbiomet/biometric-service-api-portal.md) | È possibile usare l'API Windows Biometric Framework per creare applicazioni client che acquisiscono, salvano e confrontano in modo sicuro le informazioni biometriche dell'utente finale. |
| [Articoli tecnici sulla sicurezza](https://msdn.microsoft.com/library/hh322936.aspx) | Articoli su sicurezza e crittografia. |



 

 

 