---
description: Uso di COM+ CRM in un ambiente cluster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Uso di COM+ CRM in un ambiente cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a2d0800f98c9453e7d4454cdd59185dffb837649e391ebc415c965bee6ff80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499531"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Uso di COM+ CRM in un ambiente cluster

Quando si sviluppano CPM COM+ da usare in ambienti cluster, il fattore principale da considerare è se un CRM specifico si occupa del nodo del cluster su cui opera. Ad esempio, se la risorsa gestita da CRM è l'file system o il Registro di sistema del computer, eventuali modifiche sono specifiche del nodo in cui è in esecuzione l'applicazione server CRM al momento. In questo caso, non è consigliabile eseguire il failover dell'applicazione server CRM in un altro nodo. In un caso diverso, in cui crm gestisce alcune risorse comuni al cluster, è utile eseguire il failover dell'applicazione server CRM in un altro nodo.

Il percorso di directory predefinito per i file di log crm è la stessa directory del file di log DTC. Nei cluster il file di log DTC viene inserito in un disco condiviso di cui viene effettuato il failover tra i nodi del cluster. Ciò significa che il comportamento predefinito per le applicazioni server CRM è il failover tra i nodi del cluster. Pertanto, se un SISTEMA CRM specifico richiede il comportamento alternativo di non eseguire il failover tra i nodi, è necessario modificare il percorso del file di log CRM per quella particolare applicazione server CRM.

Inoltre, se il failover è necessario per l'applicazione CRM, deve essere configurato come applicazione generica in un gruppo di cluster. La dipendenza deve essere DTC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alla Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



