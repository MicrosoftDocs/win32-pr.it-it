---
title: Arbitraggio di filtro
description: L'arbitraggio di filtro è la logica incorporata in Windows Filtering Platform (WFP) che viene usata per determinare il modo in cui i filtri interagiscono tra loro durante le decisioni di filtro del traffico di rete.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd7df778d1c24b7480de3321e7a1ec126d8e642
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727007"
---
# <a name="filter-arbitration"></a>Arbitraggio di filtro

L'arbitraggio di filtro è la logica incorporata in Windows Filtering Platform (WFP) che viene usata per determinare il modo in cui i filtri interagiscono tra loro durante le decisioni di filtro del traffico di rete.

## <a name="filter-arbitration-behaviors"></a>Filtrare i comportamenti degli arbitri

I comportamenti seguenti caratterizzano il sistema di arbitraggio del filtro:

-   Tutto il traffico può essere controllato. Nessun traffico può ignorare i filtri a un livello specificato.
-   Il traffico può essere bloccato da un filtro di callout tramite un **veto** anche se è stato consentito da un filtro con priorità superiore.
-   Più provider possono ispezionare il traffico allo stesso livello. Ad esempio, il firewall seguito da filtri di sistema di rilevamento delle intrusioni (ID) o IPsec seguito da filtri di qualità del servizio (QoS) può esaminare il traffico sullo stesso livello.

## <a name="filtering-model"></a>Modello di filtro

Ogni livello di filtro è diviso in sottolivelli ordinati per priorità (detto anche peso). Il traffico di rete attraversa i livelli secondari dalla priorità più alta alla priorità più bassa. I sottolivelli vengono creati e gestiti dagli sviluppatori che usano l'API Pam.

All'interno di ogni sottolivello, i filtri vengono ordinati in base al peso. Il traffico di rete è indicato per i filtri corrispondenti dal peso più alto a quello più basso.

L'algoritmo di arbitraggio del filtro viene applicato a tutti i livelli secondari all'interno di un livello e la decisione di filtro finale viene eseguita dopo la valutazione di tutti i sottolivelli. Questo consente di individuare più funzionalità di corrispondenza.

All'interno di un sottolivello, l'arbitraggio di filtro viene eseguito come segue:

-   Consente di calcolare l'elenco dei filtri corrispondenti ordinati in base al peso, dal più alto al più basso.
-   Valutare i filtri corrispondenti in ordine fino a quando non viene restituito un "permesso" o un "blocco" (i filtri possono anche restituire "continua") o fino a quando l'elenco non è esaurito.
-   Ignorare i filtri rimanenti e restituire l'azione dall'ultimo filtro valutato.

All'interno di un livello, l'arbitraggio di filtro viene eseguito come segue:

-   Eseguire l'arbitraggio di filtro a ogni sottolivello in ordine dalla priorità più alta alla priorità più bassa.
-   Valutare tutti i sottolivelli anche se un sottolivello con priorità più alta ha deciso di bloccare il traffico.
-   Restituisce l'azione risultante in base alle regole dei criteri descritte nella sezione seguente.

Il diagramma seguente illustra una configurazione di livello secondario di esempio. Le caselle esterne rappresentano i livelli. Le caselle interne rappresentano i sottolivelli che contengono filtri. Il carattere jolly ( \* ) in un filtro indica che tutto il traffico corrisponde al filtro.

![configurazione del sottolivello di esempio](images/fwp-sub-config2.png)

L'unico modo per ignorare un filtro è se un filtro di peso superiore ha consentito o bloccato il traffico all'interno dello stesso sottolivello. Viceversa, un modo per garantire che un filtro veda sempre tutto il traffico all'interno di un livello consiste nell'aggiungere un sottolivello che contiene un singolo filtro che corrisponde a tutto il traffico.

## <a name="configurable-override-policy"></a>Criteri di sostituzione configurabili

Le regole descritte di seguito regolano le decisioni di arbitraggio all'interno di un livello. Queste regole vengono usate dal motore di filtro per decidere quale una delle azioni del sottolivello viene applicata al traffico di rete.

Il criterio di base è il seguente.

-   Le azioni vengono valutate in ordine di priorità dei sottolivelli dalla priorità più alta alla priorità più bassa.
-   "Blocco" esegue l'override di "Consenti".
-   "Blocco" è finale (non può essere sottoposto a override) e arresta la valutazione. Il pacchetto viene eliminato.

Il criterio di base non supporta lo scenario di un'eccezione non sottoposta a override da un firewall. Esempi tipici di questo tipo di scenario sono:

-   Porta di amministrazione remota necessaria per l'apertura anche in presenza di un firewall di terze parti.
-   Componenti che richiedono l'apertura di porte per funzionare, ad esempio Universal Plug and Play UPnP). Se l'amministratore ha abilitato in modo esplicito il componente, il firewall non deve bloccare automaticamente il traffico.

Per supportare gli scenari precedenti, una decisione di filtro deve essere resa più difficile da ignorare rispetto a un'altra decisione di filtro gestendo l'autorizzazione per l'override dell'azione. Questa autorizzazione viene implementata come flag **FWPS \_ right \_ Action \_ Write** e viene impostata in base al filtro.

L'algoritmo di valutazione gestisce l'azione corrente ("Consenti" o "blocco") insieme al flag di **\_ \_ \_ scrittura azione a destra FWPS** . Il flag controlla se un sottolivello con priorità inferiore è autorizzato a eseguire l'override dell'azione. Impostando o reimpostando il flag di **\_ \_ \_ scrittura dell'azione right FWPS** nella struttura [FWPS \_ classifica \_ OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) , un provider determina il modo in cui le azioni possono o non possono essere sottoposte a override. Se il flag è impostato, indica che l'azione può essere sottoposta a override. Se il flag è assente, l'azione non può essere sottoposta a override.



| Azione | Consenti override (FWPS \_ right \_ Action \_ Write è impostato) | Descrizione                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Consenti | Sì                                                | Il traffico può essere bloccato a un altro sottolivello. Questo è un permesso soft.<br/>                            |
| Consenti | No                                                 | Il traffico può essere bloccato a un altro sottolivello solo da un **veto** di callout. Questa operazione è detta autorizzazione rigida.<br/> |
| Blocca  | Sì                                                | Il traffico può essere consentito a un altro sottolivello. Questa operazione è denominata blocco soft.<br/>                           |
| Blocca  | No                                                 | Il traffico non può essere consentito a un altro sottolivello. Questa operazione è denominata blocco rigido.<br/>                        |



 

L'azione di filtro può essere impostata impostando il membro del **tipo** nella struttura [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) su **FWP \_ Action \_ Block** o **FWP \_ Action \_ permessi**. Insieme al tipo di azione, un filtro espone anche il flag **del \_ filtro FWPM flag \_ \_ Clear \_ Action \_ right**. Se questo flag è deselezionato, il tipo di azione è rigido e non è possibile eseguirne l'override tranne quando un permesso rigido viene sostituito da un **veto** , come illustrato più avanti, altrimenti è soft, che può essere sostituito da un'azione con priorità alta.

Nella tabella seguente viene elencato il comportamento predefinito per le azioni di filtro e di callout.

| Azione         | Comportamento predefinito |
|----------------|------------------|
| Consenti filtro  | Permesso soft      |
| Consenti callout | Permesso soft      |
| Blocca filtro   | Blocco rigido       |
| Blocco callout  | Blocco flessibile       |



 

Un **veto** è un'azione "blocco" restituita dal filtro quando il flag **FWPS \_ right \_ Action \_ Write** è stato reimpostato prima di chiamare il filtro. Un **veto** bloccherà il traffico consentito con un permesso fisso.

Quando viene emesso un **veto** , si tratta di un'indicazione del conflitto nella configurazione. Per attenuare il conflitto, vengono eseguite le azioni seguenti.

-   Il traffico è bloccato.
-   Viene generato un evento di controllo.
-   Viene generata una notifica.
    > [!Note]  
    > La notifica viene ricevuta da tutte le entità che lo hanno sottoscritto. Questo include in genere il firewall (per rilevare le configurazioni errate) o le applicazioni (per rilevare se è stato eseguito l'override del relativo filtro specifico).

     

    > [!Note]  
    > Non è stata creata un'istanza dell'interfaccia utente obbligatoria quando viene eseguito l'override di un filtro "permesso rigido". Le notifiche della sostituzione vengono inviate a qualsiasi provider registrato per riceverli, che consente ai firewall o alle applicazioni che hanno creato i filtri "Consenti", di visualizzare l'interfaccia utente che richiede l'intervento dell'utente. Non esiste alcun valore nella presenza di una notifica dell'interfaccia utente della piattaforma per questi eventi di override, dal momento che gli ISV del firewall che non vogliono bloccarsi in modo invisibile possono eseguire questa operazione registrandosi in una posizione diversa in WFP o (meno preferibile) gestire tutta la logica in un driver di chiamata. Gli ISV che pensano di richiedere agli utenti è una scelta ottimale per l'esperienza utente e per creare la propria interfaccia utente.

     

Il comportamento di mitigazione descritto in precedenza garantisce che un filtro "blocco rigido" non venga sottoposto a override automaticamente da un filtro "blocco" e copra lo scenario in cui una porta di amministrazione remota non può essere bloccata dal firewall. Per eseguire l'override invisibile all'utente dei filtri "hard", un firewall deve aggiungere i filtri all'interno di un sottolivello con priorità più alta.

> [!Note]  
> Poiché non è presente alcun arbitraggio tra livelli, il traffico consentito con "permesso fisso" può essere ancora bloccato a un altro livello. Se necessario, è responsabilità dell'autore del criterio garantire che il traffico sia consentito a ogni livello.

 

Le applicazioni utente che richiedono porte da aprire aggiungono filtri sottoponibili a override a un sottolivello con priorità bassa. Il firewall può sottoscrivere gli eventi di notifica del filtro e aggiungere un filtro corrispondente dopo la convalida dell'utente (o dei criteri).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assegnazione di pesi dei filtri](filter-weight-assignment.md)
</dt> </dl>

 

