---
title: Operazione PAM
description: Windows Filtering Platform (WFP) esegue le proprie attività integrando i livelli, i filtri, gli shim e i callout seguenti delle entità di base.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e7a7d38bd0de5b1f549e2187c414644bf68442
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299756"
---
# <a name="wfp-operation"></a>Operazione PAM

Windows Filtering Platform (WFP) esegue le proprie attività integrando le seguenti entità di base: *livelli*, *filtri*, *shim* e *callout*.

## <a name="layers"></a>Livelli

Un *livello* è un contenitore gestito dal motore di filtro la cui funzione consiste nell'organizzare i filtri nei set. Un livello non è un modulo nello stack di rete. Ogni livello dispone di uno schema che definisce il tipo di filtri che è possibile aggiungere. Per ulteriori informazioni, vedere [condizioni di filtro disponibili a ogni livello di filtro](filtering-conditions-available-at-each-filtering-layer.md) .

I livelli possono contenere sottolivelli per gestire i requisiti di filtro in conflitto, ad esempio "blocca porte TCP sopra 1024" e "Apri porta 1080". Le regole per la gestione dei conflitti di filtro sono determinate dall' [arbitraggio dei filtri](filter-arbitration.md).

PAM contiene un set di [sottolivelli predefiniti](management-filtering-sublayer-identifiers.md). Ogni livello eredita tutti i livelli secondari incorporati. Gli utenti possono anche aggiungere i propri livelli secondari.

L'elenco dei livelli del motore di filtro è disponibile nella sezione di riferimento argomento [**filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filtri

Un *filtro* è una regola che viene confrontata con i pacchetti in ingresso o in uscita. La regola indica al motore di filtro le operazioni da eseguire con il pacchetto, incluso per chiamare un modulo di callout per l'ispezione approfondita di pacchetti o flussi. Un filtro può, ad esempio, specificare "blocca il traffico con una porta TCP maggiore di 1024" o "richiama gli ID per tutto il traffico non protetto".

Un filtro in fase di avvio è un filtro che viene applicato in fase di avvio non appena viene avviato il driver dello stack TCP/IP (tcpip.sys). Un filtro dell'ora di avvio viene disabilitato all'avvio di BFE. Un filtro è contrassegnato come ora di avvio impostando il [**flag \_ \_ \_ BOOTTIME del flag di filtro FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) quando viene richiamato [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) .

Un filtro in fase di esecuzione è un filtro che viene applicato dopo l'avvio di BFE. Un filtro in fase di esecuzione può essere statico, dinamico o permanente a seconda della modalità di creazione. Per ulteriori informazioni sui diversi tipi di filtri di run-time e sulla relativa durata, vedere [gestione degli oggetti](object-management.md) .

## <a name="shims"></a>Shim

Uno *shim* è un componente in modalità kernel che consente di prendere decisioni di filtro mediante la classificazione rispetto ai livelli del motore di filtro. Ogni shim viene classificato in base a uno o più livelli. Lo shim del modulo del livello di trasporto, ad esempio, viene classificato in base al livello di trasporto in ingresso, al livello di trasporto in uscita e ai livelli di ALE Connect e Receive-Accept per il primo pacchetto di un flusso.

Poiché i pacchetti, i flussi e gli eventi attraversano lo stack di rete, gli shim li analizzano per estrarre le condizioni e i valori classificabili, quindi vengono chiamati nel motore di filtro per valutarli in base ai filtri in un livello specificato. Il motore di filtro può richiamare uno o più callout come parte della classificazione. Gli shim eseguono l'eliminazione effettiva di pacchetti, flussi ed eventi in base al risultato della classificazione eseguita dal motore di filtro.

## <a name="callouts"></a>Callout

Un *callout* è un set di funzioni esposte da un driver e utilizzato per il filtraggio specializzato. Vengono usati per eseguire l'analisi e la manipolazione dei pacchetti, ad esempio l'analisi del virus, l'analisi dei controlli padre per il contenuto non appropriato, l'analisi dei dati di pacchetti per gli strumenti di monitoraggio. Alcuni callout, ad esempio il driver NAT (Network Address Translation), sono incorporati nel sistema operativo. Altri, ad esempio un callout HTTP Parental Control o il callout IDS (Intrusion Detection System), possono essere forniti da fornitori di software indipendenti (ISV). Le funzioni di callout vengono richiamate dal motore di filtro quando un filtro di callout corrispondente viene associato a un livello specificato.

I callout possono essere registrati in qualsiasi livello WFP in modalità kernel. I callout possono restituire un'azione ("Block", "Consenti" e, quando eseguono l'ispezione del flusso, "rinviare", "necessitano di più dati", "Drop Connection") e possono modificare e proteggere il traffico di rete in ingresso e in uscita.

Quando un callout viene registrato con il motore di filtro, può ricevere il traffico di rete per l'elaborazione. Il traffico può essere costituito da pacchetti, flussi o eventi a seconda del livello. Un'applicazione o un agente del firewall fa sì che il traffico venga passato a un callout aggiungendo un filtro la cui azione è "callout" e il cui ID di callout è l'identificatore del callout. I callout possono indicare al motore di filtro di restituire "Block" o "Consenti" allo shim. I callout possono anche restituire "continue" per consentire ad altri filtri di elaborare il pacchetto.

Più callout possono essere esposti da un solo driver di callout.

Prima di poter usare un callout, è necessario aggiungerlo (con [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) e registrarlo (con [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)). Prima della creazione di filtri che fanno riferimento al callout, è necessaria una chiamata a **FwpmCalloutAdd0** . Una chiamata a FwpsCalloutRegister è obbligatoria prima che PAM possa richiamare il callout quando vengono corrispondenti i filtri di callout. Per impostazione predefinita, i filtri che fanno riferimento a callout che sono stati aggiunti ma che non sono ancora stati registrati con il motore di filtro vengono considerati filtri "Block". L'ordine di chiamata di **FwpmCalloutAdd0** e FwpsCalloutRegister non è rilevante. Un callout persistente deve essere aggiunto una sola volta e deve essere registrato ogni volta che viene avviato il driver che implementa il callout, ad esempio dopo un riavvio.

## <a name="classification"></a>Classificazione

La classificazione è il processo di applicazione dei filtri al traffico di rete (pacchetto, flusso o evento) per determinare il risultato di "Consenti" o "blocca" per quel traffico. Per un pacchetto, un flusso o un evento è presente una chiamata di classificazione per livello.

Durante la classificazione, le proprietà (ad esempio, l'indirizzo di origine) del pacchetto, del flusso o dell'evento vengono confrontate con le condizioni di filtro impostate sui filtri in corrispondenza del livello in cui viene richiamata la classificazione. Quando vengono rilevate corrispondenze, viene utilizzato l'algoritmo di [arbitraggio del filtro](filter-arbitration.md) per determinare il risultato del processo di classificazione.

Una richiesta di classificazione viene attivata da uno shim.

Le azioni di classificazione potrebbero essere:

-   Consenti
-   Blocca
-   Callout
    -   Consenti
    -   Blocca
    -   Continua
    -   Rinviare
    -   Sono necessari altri dati
    -   Elimina connessione

## <a name="wfp-operation"></a>Operazione PAM

Al momento dell'avvio, non appena viene avviato il driver dello stack TCP/IP (tcpip.sys), il motore di filtro in modalità kernel impone i criteri di sicurezza del sistema tramite filtri in fase di avvio.

Quando il motore di filtro di base (BFE) viene avviato in modalità utente, i filtri permanenti vengono aggiunti alla piattaforma, i filtri della fase di avvio sono disabilitati e le notifiche vengono inviate ai driver di callout sottoscritti mediante [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0). Le notifiche vengono inviate immediatamente dopo il completamento dell'inizializzazione di BFE. La piattaforma è ora pronta per la registrazione dei callout e per gli oggetti di runtime da aggiungere.

La transizione dal tempo di avvio ai filtri permanenti può essere di alcuni secondi o anche più a lungo in un computer lento. Si tratta di un valore atomico, pertanto se un provider dispone sia di un filtro di avvio che di un filtro persistente, non sarà mai presente alcuna finestra quando nessuna delle due è attiva.

Dopo l'avvio di BFE, i filtri di run-time possono essere aggiunti dagli agenti firewall o dalle soluzioni firewall personalizzate. BFE elabora questi filtri e li invia al livello del motore di filtro appropriato per l'imposizione. BFE accetta anche le impostazioni di autenticazione e invia queste impostazioni ai moduli di chiavi IPsec (IKE/AuthIP). Per ulteriori informazioni, vedere [configurazione IPSec](ipsec-configuration.md) .

In qualsiasi momento, è possibile aggiungere, rimuovere o modificare i filtri e le impostazioni di autenticazione nel sistema tramite l'interfaccia RPC esposta dal BFE. È possibile aggiungere o rimuovere in modo analogo i moduli secondari e i moduli di callout.

Flusso di dati:

1.  Un pacchetto entra nello stack di rete.
2.  Lo stack di rete trova e chiama uno shim.
3.  Lo shim richiama il processo di classificazione a un livello particolare.
4.  Durante la classificazione, vengono confrontati i filtri e viene eseguita l'azione risultante. (Vedere [arbitraggio di filtro](filter-arbitration.md)).
5.  Se durante il processo di classificazione vengono richiamati i filtri di callout, verranno richiamati i callout corrispondenti.
6.  Lo shim agisce sulla decisione di filtro finale, ad esempio eliminando il pacchetto.

Il flusso di dati in uscita segue un modello simile.

Gli argomenti seguenti descrivono ulteriormente il funzionamento del PAM.

-   [Flussi di pacchetti TCP](tcp-packet-flows.md)
-   [Flussi di pacchetti UDP](udp-packet-flows.md)
-   [Arbitraggio di filtro](filter-arbitration.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti](object-model.md)
</dt> <dt>

[Gestione degli oggetti](object-management.md)
</dt> </dl>

 

 