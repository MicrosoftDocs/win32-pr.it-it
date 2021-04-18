---
title: Informazioni sulla piattaforma filtro Windows
description: Windows Filtering Platform (WFP) è una piattaforma di elaborazione del traffico di rete progettata per sostituire le interfacce di filtro del traffico di rete di Windows XP e Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299809"
---
# <a name="about-windows-filtering-platform"></a>Informazioni sulla piattaforma filtro Windows

Windows Filtering Platform (WFP) è una piattaforma di elaborazione del traffico di rete progettata per sostituire le interfacce di filtro del traffico di rete di Windows XP e Windows Server 2003. Pam è costituito da un set di hook nello stack di rete e da un motore di filtro che coordina le interazioni dello stack di rete.

## <a name="the-wfp-components"></a>Componenti di WFP

### <a name="filter-engine"></a>Motore di filtro

Infrastruttura di filtro a più livelli di base, ospitata in modalità kernel e in modalità utente, che sostituisce i più moduli di filtro nel sottosistema di rete Windows XP e Windows Server 2003.

-   Filtra il traffico di rete a qualsiasi livello del sistema su tutti i campi dati che uno shim può fornire.
-   Implementa i filtri "callout" richiamando i callout durante la classificazione.
-   Restituisce le azioni "Consenti" o "blocca" allo shim che lo ha richiamato per l'imposizione.
-   Fornisce l'arbitraggio tra diverse origini dei criteri. Ad esempio, determina la priorità quando un'applicazione viene configurata per proteggere il traffico di rete correlato, ma il firewall locale è configurato per impedire il traffico protetto dell'applicazione.<br/>

### <a name="base-filtering-engine-bfe"></a>Motore di filtro di base (BFE)

Servizio che controlla il funzionamento della piattaforma filtro Windows. Esegue le attività seguenti.

-   Accetta filtri e altre impostazioni di configurazione per la piattaforma.
-   Segnala lo stato corrente del sistema, incluse le statistiche.
-   Impone il modello di sicurezza per l'accettazione della configurazione nella piattaforma. Ad esempio, un amministratore locale può aggiungere filtri, ma gli altri utenti possono visualizzarli.<br/>
-   Plumbe le impostazioni di configurazione per altri moduli nel sistema. Ad esempio, i criteri di negoziazione IPsec passano a moduli di chiavi IKE/AuthIP, i filtri passano al motore di filtro.<br/>

### <a name="shims"></a>Shim

Componenti in modalità kernel che si trovano tra lo stack di rete e il motore di filtro. Gli shim effettuano la decisione di filtro classificando il motore di filtro. Di seguito è riportato un elenco di shim disponibili.

-   Shim ALE (Application Layer Enforcement).
-   Shim del modulo layer di trasporto.
-   Shim del modulo a livello di rete.
-   Shim di errore Internet Control Message Protocol (ICMP).
-   Ignora shim.
-   Shim flusso.

### <a name="callouts"></a>Callout

Set di funzioni esposte da un driver e utilizzate per il filtraggio specializzato. Oltre alle azioni di base di "Consenti" e "blocco", i callout possono modificare e proteggere il traffico di rete in ingresso e in uscita. Per ulteriori informazioni sui callout, vedere l'argomento [driver di callout della piattaforma filtro Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) nella documentazione di Windows Driver Kit (WDK). PAM fornisce callout predefiniti che eseguono le seguenti attività.<br/>

-   Eseguire l'elaborazione IPsec.
-   Modificare il comportamento del filtro con stato.
-   Eseguire il filtro in modalità Stealth (eliminazione invisibile di pacchetti non richiesti).
-   Controllare TCP Chimney Offload.
-   Interagire con il servizio Teredo.

<br/> Il motore di filtro consente la registrazione di callout di terze parti in ognuno dei relativi livelli in modalità kernel.<br/>

### <a name="application-programming-interface"></a>Interfaccia di programmazione delle applicazioni

Set di tipi di dati e funzioni disponibili agli sviluppatori per compilare e gestire le applicazioni di filtro di rete. Questi tipi di dati e funzioni sono raggruppati in più [set di API](api-sets.md).

## <a name="wfp-features"></a>Funzionalità di WFP

-   Fornisce un'infrastruttura di filtro dei pacchetti in cui i fornitori di software indipendenti (ISV) possono collegare moduli di filtro specializzati.
-   Funziona con IPv4 e IPv6.
-   Consente il filtraggio, la modifica e il reinserimento dei dati.
-   Esegue l'elaborazione di pacchetti e flussi.
-   Consente l'abilitazione del filtro pacchetti per ogni applicazione, per utente e per connessione, oltre a per interfaccia di rete o per porta.
-   Fornisce la sicurezza in fase di avvio fino a quando non è possibile avviare BFE (Base Filtering Engine).
-   Consente di filtrare le connessioni con stato.
-   Gestisce sia i dati pre che quelli crittografati tramite IPsec.
-   Consente l'integrazione dei criteri di filtro firewall e IPsec.
-   Fornisce un'infrastruttura di gestione dei criteri per determinare quando devono essere attivati filtri specifici. Ciò include la mediazione dei requisiti in conflitto da più filtri forniti da fornitori diversi.
-   Gestisce la maggior parte del riassemblaggio del pacchetto e del rilevamento dello stato.
-   Include un sistema di notifica utente generico che informa i sottoscrittori delle modifiche apportate al sistema di filtraggio.
-   Implementa funzioni di enumerazione che segnalano lo stato del sistema.
-   USA gli eventi NET per registrare gli errori IPsec e le gocce di pacchetti.
-   Supporta una [classe helper NDF (](/windows/desktop/NDF/extensible-helper-classes)Network Diagnostics Framework).
-   Supporta le [estensioni Secure Socket](/windows/desktop/WinSock/winsock-secure-socket-extensions) per l'API Winsock, che consentono alle applicazioni di rete di proteggere il traffico tramite la configurazione di WFP.
-   Ai livelli dell'applicazione a livello di applicazione (ALE), ha un effetto minimo sulle prestazioni di rete mediante l'elaborazione del primo pacchetto in una connessione.
-   Integra l'offload hardware in cui i moduli di callout in modalità kernel possono usare l'hardware per eseguire un'ispezione specifica dei pacchetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura WFP](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[Operazione PAM](basic-operation.md)
</dt> <dt>

[Application Layer Enforcement (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Configurazione IPsec](ipsec-configuration.md)
</dt> <dt>

[Configurazione di WFP](wfp-configuration.md)
</dt> <dt>

[Monitoraggio WFP](wfp-monitoring.md)
</dt> <dt>

[API PAM](api-sets.md)
</dt> </dl>

 

