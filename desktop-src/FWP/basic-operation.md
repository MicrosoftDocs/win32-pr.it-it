---
title: Operazione WFP
description: Windows Filtering Platform (WFP) esegue le proprie attività integrando le entità di base livelli, filtri, s shims e callout seguenti.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254ed468b856392477a643ce13f2b609245031f7363865b8c93ccfda64ba9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015389"
---
# <a name="wfp-operation"></a>Operazione WFP

Windows Filtering Platform (WFP) esegue le proprie attività integrando le entità di base seguenti: *Livelli,* *Filtri,* *S shims* e *Callout.*

## <a name="layers"></a>Livelli

Un *livello* è un contenitore gestito dal motore di filtro la cui funzione è organizzare i filtri in set. Un livello non è un modulo nello stack di rete. Ogni livello ha uno schema che definisce il tipo di filtri che è possibile aggiungere. Per [altre informazioni, vedere Condizioni di](filtering-conditions-available-at-each-filtering-layer.md) filtro disponibili in Ogni livello di filtro.

I livelli possono contenere livelli secondari per gestire requisiti di filtro in conflitto, ad esempio "Blocca porte TCP superiori a 1024" e "Porta aperta 1080". Le regole per la gestione dei conflitti di filtro sono determinate da [Filter Arbitration.](filter-arbitration.md)

WFP contiene un set [di sotto-livelli predefiniti.](management-filtering-sublayer-identifiers.md) Ogni livello eredita tutti i sottostrati predefiniti. Gli utenti possono anche aggiungere i propri livelli secondari.

L'elenco dei livelli del motore di filtro è disponibile nell'argomento della sezione di riferimento [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filtri

Un *filtro* è una regola corrispondente ai pacchetti in ingresso o in uscita. La regola indica al motore di filtro cosa fare con il pacchetto, incluso chiamare un modulo callout per l'ispezione approfondita dei pacchetti o dei flussi. Ad esempio, un filtro può specificare "Blocca il traffico con una porta TCP maggiore di 1024" o "Chiama a IDS per tutto il traffico non protetto".

Un filtro in fase di avvio è un filtro applicato in fase di avvio non appena viene avviato il driver dello stack TCP/IP (tcpip.sys). Un filtro in fase di avvio è disabilitato all'avvio di BFE. Un filtro viene contrassegnato come boot-time impostando il flag [**FWPM \_ FILTER \_ FLAG \_ BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) quando viene richiamato [**FwpmFilterAdd0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Un filtro di run-time è un filtro applicato dopo l'avvio di BFE. Un filtro di run-time può essere statico, dinamico o persistente a seconda del modo in cui è stato creato. Per [altre informazioni sui](object-management.md) diversi tipi di filtri di run-time e sulla relativa durata, vedere Gestione oggetti.

## <a name="shims"></a>Spessori

Uno *shim è* un componente in modalità kernel che prende decisioni di filtro classificando in base ai livelli del motore di filtro. Ogni shim classifica in base a uno o più livelli. Ad esempio, lo shim Transport Layer Module classifica in base al livello Trasporto in ingresso, al livello Trasporto in uscita e ai livelli ale Connessione e Receive-Accept per il primo pacchetto di un flusso.

Quando pacchetti, flussi ed eventi attraversano lo stack di rete, gli s shims li analizzano per estrarre le condizioni e i valori classificabili e quindi chiamano il motore di filtro per valutarli in base ai filtri in un determinato livello. Il motore di filtro può richiamare uno o più callout come parte della classificazione. Gli s shims esempono l'eliminazione effettiva di pacchetti, flussi ed eventi in base al risultato della classificazione eseguita dal motore di filtro.

## <a name="callouts"></a>Callout

Un *callout* è un set di funzioni esposte da un driver e usate per filtri specializzati. Vengono usati per eseguire l'analisi e la manipolazione dei pacchetti, ad esempio l'analisi dei virus, il controllo genitori alla ricerca di contenuto inappropriato, l'analisi dei dati dei pacchetti per gli strumenti di monitoraggio. Alcuni callout, ad esempio il driver NAT (Network Address Translation), sono incorporati nel sistema operativo. Altri, ad esempio un callout HTTP Parental Control o il callout IDS (Intrusion Detection System), possono essere forniti da fornitori di software indipendenti (ISV). Le funzioni callout vengono richiamate dal motore di filtro quando viene trovata una corrispondenza con un filtro callout corrispondente a un determinato livello.

I callout possono essere registrati in qualsiasi livello WFP in modalità kernel. I callout possono restituire un'azione ("Blocca", "Consenti" e, quando si esegue l'ispezione del flusso, "Rinvia", "Servono più dati", "Elimina connessione") e possono modificare e proteggere il traffico di rete in ingresso e in uscita.

Una volta registrato con il motore di filtro, un callout può ricevere il traffico di rete da elaborare. Il traffico può essere pacchetti, flussi o eventi a seconda del livello. Un agente applicazione o firewall fa sì che il traffico sia passato a un callout aggiungendo un filtro la cui azione è "Callout" e il cui ID callout è l'identificatore del callout. I callout possono indicare al motore di filtro di restituire "Block" o "Permit" per lo shim. I callout possono anche restituire "Continue" per consentire ad altri filtri di elaborare il pacchetto.

Più callout possono essere esposti da un driver di callout.

Un callout deve essere aggiunto (con [**FwpmCalloutAdd0)**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)e registrato (con [FwpsCalloutRegister)](/windows-hardware/drivers/ddi/_netvista/)prima di poterlo usare. Una chiamata a **FwpmCalloutAdd0** è necessaria prima della creazione di filtri che fanno riferimento al callout. Una chiamata a FwpsCalloutRegister è necessaria prima che WFP possa richiamare il callout quando i filtri di callout corrispondono. Per impostazione predefinita, i filtri che fanno riferimento ai callout aggiunti ma non ancora registrati con il motore di filtro vengono considerati filtri "Blocca". L'ordine di chiamata **di FwpmCalloutAdd0** e FwpsCalloutRegister non è importante. Un callout permanente deve essere aggiunto una sola volta e deve essere registrato ogni volta che il driver che implementa il callout viene avviato (ad esempio, dopo un riavvio).

## <a name="classification"></a>Classificazione

La classificazione è il processo di applicazione di filtri al traffico di rete (pacchetto, flusso o evento) per determinare il risultato di "Permit" o "Block" per tale traffico. Per un pacchetto, un flusso o un evento è presente una chiamata di classificazione per ogni livello.

Durante la classificazione, le proprietà (ad esempio, l'indirizzo di origine) del pacchetto, del flusso o dell'evento vengono confrontate con le condizioni di filtro impostate sui filtri nel livello in cui viene richiamata la classificazione. Quando vengono trovate corrispondenze, [l'algoritmo Filter Arbitration](filter-arbitration.md) viene usato per determinare il risultato del processo di classificazione.

Una richiesta di classificazione viene attivata da uno shim.

Le azioni di classificazione possono essere:

-   Consenti
-   Blocca
-   Callout
    -   Consenti
    -   Blocca
    -   Continua
    -   Rinviare
    -   Sono necessari più dati
    -   Eliminare la connessione

## <a name="wfp-operation"></a>Operazione WFP

In fase di avvio, non appena viene avviato il driver dello stack TCP/IP (tcpip.sys), il motore di filtro in modalità kernel applica i criteri di sicurezza del sistema tramite filtri in fase di avvio.

Quando il Base Filtering Engine (BFE) viene avviato in modalità utente, vengono aggiunti filtri permanenti alla piattaforma, i filtri in fase di avvio vengono disabilitati e le notifiche vengono inviate ai driver callout sottoscritti tramite [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0). Le notifiche vengono inviate immediatamente dopo il completamento dell'inizializzazione BFE. La piattaforma è ora pronta per la registrazione dei callout e per l'aggiunta di oggetti in fase di esecuzione.

La transizione dal tempo di avvio ai filtri permanenti può essere di diversi secondi o anche più lunga in un computer lento. È atomico, quindi se un provider ha sia un filtro in fase di avvio che un filtro permanente, non verrà mai visualizzata una finestra quando nessuno dei due è attivo.

Dopo l'avvio di BFE, i filtri di run-time possono essere aggiunti dagli agenti firewall o da soluzioni firewall personalizzate. BFE elabora questi filtri e li invia al livello del motore di filtro appropriato per l'imposizione. BFE accetta anche le impostazioni di autenticazione e le invia ai moduli di keying IPsec (IKE/AuthIP). Per [altre informazioni, vedere Configurazione IPsec.](ipsec-configuration.md)

In qualsiasi momento, i filtri e le impostazioni di autenticazione possono essere aggiunti, rimossi o modificati nel sistema tramite l'interfaccia RPC esposta dal BFE. I sotto-livelli e i moduli callout possono essere aggiunti o rimossi allo stesso modo.

Flusso di dati:

1.  Un pacchetto entra nello stack di rete.
2.  Lo stack di rete trova e chiama uno shim.
3.  Lo shim richiama il processo di classificazione a un livello specifico.
4.  Durante la classificazione, viene trovata una corrispondenza con i filtri e viene eseguita l'azione risultante. Vedere [l'arbitraggio dei](filter-arbitration.md)filtri.
5.  Se durante il processo di classificazione viene trovata una corrispondenza con i filtri di callout, vengono richiamati i callout corrispondenti.
6.  Lo shim agisce sulla decisione di filtro finale (ad esempio, eliminare il pacchetto).

Il flusso di dati in uscita segue un modello simile.

Gli argomenti seguenti descrivono ulteriormente il funzionamento del WFP.

-   [Flussi di pacchetti TCP](tcp-packet-flows.md)
-   [Flussi di pacchetti UDP](udp-packet-flows.md)
-   [Filtra arbitraggio](filter-arbitration.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti](object-model.md)
</dt> <dt>

[Gestione oggetti](object-management.md)
</dt> </dl>

 

 