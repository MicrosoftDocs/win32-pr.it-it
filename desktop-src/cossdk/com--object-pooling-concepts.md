---
description: Il pool di oggetti è un servizio automatico fornito da COM+ che consente di configurare un componente in modo che le istanze di siano mantenute attive in un pool, pronte per essere utilizzate da qualsiasi client che richiede il componente.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Concetti relativi al pool di oggetti COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb2aa6481b2493371801d0d274420d356b0a32e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401406"
---
# <a name="com-object-pooling-concepts"></a>Concetti relativi al pool di oggetti COM+

Il pool di oggetti è un servizio automatico fornito da COM+ che consente di configurare un componente in modo che le istanze di siano mantenute attive in un pool, pronte per essere utilizzate da qualsiasi client che richiede il componente. È possibile configurare e monitorare in modo amministrativo il pool mantenuto per un determinato componente, specificando caratteristiche quali le dimensioni del pool e i valori di timeout delle richieste di creazione. Quando l'applicazione è in esecuzione, COM+ gestisce automaticamente il pool, gestendo i dettagli di attivazione e riutilizzo degli oggetti in base ai criteri specificati.

È possibile ottenere vantaggi molto significativi in termini di prestazioni e scalabilità riutilizzando gli oggetti in questo modo, in particolare quando vengono scritti per sfruttare appieno il riutilizzo. Con il pool di oggetti si ottengono i vantaggi seguenti:

-   È possibile velocizzare il tempo di utilizzo dell'oggetto per ogni client, fattorizzando l'inizializzazione dispendiosa in termini di tempo e l'acquisizione di risorse dal lavoro effettivo eseguito dall'oggetto per i client.
-   È possibile condividere i costi di acquisizione di risorse costose in tutti i client.
-   È possibile pre-allocare gli oggetti all'avvio dell'applicazione, prima che vengano richieste richieste client.
-   È possibile governare l'uso delle risorse con la gestione dei pool amministrativi, ad esempio, impostando un livello di pool massimo appropriato, è possibile aprire solo il numero di connessioni di database disponibili per la licenza.
-   È possibile configurare in modo amministrativo il pool per sfruttare al meglio le risorse hardware disponibili. è possibile modificare facilmente la configurazione del pool in quanto le risorse hardware disponibili cambiano.
-   È possibile velocizzare la riattivazione per gli oggetti che usano l' [attivazione JIT (just-in-Time)](com--just-in-time-activation.md), controllando deliberatamente il modo in cui le risorse sono dedicate ai client.

## <a name="writing-poolable-objects"></a>Scrittura di oggetti pool

Gli oggetti configurabili devono soddisfare determinati requisiti per consentire l'uso di una singola istanza di oggetto da parte di più client. Ad esempio, non possono contenere lo stato del client o avere affinità di thread. Gli oggetti transazionali presentano anche requisiti specifici, in quanto le risorse gestite da un oggetto in pool devono essere integrate manualmente in una transazione.

Gli oggetti in pool possono implementare [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) per controllare il modo in cui vengono riutilizzati. In questo modo è possibile eseguire l'inizializzazione quando viene attivato in un determinato contesto, per eliminare qualsiasi stato del client in fase di disattivazione e per indicare quando si trovano in uno stato non riutilizzabile.

Spesso è utile scrivere oggetti in pool in modo generico, in modo che possano essere personalizzati in modo amministrativo con una stringa del costruttore. È possibile, ad esempio, che un oggetto venga scritto in modo da contenere una connessione ODBC generica con un determinato DSN amministrativo specificato in una stringa del costruttore.

Negli argomenti di questa sezione, descritti nella tabella seguente, vengono fornite informazioni sul funzionamento del pool di oggetti in COM+, oltre a informazioni su come scrivere, configurare e implementare oggetti pool.



| Argomento                                                                                                 | Descrizione                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Funzionamento del pool di oggetti](how-object-pooling-works.md)<br/>                                   | Vengono presentati i concetti di base.<br/>                                                                      |
| [Miglioramento delle prestazioni con il pool di oggetti](improving-performance-with-object-pooling.md)<br/> | Fornisce dettagli specifici su come è possibile utilizzare il pool di oggetti in modo più efficace.<br/>                 |
| [Requisiti per gli oggetti pool](requirements-for-poolable-objects.md)<br/>                 | Fornisce informazioni dettagliate su come scrivere un oggetto da raggruppare.<br/>                              |
| [Raggruppamento di oggetti transazionali](pooling-transactional-objects.md)<br/>                         | Fornisce informazioni dettagliate sui requisiti speciali che si applicano agli oggetti transazionali in pool.<br/> |
| [Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)<br/>         | Descrive il modo in cui gli oggetti in pool possono essere implementati per controllare il modo in cui vengono riutilizzati.<br/>               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività del pool di oggetti COM+](com--object-pooling-tasks.md)
</dt> </dl>

 

 




