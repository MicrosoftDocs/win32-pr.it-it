---
title: Novità dell'API server HTTP versione 2,0
description: Nell'API server HTTP versione 2,0 sono disponibili le funzionalità seguenti.
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- Novità dell'API server HTTP versione 2,0
- API server HTTP versione 2,0, novità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 932a27a45768d0cb00cde4cb89fc4e5d424d1f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044331"
---
# <a name="whats-new-for-http-server-version-20-api"></a>Novità dell'API server HTTP versione 2,0

L'API server HTTP versione 2,0 aggiunge gli oggetti di configurazione delle proprietà e la gestione delle code di richiesta avanzate. Per ulteriori informazioni e per un elenco completo di funzioni, vedere l'argomento di [riferimento versione HTTP Server 2,0](http-server-api-version-2-0-reference.md) . Nell'API server HTTP versione 2,0 sono disponibili le funzionalità seguenti.

## <a name="configuration-objects"></a>Oggetti di configurazione

Gli oggetti di configurazione della sessione del server e del gruppo di URL consentono alle applicazioni di configurare il servizio HTTP. La sessione del server è l'oggetto di configurazione di primo livello che sostituisce le impostazioni predefinite dell'API del server HTTP per tutti i gruppi di URL creati nella sessione. Il gruppo URL, creato in una sessione del server, gestisce un set di URL che ricevono le impostazioni di configurazione per il gruppo. Per ulteriori informazioni, vedere l'argomento [architettura http versione 2,0](http-version-2-0-architecture.md) .

## <a name="property-configuration-in-version-20"></a>Configurazione della proprietà nella versione 2,0

La configurazione viene eseguita negli oggetti sessione del server o gruppo di URL. Le configurazioni a livello di server sono impostate nell'oggetto configurazione della sessione del server. I gruppi di URL, creati nella sessione del server, ereditano le configurazioni di sessione del server. Le configurazioni impostate nel gruppo di URL eseguono l'override delle configurazioni di sessione del server. Le configurazioni che possono essere impostate dall'applicazione includono i timeout di connessione, i limiti delle connessioni, l'autenticazione e la registrazione. Per ulteriori informazioni, vedere l'argomento [configurazione delle proprietà nella versione HTTP 2,0](configuring-properties-in-http-version-2-0.md) .

## <a name="process-isolation-on-request-queues"></a>Isolamento del processo nelle code di richiesta

La coda di richieste versione 2,0 supporta l'isolamento dei processi, consentendo a più processi di lavoro di eseguire operazioni di i/o nella coda di richieste. Le proprietà di configurazione impostate nella coda di richieste consentono alle applicazioni di avere un maggiore controllo sul servizio. La funzionalità della coda di richieste denominata consente alle applicazioni di creare code di richieste e di proteggerle con elenchi di controllo di accesso (ACL). Le applicazioni che operano con account utente diversi dall'account che ha creato la coda di richieste sono in grado di aprire la coda di richieste, ricevere richieste e inviare risposte. Per ulteriori informazioni, vedere l'argomento relativo all' [isolamento dei processi](process-isolation.md) .

## <a name="full-kernel-mode-ssl"></a>SSL in modalità kernel completa

La sicurezza SSL in modalità kernel è abilitata per impostazione predefinita. sono supportati anche i certificati client per l'autenticazione reciproca. Le prestazioni vengono aumentate completando le operazioni SSL in modalità kernel, riducendo così le transizioni tra il kernel e la modalità utente. Per ulteriori informazioni, vedere l'argomento relativo a [SSL in modalità kernel](kernel-mode-ssl.md) .

## <a name="kernel-mode-response-cache"></a>Cache di risposta in modalità kernel

Le risposte con contenuto statico possono essere memorizzate nella cache in modalità kernel garantendo un miglioramento delle prestazioni rispetto alla cache in modalità utente. La struttura dei criteri di cache viene inviata con la risposta. Per ulteriori informazioni, vedere l'argomento relativo alla [cache in modalità kernel nell'argomento HTTP 2,0](kernel-mode-cache-in-http-2-0.md) .

## <a name="authentication"></a>Authentication

La \_ risposta http e le \_ strutture di richiesta HTTP vengono aggiornate per includere le informazioni di autenticazione. L'autenticazione sul lato server è supportata per gli schemi seguenti: Negotiate, NTLM, Basic e digest. Le applicazioni possono specificare gli schemi di autenticazione supportati e impostare l'ordine di preferenza per tali schemi.

## <a name="object-scoped-versioning"></a>Controllo delle versioni con ambito di oggetto

L'API server HTTP versione 1,0 ha passato le informazioni sulla versione nella chiamata a HTTPInitialize. La versione è stata impostata globalmente per tutte le applicazioni nello stesso processo. Nell'API server HTTP versione 2,0 le informazioni sulla versione vengono fornite al momento della creazione dell'oggetto. Per ulteriori informazioni, vedere [controllo delle versioni in http server versione 2,0 API](versioning-in-http-2-0.md).

## <a name="logging"></a>Registrazione

A partire dalla versione 2,0, la registrazione può essere configurata tramite l'API del server HTTP. La registrazione abilitata in una sessione server serve come forma centralizzata di registrazione per il servizio. È anche possibile abilitare la registrazione in un gruppo di URL per i file di log individuali. L'applicazione specifica il formato per i file di log, nonché i campi che vengono registrati per individuare eventuali errori e transazioni con esito positivo.

## <a name="graceful-request-queue-shutdown"></a>Arresto normale della coda di richieste

Le applicazioni possono arrestare la coda delle richieste e gestire correttamente le richieste in attesa nella coda prima di terminare il processo della coda di richieste. Quando la coda di richieste viene arrestata, l'API del server HTTP interrompe l'accodamento delle richieste e reindirizza le richieste in attesa nella coda delle richieste.

## <a name="demand-start-on-a-request-queue"></a>Avvio della richiesta in una coda di richieste

La funzionalità di avvio della richiesta nella coda di richieste consente all'applicazione controller di ritardare la creazione di un'istanza del processo di lavoro fino a quando la prima richiesta arriva nella coda di richieste. Pertanto, le applicazioni possono evitare l'utilizzo di risorse fino a quando non sono necessarie. Per ulteriori informazioni, vedere l'argomento [sulla richiesta di avvio della versione 2,0](demand-start-on-version-2-0-request-queues.md) per le code di richieste.

## <a name="port-sharing"></a>Condivisione delle porte

Le applicazioni basate su API del server HTTP condividono automaticamente lo spazio di ascolto IP con altre applicazioni basate su API del server non HTTP nel computer. l'elenco di ascolto IP non è più necessario. Quando l'applicazione registra un URL, l'API del server HTTP resta in attesa solo sulla coppia di porta e indirizzo IP specificati.

## <a name="etw-support"></a>Supporto ETW

La traccia avanzata tramite il Event Tracing for Windows (ETW) consente alle applicazioni di ottenere una maggiore capacità di diagnostica. Traccia eventi è disponibile per le registrazioni e le prenotazioni URL, la configurazione delle proprietà, gli eventi della cache, l'autenticazione e la registrazione per citarne alcuni.

## <a name="performance-counters"></a>Contatori delle prestazioni

Lo strumento contatore delle prestazioni consente alle applicazioni di recuperare i contatori dei servizi e di diagnosticare le prestazioni del servizio. I contatori globali tengono traccia delle prestazioni per il servizio, i contatori del sito tengono traccia delle prestazioni dei gruppi di URL e i contatori della coda delle richieste tengono traccia delle prestazioni della coda di

## <a name="international-domain-names-idn"></a>Nomi di dominio internazionali (IDN)

Parti host e percorso internazionalizzate dell'URL consentono la registrazione di percorsi e nomi di dominio non ASCII. L'API server HTTP elabora gli URL Unicode per conformità con gli standard IDN.

## <a name="netsh-extensions"></a>Estensioni NetSH

L'utilità netsh sostituisce lo strumento HttpCfg.exe disponibile in Windows Server 2003 e Windows XP con Service Pack 2 (SP2). L'estensione Netsh fornisce un mezzo per gestire, diagnosticare e configurare il servizio HTTP. Gli amministratori possono eseguire query e configurare impostazioni a livello di server, ad esempio registrazioni dello spazio dei nomi e certificati SSL.

 

 




