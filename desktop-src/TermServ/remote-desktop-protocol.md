---
title: Remote Desktop Protocol
description: Il Desktop remoto Microsoft Protocol (RDP) offre funzionalità di input e visualizzazione remota tramite connessioni di rete per Windows in esecuzione in un server.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Remote Desktop Protocol (RDP) Servizi Desktop remoto
- RDP (vedere Remote Desktop Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a322e90bd036533e357925607fac6a78c364eababad5f353b4d53dfa51df735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756172"
---
# <a name="remote-desktop-protocol"></a>Remote Desktop Protocol

Il Desktop remoto Microsoft Protocol (RDP) offre funzionalità di input e visualizzazione remota tramite connessioni di rete per Windows in esecuzione in un server. RDP è progettato per supportare diversi tipi di topologie di rete e più protocolli LAN.

> [!Note]  
> Questo argomento è per sviluppatori di software. Per informazioni sull'utente per Desktop remoto, vedere Windows [support](https://windows.microsoft.com/windows/support#1TC=windows-8). Per informazioni sui professionisti IT per Desktop remoto, vedere Servizi Desktop remoto [su TechNet.](/windows/deployment/deploy-whats-new)

 

## <a name="basic-architecture"></a>Architettura di base

RDP si basa su e su un'estensione della famiglia di protocolli ITU T.120. RDP è un protocollo con supporto per più canali che consente canali virtuali separati per il trasporto di dati di presentazione e comunicazione del dispositivo dal server, nonché dati crittografati del mouse e della tastiera client. RDP offre una base estensibile e supporta fino a 64.000 canali separati per la trasmissione dei dati e il provisioning per la trasmissione multipoint.

Nel server RDP usa il proprio driver video per eseguire il rendering dell'output visualizzato creando le informazioni di rendering in pacchetti di rete usando il protocollo RDP e inviandole in rete al client. Nel client RDP riceve i dati di rendering e interpreta i pacchetti nelle chiamate API GDI (Graphics Device Interface) di Microsoft Windows corrispondenti. Per il percorso di input, gli eventi del mouse e della tastiera client vengono reindirizzati dal client al server. Nel server RDP usa il proprio driver di tastiera e mouse per ricevere questi eventi di tastiera e mouse.

In una sessione Desktop remoto, tutte le variabili di ambiente, ad esempio le variabili che determinano la profondità del colore e lo sfondo che abilitano e disabilitano, sono determinate dalle impostazioni di connessione RCP-Tcp predefinite. Questo vale per tutte le funzioni e i metodi che impostano le variabili di ambiente nel riferimento [Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md) e nell Servizi Desktop remoto intervazione [del provider WMI.](terminal-services-wmi-provider-reference.md)

## <a name="features"></a>Funzionalità

Microsoft RDP include le funzionalità e le funzionalità seguenti:

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Crittografia
</dt> <dd>

RDP usa la crittografia RC4 di RSA Security, una crittografia di flusso progettata per crittografare in modo efficiente piccole quantità di dati. RC4 è progettato per le comunicazioni protette sulle reti. Gli amministratori possono scegliere di crittografare i dati usando una chiave a 56 o 128 bit.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Funzionalità di riduzione della larghezza di banda
</dt> <dd>

RDP supporta vari meccanismi per ridurre la quantità di dati trasmessi tramite una connessione di rete. I meccanismi includono la compressione dei dati, la memorizzazione nella cache persistente delle bitmap e la memorizzazione nella cache di glifi e frammenti nella RAM. La cache bitmap persistente può offrire un miglioramento sostanziale delle prestazioni rispetto alle connessioni a larghezza di banda ridotta, soprattutto quando si eseguono applicazioni che usano bitmap di grandi dimensioni.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Disconnessione in roaming
</dt> <dd>

Un utente può disconnettersi manualmente da una sessione desktop remoto senza disconnettersi. L'utente viene riconnesso automaticamente alla sessione disconnessa quando accede di nuovo al sistema, dallo stesso dispositivo o da un dispositivo diverso. Quando la sessione di un utente viene terminata in modo imprevisto da un errore di rete o client, l'utente viene disconnesso ma non disconnesso.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Mapping degli Appunti
</dt> <dd>

Gli utenti possono eliminare, copiare e incollare testo e grafica tra le applicazioni in esecuzione nel computer locale e quelle in esecuzione in una sessione desktop remoto e tra una sessione e l'altra.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Reindirizzamento della stampa
</dt> <dd>

Le applicazioni in esecuzione all'interno di una sessione desktop remoto possono stampare su una stampante collegata al dispositivo client.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canali virtuali
</dt> <dd>

Usando l'architettura del canale virtuale RDP, è possibile aumentare le applicazioni esistenti e sviluppare nuove applicazioni per aggiungere funzionalità che richiedono comunicazioni tra il dispositivo client e un'applicazione in esecuzione in una sessione desktop remoto.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Telecomando
</dt> <dd>

Il personale del supporto tecnico può visualizzare e controllare una sessione desktop remoto. La condivisione di grafica di input e visualizzazione tra due sessioni desktop remoto offre a un utente del supporto la possibilità di diagnosticare e risolvere i problemi in remoto.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Bilanciamento del carico di rete
</dt> <dd>

RDP sfrutta il bilanciamento del carico di rete (NLB), se disponibile.

</dd> </dl>

RdP contiene inoltre le funzionalità seguenti:

-   Supporto per il colore a 24 bit.
-   Prestazioni migliorate rispetto alle connessioni remote a bassa velocità tramite una larghezza di banda ridotta.
-   Autenticazione con smart card tramite Servizi Desktop remoto.
-   Hook della tastiera. Possibilità di indirizzare Windows combinazioni di tasti speciali, in modalità schermo intero, al computer locale o a un computer remoto.
-   Reindirizzamento audio, unità, porta e stampante di rete. I suoni che si verificano nel computer remoto possono essere ascoltati nel computer client che esegue il client RdC e le unità client locali saranno visibili alla sessione desktop remoto.

 

 