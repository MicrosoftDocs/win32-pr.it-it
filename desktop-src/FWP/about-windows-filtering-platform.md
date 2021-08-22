---
title: Informazioni Windows filtering platform
description: Windows Filtering Platform (WFP) è una piattaforma di elaborazione del traffico di rete progettata per sostituire le interfacce di filtro del traffico di rete Windows XP e Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a81f4f67c2f3281a6fa6b5d3220f9e2157643dfd7cf3bac34ea55743024946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069491"
---
# <a name="about-windows-filtering-platform"></a>Informazioni Windows filtering platform

Windows Filtering Platform (WFP) è una piattaforma di elaborazione del traffico di rete progettata per sostituire le interfacce di filtro del traffico di rete Windows XP e Windows Server 2003. WFP è costituito da un set di hook nello stack di rete e da un motore di filtro che coordina le interazioni dello stack di rete.

## <a name="the-wfp-components"></a>Componenti del WFP

### <a name="filter-engine"></a>Motore di filtro

Infrastruttura di filtro a più livelli principale, ospitata sia in modalità kernel che in modalità utente, che sostituisce i più moduli di filtro nel sottosistema di rete Windows XP e Windows Server 2003.

-   Filtra il traffico di rete a qualsiasi livello del sistema su tutti i campi dati che possono essere forniti da uno shim.
-   Implementa i filtri "Callout" richiamando i callout durante la classificazione.
-   Restituisce le azioni "Permit" o "Block" per lo shim che lo ha richiamato per l'imposizione.
-   Fornisce l'arbitraggio tra diverse origini dei criteri. Ad esempio, determina la priorità quando un'applicazione è configurata per proteggere qualsiasi traffico di rete correlato, ma il firewall locale è configurato per impedire il traffico protetto dall'applicazione.<br/>

### <a name="base-filtering-engine-bfe"></a>Base Filtering Engine (BFE)

Servizio che controlla il funzionamento della piattaforma Windows filtri. Esegue le attività seguenti.

-   Accetta filtri e altre impostazioni di configurazione per la piattaforma.
-   Segnala lo stato corrente del sistema, incluse le statistiche.
-   Applica il modello di sicurezza per accettare la configurazione nella piattaforma. Ad esempio, un amministratore locale può aggiungere filtri, ma altri utenti possono solo visualizzarli.<br/>
-   Modifica le impostazioni di configurazione in altri moduli del sistema. Ad esempio, i criteri di negoziazione IPsec passano ai moduli di keying IKE/AuthIP e i filtri passano al motore di filtro.<br/>

### <a name="shims"></a>Spessori

Componenti in modalità kernel che si trovano tra lo stack di rete e il motore di filtro. Gli s shims fanno la decisione di filtro classificando in base al motore di filtro. Di seguito è riportato un elenco di sms disponibili.

-   Shim application layer enforcement (ALE).
-   Shim del modulo Transport Layer.
-   Shim del modulo del livello di rete.
-   Internet Control Message Protocol shim di errore (ICMP).
-   Eliminare lo shim.
-   Shim di flusso.

### <a name="callouts"></a>Callout

Set di funzioni esposte da un driver e usate per filtri specializzati. Oltre alle azioni di base di "Permit" e "Block", i callout possono modificare e proteggere il traffico di rete in ingresso e in uscita. Per altre [informazioni sui callout, vedere](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) l'argomento Windows Filtering Platform Callout Drivers nella documentazione di Windows Driver Kit (WDK). Il WFP fornisce callout predefiniti che eseere le attività seguenti.<br/>

-   Eseguire l'elaborazione IPsec.
-   Modificare il comportamento del filtro con stato.
-   Eseguire il filtro in modalità stealth (eliminazione invisibile all'utente dei pacchetti non richiesti).
-   Controllare l'offload dei camini TCP.
-   Interagire con il Teredo servizio.

<br/> Il motore di filtro consente ai callout di terze parti di registrarsi in ogni livello in modalità kernel.<br/>

### <a name="application-programming-interface"></a>Interfaccia di programmazione delle applicazioni

Set di tipi di dati e funzioni disponibili per gli sviluppatori per compilare e gestire applicazioni di filtro di rete. Questi tipi di dati e funzioni sono raggruppati in più [set di API.](api-sets.md)

## <a name="wfp-features"></a>Funzionalità del WFP

-   Fornisce un'infrastruttura di filtro dei pacchetti in cui i fornitori di software indipendenti (ISV) possono collegare moduli di filtro specializzati.
-   Funziona sia con IPv4 che con IPv6.
-   Consente il filtro dei dati, la modifica e il re-injection.
-   Esegue sia l'elaborazione di pacchetti che di flussi.
-   Consente di abilitato il filtro pacchetti per ogni applicazione, per utente e per connessione, oltre che per interfaccia di rete o per porta.
-   Garantisce la sicurezza in fase di avvio fino all'Base Filtering Engine (BFE).
-   Abilita il filtro connessioni con stato.
-   Gestisce i dati pre e post-crittografati con IPsec.
-   Consente l'integrazione dei criteri di filtro IPsec e del firewall.
-   Fornisce un'infrastruttura di gestione dei criteri per determinare quando attivare filtri specifici. Ciò include la mediazione di requisiti in conflitto da più filtri forniti da fornitori diversi.
-   Gestisce la maggior parte del riassemblaggio dei pacchetti e il rilevamento dello stato.
-   Include un sistema di notifica utente generico che informa i sottoscrittori delle modifiche al sistema di filtro.
-   Implementa funzioni di enumerazione che segnalano lo stato del sistema.
-   Usa gli eventi net per registrare gli errori IPsec e le eliminazioni dei pacchetti.
-   Supporta una classe helper Framework di diagnostica di rete [(NDF)](/windows/desktop/NDF/extensible-helper-classes).
-   Supporta le estensioni [Secure Socket per](/windows/desktop/WinSock/winsock-secure-socket-extensions) l'API Winsock, che consentono alle applicazioni di rete di proteggere il traffico configurando WFP.
-   Ai livelli ale (Application Layer Enforcement) influisce minimamente sulle prestazioni di rete elaborando solo il primo pacchetto in una connessione.
-   Integra l'offload hardware in cui i moduli callout in modalità kernel possono usare l'hardware per eseguire l'ispezione dei pacchetti specifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura del WFP](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[Operazione WFP](basic-operation.md)
</dt> <dt>

[Applicazione a livello di applicazione (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Configurazione IPsec](ipsec-configuration.md)
</dt> <dt>

[Configurazione di WFP](wfp-configuration.md)
</dt> <dt>

[Monitoraggio del WFP](wfp-monitoring.md)
</dt> <dt>

[WFP API](api-sets.md)
</dt> </dl>

 

