---
title: Remote Desktop Protocol
description: Il protocollo Desktop remoto Microsoft (RDP) fornisce funzionalità di visualizzazione e input Remote sulle connessioni di rete per le applicazioni basate su Windows in esecuzione in un server.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Remote Desktop Protocol (RDP) Servizi Desktop remoto
- RDP (vedere Remote Desktop Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299920"
---
# <a name="remote-desktop-protocol"></a>Remote Desktop Protocol

Il protocollo Desktop remoto Microsoft (RDP) fornisce funzionalità di visualizzazione e input Remote sulle connessioni di rete per le applicazioni basate su Windows in esecuzione in un server. RDP è progettato per supportare diversi tipi di topologie di rete e più protocolli LAN.

> [!Note]  
> Questo argomento è per gli sviluppatori di software. Per informazioni sull'utente per Desktop remoto, vedere [supporto di Windows](https://windows.microsoft.com/windows/support#1TC=windows-8). Per informazioni sui professionisti IT per Desktop remoto, vedere [Servizi Desktop remoto su TechNet](/windows/deployment/deploy-whats-new).

 

## <a name="basic-architecture"></a>Architettura di base

RDP si basa su e su un'estensione della famiglia di protocolli ITU T. 120. RDP è un protocollo in grado di supportare più canali che consente di usare canali virtuali distinti per il trasporto di dati di comunicazione e presentazione del dispositivo dal server, oltre ai dati crittografati del mouse e della tastiera del client. RDP fornisce una base estendibile e supporta fino a 64.000 canali separati per la trasmissione dei dati e il provisioning per la trasmissione multipoint.

Sul server, RDP usa il proprio driver video per eseguire il rendering dell'output di visualizzazione costruendo le informazioni di rendering nei pacchetti di rete usando il protocollo RDP e inviando i dati attraverso la rete al client. Sul client, il protocollo RDP riceve i dati di rendering e interpreta i pacchetti nelle chiamate API GDI (Graphics Device Interface) corrispondenti di Microsoft Windows. Per il percorso di input, gli eventi del mouse e della tastiera del client vengono reindirizzati dal client al server. Sul server, il protocollo RDP utilizza il proprio driver di tastiera e mouse per ricevere gli eventi della tastiera e del mouse.

In una sessione di Desktop remoto tutte le variabili di ambiente, ad esempio le variabili che determinano la profondità dei colori e l'abilitazione e la disabilitazione dello sfondo, sono determinate dalle impostazioni di connessione RCP-Tcp. Questo vale per tutte le funzioni e i metodi che impostano le variabili di ambiente nel [riferimento connessione Web Desktop remoto](remote-desktop-web-connection-reference.md) e nell' [interfaccia del provider servizi desktop remoto WMI](terminal-services-wmi-provider-reference.md).

## <a name="features"></a>Funzionalità

In Microsoft RDP sono incluse le funzionalità e le funzionalità seguenti:

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Crittografia
</dt> <dd>

RDP usa la crittografia RC4 di RSA Security, una crittografia di flusso progettata per crittografare in modo efficiente piccole quantità di dati. RC4 è progettato per garantire comunicazioni sicure su reti. Gli amministratori possono scegliere di crittografare i dati usando una chiave di 56 o 128 bit.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Funzionalità di riduzione della larghezza di banda
</dt> <dd>

RDP supporta diversi meccanismi per ridurre la quantità di dati trasmessi tramite una connessione di rete. I meccanismi includono la compressione dei dati, la memorizzazione nella cache persistente delle bitmap e la memorizzazione nella cache di glifi e frammenti in RAM. La cache di bitmap persistente può offrire un miglioramento sostanziale delle prestazioni rispetto alle connessioni a larghezza di banda ridotta, soprattutto quando si eseguono applicazioni che fanno uso estensivo di bitmap di grandi dimensioni.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Disconnessione roaming
</dt> <dd>

Un utente può disconnettersi manualmente da una sessione di desktop remoto senza disconnettersi. L'utente viene automaticamente riconnesso alla sessione disconnessa quando si connette nuovamente al sistema, dallo stesso dispositivo o da un dispositivo diverso. Quando la sessione di un utente viene interrotta in modo imprevisto da un errore di rete o del client, l'utente viene disconnesso ma non disconnesso.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Mapping degli Appunti
</dt> <dd>

Gli utenti possono eliminare, copiare e incollare testo e grafica tra le applicazioni in esecuzione nel computer locale e quelle eseguite in una sessione Desktop remoto e tra le sessioni.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Reindirizzamento di stampa
</dt> <dd>

Le applicazioni in esecuzione all'interno di una sessione Desktop remoto possono stampare su una stampante collegata al dispositivo client.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canali virtuali
</dt> <dd>

Utilizzando l'architettura del canale virtuale RDP, è possibile aumentare le applicazioni esistenti e sviluppare nuove applicazioni per aggiungere funzionalità che richiedono le comunicazioni tra il dispositivo client e un'applicazione in esecuzione in una sessione di desktop remoto.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Controllo remoto
</dt> <dd>

Il personale di supporto del computer può visualizzare e controllare una sessione Desktop remoto. La condivisione di input e la visualizzazione di immagini tra due sessioni di desktop remoto offre a un utente di supporto la possibilità di diagnosticare e risolvere i problemi in modalità remota.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Bilanciamento carico di rete
</dt> <dd>

RDP sfrutta i vantaggi del bilanciamento del carico di rete, se disponibile.

</dd> </dl>

Inoltre, RDP contiene le funzionalità seguenti:

-   Supporto per il colore a 24 bit.
-   Miglioramento delle prestazioni rispetto alle connessioni remote a bassa velocità tramite una larghezza di banda ridotta.
-   Autenticazione con smart card tramite Servizi Desktop remoto.
-   Hook da tastiera. Possibilità di indirizzare le combinazioni di tasti speciali di Windows, in modalità schermo intero, al computer locale o a un computer remoto.
-   Reindirizzamento stampanti audio, unità, porta e rete. I suoni che si verificano nel computer remoto possono essere rilevati nel computer client in cui è in esecuzione il client RDC e le unità client locali saranno visibili alla sessione Desktop remoto.

 

 