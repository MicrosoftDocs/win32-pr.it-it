---
title: Filtra arbitraggio
description: L'arbitraggio dei filtri è la logica incorporata nella piattaforma di filtro Windows (WFP) usata per determinare il modo in cui i filtri interagiscono tra loro quando si prendono decisioni relative ai filtri del traffico di rete.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7640e94440cf040d9ca51b6c639dc66e3e8a767024d6dbcd01b9c0cd2b87a24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151190"
---
# <a name="filter-arbitration"></a>Filtra arbitraggio

L'arbitraggio dei filtri è la logica incorporata nella piattaforma di filtro Windows (WFP) usata per determinare il modo in cui i filtri interagiscono tra loro quando si prendono decisioni relative ai filtri del traffico di rete.

## <a name="filter-arbitration-behaviors"></a>Filtrare i comportamenti di arbitraggio

I comportamenti seguenti caratterizzano il sistema di arbitraggio dei filtri:

-   Tutto il traffico può essere controllato. Nessun traffico può ignorare i filtri a un determinato livello.
-   Il traffico può essere bloccato da un filtro callout tramite **un veto** anche se è consentito da un filtro con priorità più alta.
-   Più provider possono controllare il traffico allo stesso livello. Ad esempio, il firewall seguito dai filtri del sistema di rilevamento delle intrusioni (IDS) o IPsec seguito dai filtri QoS (Quality of Service) può esaminare tutti il traffico allo stesso livello.

## <a name="filtering-model"></a>Modello di filtro

Ogni livello di filtro è suddiviso in sottostrati ordinati in base alla priorità (detto anche peso). Il traffico di rete attraversa i livelli secondari dalla priorità più alta alla priorità più bassa. I sotto-livelli vengono creati e gestiti dagli sviluppatori usando l'API WFP.

All'interno di ogni livello secondario, i filtri vengono ordinati in base al peso. Il traffico di rete viene indicato per abbinare i filtri dal peso più alto al peso più basso.

L'algoritmo di arbitraggio dei filtri viene applicato a tutti i sottostrati all'interno di un livello e la decisione finale del filtro viene presa dopo la valutazione di tutti i livelli secondari. In questo modo sono disponibili più funzionalità di corrispondenza.

All'interno di un livello secondario, l'arbitraggio dei filtri viene eseguito come segue:

-   Calcolare l'elenco di filtri corrispondenti ordinati in base al peso dal più alto al più basso.
-   Valutare i filtri corrispondenti nell'ordine fino a quando non viene restituito "Permit" o "Block" (i filtri possono anche restituire "Continue") o finché l'elenco non viene esaurito.
-   Ignorare i filtri rimanenti e restituire l'azione dall'ultimo filtro valutato.

All'interno di un livello, l'arbitraggio dei filtri viene eseguito come segue:

-   Eseguire l'arbitraggio dei filtri a ogni livello secondario in ordine dalla priorità più alta alla priorità più bassa.
-   Valutare tutti i livelli secondari anche se un livello secondario con priorità più alta ha deciso di bloccare il traffico.
-   Restituire l'azione risultante in base alle regole dei criteri descritte nella sezione seguente.

Il diagramma seguente illustra una configurazione di sottoprogetto di esempio. Le caselle esterne rappresentano i livelli. Le caselle interne rappresentano i sotto-livelli che contengono filtri. Il carattere jolly ( \* ) in un filtro indica che tutto il traffico corrisponde al filtro.

![configurazione del livello secondario di esempio](images/fwp-sub-config2.png)

L'unico modo per ignorare un filtro è se un filtro con peso più elevato ha consentito o bloccato il traffico all'interno dello stesso sottostrato. Al contrario, un modo per garantire che un filtro veda sempre tutto il traffico all'interno di un livello è aggiungere un livello secondario che contiene un singolo filtro che corrisponde a tutto il traffico.

## <a name="configurable-override-policy"></a>Criteri di sostituzione configurabili

Le regole descritte di seguito regolano le decisioni di arbitrati all'interno di un livello. Queste regole vengono usate dal motore di filtro per decidere quale delle azioni del livello secondario viene applicata al traffico di rete.

I criteri di base sono i seguenti.

-   Le azioni vengono valutate in ordine di priorità dei livelli secondari dalla priorità più alta alla priorità più bassa.
-   "Block" esegue l'override di "Permit".
-   "Block" è finale (non può essere sottoposto a override) e arresta la valutazione. Il pacchetto viene eliminato.

I criteri di base non supportano lo scenario di un'eccezione non sottoposta a override da un firewall. Esempi tipici di questo tipo di scenario sono:

-   La porta di amministrazione remota deve essere aperta anche in presenza di un firewall di terze parti.
-   Componenti che richiedono l'apertura delle porte per il funzionamento ,ad esempio universal Plug and Play UPnP. Se l'amministratore ha abilitato in modo esplicito il componente, il firewall non deve bloccare automaticamente il traffico.

Per supportare gli scenari precedenti, una decisione di filtro deve essere resa più difficile da sostituire rispetto a un'altra decisione di filtro gestendo l'autorizzazione di override dell'azione. Questa autorizzazione viene implementata come flag **FWPS \_ RIGHT \_ ACTION \_ WRITE** e viene impostata in base al filtro.

L'algoritmo di valutazione mantiene l'azione corrente ("Permit" o "Block") insieme al flag **FWPS \_ RIGHT \_ ACTION \_ WRITE.** Il flag controlla se a un livello secondario con priorità inferiore è consentito eseguire l'override dell'azione. Impostando o reimpostando il flag **FWPS \_ RIGHT \_ ACTION \_ WRITE** nella struttura [FWPS \_ CLASSIFY \_ OUT0,](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) un provider regola il modo in cui le azioni possono o non possono essere sottoposte a override. Se il flag è impostato, indica che è possibile eseguire l'override dell'azione. Se il flag è assente, non è possibile eseguire l'override dell'azione.



| Azione | Consenti override (FWPS \_ RIGHT ACTION WRITE è \_ \_ impostato) | Descrizione                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Consenti | Sì                                                | Il traffico può essere bloccato a un altro livello secondario. Si tratta di un'autorizzazione soft.<br/>                            |
| Consenti | No                                                 | Il traffico può essere bloccato a un altro livello secondario solo da un callout **Veto**. Si tratta di un'autorizzazione hard.<br/> |
| Blocca  | Sì                                                | Il traffico può essere consentito a un altro livello secondario. Si tratta di un blocco soft.<br/>                           |
| Blocca  | No                                                 | Il traffico non può essere consentito a un altro livello secondario. Si tratta di un blocco rigido.<br/>                        |



 

L'azione di filtro può  essere impostata impostando il membro del tipo nella struttura [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) su **FWP \_ ACTION \_ BLOCK** o **FWP \_ ACTION \_ PERMIT.** Insieme al tipo di azione, un filtro espone anche il flag **FWPM \_ FILTER FLAG CLEAR ACTION \_ \_ \_ \_ RIGHT**. Se questo flag è deselezionato, il tipo di azione è rigido e non può essere sottoposto a override se non quando un'autorizzazione hard viene sostituita da un **veto** come spiegato più avanti, altrimenti è soft che può essere sostituito da un'azione con priorità alta.

La tabella seguente elenca il comportamento predefinito per le azioni filtro e callout.

| Azione         | Comportamento predefinito |
|----------------|------------------|
| Autorizzazione di filtro  | Autorizzazione soft      |
| Autorizzazione callout | Autorizzazione soft      |
| Blocco di filtri   | Blocco rigido       |
| Blocco callout  | Blocco soft       |



 

Un **veto** è un'azione "Blocca" restituita dal filtro quando il flag **FWPS \_ RIGHT ACTION \_ \_ WRITE** è stato reimpostato prima di chiamare il filtro. Un **veto blocderà** il traffico consentito con un permesso rigido.

Quando viene emesso un **veto,** è un'indicazione di conflitto nella configurazione. Per attenuare il conflitto, vengono eseguite le azioni seguenti.

-   Il traffico è bloccato.
-   Viene generato un evento di controllo.
-   Viene generata una notifica.
    > [!Note]  
    > La notifica viene ricevuta da tutte le entità che la hanno sottoscritta. Questo include in genere il firewall (per rilevare configurazioni erre) o le applicazioni (per rilevare se il filtro specifico viene sostituito).

     

    > [!Note]  
    > Non viene creata un'istanza obbligatoria dell'interfaccia utente quando viene eseguito l'override di un filtro "Hard Permit". Le notifiche dell'override vengono inviate a qualsiasi provider registrato per riceverle, che consente ai firewall o alle applicazioni che hanno creato i filtri "Consenti", di visualizzare l'interfaccia utente che richiede l'azione dell'utente. Non è necessario avere una notifica dell'interfaccia utente della piattaforma per questi eventi di override perché gli ISV del firewall che non vogliono bloccare in modo invisibile all'utente possono eseguire questa operazione registrando in una posizione diversa in WFP o (scelta meno preferita) gestire tutta la logica in un driver call-out. Gli ISV che ritieni che la richiesta di conferma agli utenti sia una buona idea vogliono essere proprietari dell'esperienza utente e creare la propria interfaccia utente.

     

Il comportamento di mitigazione descritto in precedenza garantisce che un filtro "Hard Permit" non venga sostituito automaticamente da un filtro "Blocca" e copre lo scenario in cui una porta di amministrazione remota non può essere bloccata dal firewall. Per eseguire l'override invisibile all'utente dei filtri "Hard Permit" un firewall deve aggiungere i filtri all'interno di un livello secondario con priorità più alta.

> [!Note]  
> Poiché non è presente alcun arbitraggio tra livelli, il traffico consentito con "Hard Permit" può comunque essere bloccato a un altro livello. È responsabilità dell'autore dei criteri assicurarsi che il traffico sia consentito a ogni livello, se necessario.

 

Le applicazioni utente che richiedono l'apertura delle porte aggiungono filtri sottoponibili a override a un livello secondario con priorità bassa. Il firewall può sottoscrivere gli eventi di notifica di aggiunta del filtro e aggiungere un filtro corrispondente dopo la convalida dell'utente (o dei criteri).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assegnazione di pesi dei filtri](filter-weight-assignment.md)
</dt> </dl>

 

