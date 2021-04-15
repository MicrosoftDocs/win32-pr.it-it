---
title: Procedure consigliate (piattaforma filtro Windows)
description: Nell'elenco seguente sono contenute le procedure consigliate per lo sviluppo di applicazioni tramite l'API Windows Filtering Platform (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517289"
---
# <a name="best-practices-windows-filtering-platform"></a>Procedure consigliate (piattaforma filtro Windows)

Nell'elenco seguente sono contenute le procedure consigliate per lo sviluppo di applicazioni tramite l'API Windows Filtering Platform (WFP).

-   Utilizzare sessioni dinamiche.

    Molte applicazioni aggiungono oggetti Criteri di filtro all'avvio, quindi eliminano questi oggetti in fase di arresto. Utilizzando una sessione dinamica, si garantisce che questi oggetti vengano eliminati anche in caso di arresto anomalo dell'applicazione. Inoltre, la semplice chiusura dell'handle del motore alla fase di arresto è più efficiente rispetto all'esecuzione di singole chiamate per eliminare ogni oggetto.

-   Gestire correttamente i timeout delle transazioni o impostare la sessione **txnWaitTimeoutInMSec** su infinite per impedire i timeout.

    Anche se non si utilizzano transazioni esplicite, la maggior parte delle chiamate viene comunque eseguita in una transazione implicita e pertanto può essere timeout.

-   Utilizzare transazioni esplicite per combinare operazioni di aggiunta o eliminazione correlate in una singola transazione.

    Questa operazione è più efficiente e semplifica la pulizia dei risultati parziali nei percorsi degli errori.

-   Utilizzare stringhe compatibili con MUI.

    Tutte le stringhe localizzabili sono archiviate in una struttura di dati comune: [**FWPM \_ Visualizza \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). Le stringhe all'interno di questa struttura possono essere stringhe indirette del tipo supportato da [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring). Prima che venga restituita una struttura **\_ \_ DATA0 per la visualizzazione FWPM** da parte delle funzioni, le stringhe indirette vengono risolte nella risorsa di stringa specificata utilizzando le impostazioni locali del chiamante.

-   Associare tutti gli oggetti a un provider.

    Quando più provider sono installati nel sistema, ciò rende più semplice per gli strumenti di diagnostica determinare chi ha aggiunto.

-   Aggiungere filtri al sottolivello personalizzato.

    Quando viene raggiunto un filtro di terminazione in un sottolivello, non vengono valutati altri filtri in quel sottolivello. Pertanto, se si aggiungono i filtri allo stesso sottolivello di un altro provider, è possibile impedire che vengano richiamati i filtri di altri, ottenendo risultati imprevisti.

-   Usare l'applicazione a livello di applicazione (ALE) anziché il filtro orientato ai pacchetti.

    Il filtro a livello di pacchetto è lento.

-   Filtrare gli errori ICMP e gli eventi RST prima che vengano generati.

    Questa operazione è più efficiente che filtra questi eventi dopo che sono stati generati.

-   Eseguire l'ispezione di pacchetti a livello di dati Stream/datagramma anziché a livello di trasporto.

    Questo vale per lo sviluppo di callout. Per ulteriori informazioni, vedere [considerazioni sulla programmazione dei driver di callout](/windows-hardware/drivers/network/callout-driver-programming-considerations) in Windows Driver Kit (WDK).

-   Prendere in considerazione le implicazioni sulle prestazioni quando si usano filtri complessi.

    A partire da Windows 7 e Windows Server 2008 R2, è possibile creare filtri con più condizioni che usano la stessa chiave di campo. In questo modo è possibile creare criteri complessi con un minor numero di filtri. Tuttavia, tali filtri complessi potrebbero comportare una riduzione delle prestazioni per la classificazione del motore di filtro WFP. È necessario eseguire una valutazione per determinare se l'utilizzo di tali filtri causa un effetto negativo sulle prestazioni complessive della soluzione.

 

 
