---
title: Riautorizzazione ALE
description: Il traffico di rete a livello di imposizione dell'applicazione (ALE) di Windows Filtering Platform (PAM) viene filtrato in base ai flussi ALE.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05c4c0767d449ec128250f852c365455bd0dc7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727010"
---
# <a name="ale-reauthorization"></a>Riautorizzazione ALE

Il traffico di rete a livello di imposizione dell'applicazione (ALE) di Windows Filtering Platform (PAM) viene filtrato in base ai [flussi ale](ale-stateful-filtering.md). Una volta che è stato consentito un flusso di ALE, tutto il traffico che fa parte del flusso ALE è consentito. La riautorizzazione è una richiesta di convalida delle autorizzazioni del flusso di ALE, in genere a causa di una modifica dei criteri di rete.

Ai flussi ALE viene assegnata una direzione, in ingresso o in uscita, in base alla direzione del primo pacchetto che ha attivato la creazione e l'autorizzazione del flusso. I flussi ALE in ingresso vengono creati e autorizzati al livello [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) . I flussi ALE in uscita vengono creati e autorizzati a livello di **FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}** . La direzione del flusso ALE non limita la direzione dei pacchetti che appartengono al flusso. I flussi ALE contengono sia i pacchetti in ingresso che quelli in uscita, indipendentemente dalla direzione del flusso ALE.

La riautorizzazione di un flusso di ALE viene attivata da:

-   Una modifica ai criteri nel livello in cui il flusso ALE è stato originariamente autorizzato o creato.
-   Interfaccia di arrivo diversa dall'interfaccia in cui il flusso ALE è stato originariamente autorizzato o creato.
-   Una connessione in sospeso.

La riautorizzazione si distingue dall'autorizzazione iniziale perché la presenza del flag di [**\_ condizione FWP \_ è \_ la \_ Riautorizzazione**](filtering-condition-flags-.md) del flag.

La riautorizzazione può essere eseguita solo a [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) e **FWPM \_ Layer \_ ale \_ auth \_ Connect \_ v {4 \| 6}** livelli.

### <a name="policy-change-reauthorization"></a>Criteri-modifica Riautorizzazione

Una modifica del criterio viene implementata come aggiunta o rimozione di un filtro a livello di ALE. Una volta rilevata una modifica ai criteri, il primo pacchetto che attraversa un flusso di ALE creato al livello interessato verrà specificato per la riautorizzazione al livello. Per la riautorizzazione è pertanto possibile che un pacchetto in uscita sia Classificato al livello [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) e che un pacchetto in ingresso sia Classificato al livello **FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}** .

Un motivo per questa classificazione a direzione mista è che potrebbe non essere disponibile un ulteriore traffico di rete dalla direzione originale (ad esempio, il pacchetto in ingresso per il flusso di ALE in ingresso). Uno di questi esempi è un flusso UDP unidirezionale dopo un handshake bidirezionale iniziale. In questo caso è preferibile chiudere il flusso il prima possibile.

### <a name="arrival-interface-reauthorization"></a>Riautorizzazione dell'interfaccia di arrivo

La riautorizzazione dell'interfaccia di arrivo è disponibile a partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

I pacchetti appartenenti allo stesso flusso di ALE possono arrivare da più interfacce. Il primo pacchetto da passare a un'interfaccia diversa dall'interfaccia originale del flusso di ALE viene riautorizzato.

In un modello host sicuro, che è il modello di sicurezza predefinito per lo stack TCP/IP, una connessione su un'interfaccia di rete accetta solo i pacchetti presenti nella stessa interfaccia. Quindi, la riautorizzazione dell'interfaccia di arrivo non viene usata in un computer host sicuro.

In un modello host vulnerabile, una connessione su un'interfaccia di rete consente l'ingresso di pacchetti in qualsiasi altra interfaccia di rete. La riautorizzazione dell'interfaccia di arrivo viene usata in un computer host debole per implementare criteri specifici dell'interfaccia. Per ulteriori informazioni, vedere ["The Cable Guy: Strong and vulnerabili host Models".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Alcuni [campi classificabili](filtering-conditions.md) potrebbero essere sconosciuti durante la riautorizzazione. Se, ad esempio, un pacchetto in uscita viene riautorizzato al livello [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , tutti i campi relativi all'interfaccia di arrivo sono sconosciuti. In tal caso, i valori dei campi sconosciuti vengono indicati come [**FWP \_ vuoti**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

È possibile trovare una corrispondenza tra i campi di tipo [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) e [**FWP \_ \_**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type). È quindi possibile impostare un criterio in modo da bloccare le riautorizzazioni ed eliminare un flusso ALE al momento dell'arrivo delle richieste di Riautorizzazione per il flusso ALE.

## <a name="pending-connection-reauthorization"></a>Riautorizzazione della connessione in sospeso

Un driver di callout può posticipare un'operazione di classificazione a livelli ALE e completarla in un secondo momento, quando la decisione di filtro può essere effettuata in modo sicuro. La funzionalità di rimandare/completare ALE è supportata tramite le funzioni in modalità kernel [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) e [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).

La riautorizzazione viene attivata immediatamente dopo la chiamata a FwpsCompleteOperation0 e consente al driver di callout di consentire o bloccare il flusso.

Solo un'autorizzazione iniziale può essere posticipata. Una chiamata a FwpsPendOperation0 avrà esito negativo se il [**\_ flag di condizione FWP \_ \_ è \_ reautorizzazione**](filtering-condition-flags-.md) flag è impostato.

Per ulteriori informazioni, vedere la documentazione di [Windows Driver Kit](/windows-hardware/drivers/ddi/_netvista/) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Application Layer Enforcement (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Traffico di broadcast/multicast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Personalizzazione del flusso di ALE](ale-flow-customization.md)
</dt> </dl>

 

 