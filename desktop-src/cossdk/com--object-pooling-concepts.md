---
description: Il pool di oggetti è un servizio automatico fornito da COM+ che consente di configurare un componente in modo che le istanze di se stesso siano mantenute attive in un pool, pronte per essere usate da qualsiasi client che richiede il componente.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Concetti relativi al pool di oggetti COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836dd6f29c2f0bd120843a1a93763d46cb51224966f255251f7e3bfb4c7fa66a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129143"
---
# <a name="com-object-pooling-concepts"></a>Concetti relativi al pool di oggetti COM+

Il pool di oggetti è un servizio automatico fornito da COM+ che consente di configurare un componente in modo che le istanze di se stesso siano mantenute attive in un pool, pronte per essere usate da qualsiasi client che richiede il componente. È possibile configurare e monitorare a livello amministrativo il pool gestito per un determinato componente, specificando caratteristiche quali le dimensioni del pool e i valori di timeout della richiesta di creazione. Quando l'applicazione è in esecuzione, COM+ gestisce automaticamente il pool, gestendo i dettagli dell'attivazione e del riutilizzo degli oggetti in base ai criteri specificati.

È possibile ottenere prestazioni molto significative e vantaggi di ridimensionamento riutilizzando gli oggetti in questo modo, in particolare quando vengono scritti per sfruttare al meglio il riutilizzo. Con il pooling di oggetti si ottengono i vantaggi seguenti:

-   È possibile velocizzare il tempo di utilizzo degli oggetti per ogni client, effettuando il factoring dell'inizializzazione e dell'acquisizione delle risorse che richiedono molto tempo dal lavoro effettivo eseguito dall'oggetto per i client.
-   È possibile condividere il costo dell'acquisizione di risorse costose tra tutti i client.
-   È possibile preallocare gli oggetti all'avvio dell'applicazione, prima dell'arrivo di qualsiasi richiesta client.
-   È possibile gestire l'uso delle risorse con la gestione del pool amministrativo, ad esempio impostando un livello di pool massimo appropriato, è possibile mantenere aperte solo tutte le connessioni di database per cui si dispone di una licenza.
-   È possibile configurare il pooling a livello amministrativo per sfruttare al meglio le risorse hardware disponibili, è possibile modificare facilmente la configurazione del pool quando cambiano le risorse hardware disponibili.
-   È possibile velocizzare il tempo di riattivazione per gli oggetti che usano l'attivazione [JIT ( Just-In-Time),](com--just-in-time-activation.md)controllando intenzionalmente come le risorse vengono dedicate ai client.

## <a name="writing-poolable-objects"></a>Scrittura di oggetti in pool

Gli oggetti in pool devono soddisfare determinati requisiti per consentire l'uso di una singola istanza di oggetto da parte di più client. Ad esempio, non possono contenere lo stato client o avere affinità di thread. Anche gli oggetti transazionali hanno requisiti specifici, in modo che le risorse gestite mantenute da un oggetto in pool devono essere integrate manualmente in una transazione.

Gli oggetti in pool possono implementare [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) per controllare come vengono riutilizzati. Ciò consente loro di eseguire l'inizializzazione quando sono attivati in un determinato contesto, di pulire qualsiasi stato client in fase di disattivazione e di indicare quando sono in uno stato non riutilizzabile.

Spesso è utile scrivere oggetti in pool in modo piuttosto generico in modo che possano essere personalizzati a livello amministrativo con una stringa del costruttore. Ad esempio, un oggetto potrebbe essere scritto per contenere una connessione ODBC generica, con un DSN specifico specificato a livello amministrativo in una stringa del costruttore.

Negli argomenti di questa sezione, descritti nella tabella seguente, vengono fornite informazioni sul funzionamento del pool di oggetti in COM+, oltre a informazioni su come scrivere, configurare e implementare oggetti in pool.



| Argomento                                                                                                 | Descrizione                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Funzionamento del pool di oggetti](how-object-pooling-works.md)<br/>                                   | Presenta i concetti di base.<br/>                                                                      |
| [Miglioramento delle prestazioni con il pool di oggetti](improving-performance-with-object-pooling.md)<br/> | Fornisce dettagli specifici su come usare il pool di oggetti in modo più efficace.<br/>                 |
| [Requisiti per gli oggetti in pool](requirements-for-poolable-objects.md)<br/>                 | Fornisce informazioni dettagliate su come scrivere un oggetto di cui eseguire il pool.<br/>                              |
| [Pooling di oggetti transazionali](pooling-transactional-objects.md)<br/>                         | Fornisce informazioni dettagliate sui requisiti speciali applicabili agli oggetti transazionali in pool.<br/> |
| [Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)<br/>         | Descrive come possono essere implementati gli oggetti in pool per controllare il modo in cui vengono riutilizzati.<br/>               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività del pool di oggetti COM+](com--object-pooling-tasks.md)
</dt> </dl>

 

 




