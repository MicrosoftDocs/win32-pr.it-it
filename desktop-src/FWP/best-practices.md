---
title: Procedure consigliate (Windows Filtering Platform)
description: L'elenco seguente contiene le procedure consigliate per lo sviluppo di applicazioni usando l'API Windows Filtering Platform (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0ddb6038a9fe43070f1c16e545dbd7ac8929f3363fc88556aac391428175ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069461"
---
# <a name="best-practices-windows-filtering-platform"></a>Procedure consigliate (Windows Filtering Platform)

L'elenco seguente contiene le procedure consigliate per lo sviluppo di applicazioni usando l'API Windows Filtering Platform (WFP).

-   Usare sessioni dinamiche.

    Molte applicazioni aggiungono oggetti criteri di filtro all'avvio e quindi eliminano questi oggetti in fase di arresto. Usando una sessione dinamica, si garantisce che questi oggetti siano eliminati anche se l'applicazione si arresta in modo anomalo. Inoltre, la semplice chiusura dell'handle del motore in fase di arresto è più efficiente rispetto all'esecuzione di singole chiamate per eliminare ogni oggetto.

-   Gestire correttamente i timeout delle transazioni o impostare la sessione **txnWaitTimeoutInMSec** su infinito per evitare timeout.

    Anche se non si usano transazioni esplicite, la maggior parte delle chiamate viene comunque eseguita in una transazione implicita e pertanto può verificarsi un timeout.

-   Usare transazioni esplicite per combinare operazioni di aggiunta o eliminazione correlate in una singola transazione.

    Questo è più efficiente e semplifica la pulizia dei risultati parziali nei percorsi di errore.

-   Usare stringhe conformi a MUI.

    Tutte le stringhe localizzabili vengono archiviate in una struttura di dati comune: [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). Le stringhe all'interno di questa struttura possono essere stringhe indirette del tipo supportato [**da SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring). Prima che **una struttura \_ DISPLAY \_ DATA0 FWPM** venga restituita da una delle funzioni, le stringhe indirette vengono risolte nella risorsa stringa specificata usando le impostazioni locali del chiamante.

-   Associare tutti gli oggetti a un provider.

    Quando nel sistema sono installati più provider, è più semplice per gli strumenti di diagnostica determinare chi ha aggiunto l'elemento.

-   Aggiungere filtri al proprio sottolivente.

    Quando viene raggiunto un filtro di terminazione in un sottolivelli, non vengono valutati altri filtri in tale sottolivente. Di conseguenza, se si aggiungono i filtri allo stesso sottolivelli di un altro provider, è possibile impedire la chiamata dei filtri reciproci, con risultati imprevisti.

-   Usare l'imposizione del livello applicazione anziché il filtro orientato ai pacchetti.

    Il filtro a livello di pacchetto è lento.

-   Filtrare gli errori ICMP e gli eventi RST prima che siano generati.

    Si tratta di un'operazione più efficiente che consente di filtrare questi eventi dopo che sono stati generati.

-   Eseguire l'ispezione dei pacchetti a livello di dati di flusso/datagramma anziché a livello di trasporto.

    Questo vale per lo sviluppo di callout. Per altre informazioni, vedere [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in Windows Driver Kit (WDK).

-   Prendere in considerazione le implicazioni relative alle prestazioni quando si usano filtri complessi.

    A partire Windows 7 e Windows Server 2008 R2, è possibile creare filtri con più condizioni che usano la stessa chiave di campo. In questo modo è possibile creare criteri complessi con un minor numero di filtri. Tuttavia, tali filtri complessi potrebbero avere prestazioni più lente per la classificazione del motore di filtro WFP. È necessario eseguire una valutazione per determinare se l'uso di tali filtri causa un effetto negativo sulle prestazioni complessive della soluzione.

 

 
