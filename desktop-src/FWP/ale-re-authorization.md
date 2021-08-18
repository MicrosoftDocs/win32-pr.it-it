---
title: Riautorizzazione ALE
description: Il traffico di rete ai livelli Application Layer Enforcement (ALE) di Windows Filtering Platform (WFP) viene filtrato in base ai flussi ALE.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850cd7f789c1fb1222a0d6820e84a42cf41763dac4e57b96667e7feda364374c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582691"
---
# <a name="ale-reauthorization"></a>Riautorizzazione ALE

Il traffico di rete ai livelli Application Layer Enforcement (ALE) di Windows Filtering Platform (WFP) viene filtrato in base ai [flussi ALE.](ale-stateful-filtering.md) Dopo aver consentito un flusso ALE, tutto il traffico che fa parte del flusso ALE è consentito. La riautorizzazione è una richiesta per convalidare le autorizzazioni del flusso ALE, in genere a causa di una modifica dei criteri di rete.

Ai flussi ALE viene assegnata una direzione, in ingresso o in uscita, in base alla direzione del primo pacchetto che ha attivato la creazione e l'autorizzazione del flusso. I flussi ALE in ingresso vengono creati e autorizzati al livello [**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}.**](management-filtering-layer-identifiers-.md) I flussi ALE in uscita vengono creati e autorizzati al livello **FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}.** La direzione del flusso ALE non limita la direzione dei pacchetti che appartengono al flusso. I flussi ALE contengono pacchetti sia in ingresso che in uscita indipendentemente dalla direzione del flusso ALE stesso.

La riautorizzazione di un flusso ALE viene attivata da:

-   Modifica dei criteri nel livello in cui il flusso ALE è stato originariamente autorizzato o creato.
-   Interfaccia di arrivo diversa dall'interfaccia in cui il flusso ALE è stato originariamente autorizzato o creato.
-   Connessione in sospeso.

La riautorizzazione si distingue dall'autorizzazione iniziale in base alla presenza del flag [**FWP \_ CONDITION FLAG IS \_ \_ \_ REAUTHORIZE.**](filtering-condition-flags-.md)

La riautorizzazione può essere completata solo ai livelli [**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) e **FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}.**

### <a name="policy-change-reauthorization"></a>Riautorizzazione delle modifiche dei criteri

Una modifica dei criteri viene implementata come aggiunta o rimozione di filtri a un livello ALE. Dopo aver rilevato una modifica dei criteri, il primo pacchetto che attraversa un flusso ALE creato al livello interessato verrà specificato per la nuova autorizzazione al livello. Pertanto, per la riautorizzazione è possibile che un pacchetto in uscita sia classificato al livello [**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) e che un pacchetto in ingresso sia classificato al livello **FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}.**

Uno dei motivi di questa classificazione in direzione mista è che potrebbe non esserci altro traffico di rete dalla direzione originale (ad esempio, un pacchetto in ingresso per il flusso ALE in ingresso). Un esempio di questo tipo è lo streaming UDP unidirettico dopo un handshake bidirettico iniziale. In questo caso è più opportuno disassurare lo streaming il prima possibile.

### <a name="arrival-interface-reauthorization"></a>Riautorizzazione dell'interfaccia di arrivo

La riautorizzazione dell'interfaccia arrival è disponibile a partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

I pacchetti appartenenti allo stesso flusso ALE possono arrivare da più interfacce. Il primo pacchetto che viene ricevuto tramite un'interfaccia diversa dall'interfaccia originale del flusso ALE viene riautorizzato.

In un modello di host sicuro, che è il modello di sicurezza predefinito per lo stack TCP/IP, una connessione in un'interfaccia di rete accetta solo i pacchetti presenti nella stessa interfaccia. Di conseguenza, la riautorizzazione dell'interfaccia di arrivo non viene usata in un computer host sicuro.

In un modello di host debole, una connessione su un'interfaccia di rete consente l'ingresso di pacchetti in qualsiasi altra interfaccia di rete. La riautorizzazione dell'interfaccia arrival viene usata in un computer host debole per implementare criteri specifici dell'interfaccia. Per altre informazioni, vedere ["The Cable Guy: Strong and Weak Host Models".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Alcuni [campi classificabili potrebbero](filtering-conditions.md) essere sconosciuti durante la riautorizzazione. Ad esempio, se un pacchetto in uscita viene riautorizzato al livello [**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6},**](management-filtering-layer-identifiers-.md) tutti i campi relativi all'interfaccia di arrivo sono sconosciuti. In tal caso, i valori dei campi sconosciuti vengono indicati come [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)

I campi di [**tipo FWP \_ EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) possono essere associati a [**FWP \_ MATCH \_ EQUAL.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) Pertanto, è possibile impostare un criterio per bloccare le riautorizzazioni ed eseguire l'applicazione di un flusso ALE all'arrivo delle richieste di riautorizzazione per il flusso ALE.

## <a name="pending-connection-reauthorization"></a>Riautorizzazione della connessione in sospeso

Un driver callout può posticipare un'operazione di classificazione ai livelli ALE e completarla in un secondo momento, quando la decisione di filtro può essere presa in modo sicuro. La funzionalità posticipata/completa di ALE è supportata tramite le funzioni in modalità kernel [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) e [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).

La riautorizzazione viene attivata immediatamente dopo la chiamata FwpsCompleteOperation0 e consente al driver del callout di consentire o bloccare il flusso.

Solo un'autorizzazione iniziale può essere posticipata. Una chiamata a FwpsPendOperation0 avrà esito negativo se è impostato il flag [**FWP \_ CONDITION FLAG IS \_ \_ \_ REAUTHORIZE.**](filtering-condition-flags-.md)

Per altre informazioni, vedere la documentazione [Windows Driver Kit.](/windows-hardware/drivers/ddi/_netvista/)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione a livello di applicazione (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Traffico multicast/broadcast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Personalizzazione Flow ale](ale-flow-customization.md)
</dt> </dl>

 

 