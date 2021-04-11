---
description: Utilizzo di COM+ CRM in un ambiente cluster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Utilizzo di COM+ CRM in un ambiente cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342241"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Utilizzo di COM+ CRM in un ambiente cluster

Quando si sviluppano COM+ dispongono per lavorare negli ambienti cluster, il fattore principale da considerare è se un CRM specifico è interessato da quale nodo del cluster sta operando. Ad esempio, se la risorsa gestita da CRM è il computer file system o il registro di sistema, tutte le modifiche sono specifiche del nodo in cui è in esecuzione l'applicazione del server CRM. In questo caso, non è consigliabile eseguire il failover dell'applicazione server CRM in un altro nodo. In un caso diverso, in cui il CRM gestisce alcune risorse comuni al cluster, è utile eseguire il failover dell'applicazione server CRM in un altro nodo.

Il percorso predefinito della directory per i file di log di CRM è la stessa directory del file di log DTC. Nei cluster, il file di log DTC si trova su un disco condiviso di cui è stato eseguito il failover tra i nodi del cluster. Questo significa che il comportamento predefinito per le applicazioni server CRM consiste nel failover tra i nodi del cluster. Di conseguenza, se un CRM specifico richiede il comportamento alternativo del failover tra i nodi, è necessario modificare il percorso del file di log CRM per quella particolare applicazione del server CRM.

Se, inoltre, è necessario il failover per l'applicazione CRM, è necessario configurarlo come applicazione generica in un gruppo di cluster. La dipendenza deve essere DTC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



