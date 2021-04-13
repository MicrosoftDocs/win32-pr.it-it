---
title: Modalità di allocazione e deallocazione della memoria
description: Per impostazione predefinita, il codice stub generato dal compilatore MIDL chiama funzioni fornite dall'utente per allocare e liberare memoria. Queste funzioni, denominato MIDL \_ User \_ allocate e MIDL \_ User \_ Free, devono essere fornite dallo sviluppatore e collegate con l'applicazione.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c32ac4d33fbd67f617f79125921ddfffc0de5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399424"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Modalità di allocazione e deallocazione della memoria

Per impostazione predefinita, il codice stub generato dal compilatore MIDL chiama funzioni fornite dall'utente per allocare e liberare memoria. Queste funzioni, denominato [**MIDL \_ User \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e [**MIDL \_ User \_ Free**](/windows/desktop/Midl/midl-user-free-1), devono essere fornite dallo sviluppatore e collegate con l'applicazione.

Tutte le applicazioni devono fornire le implementazioni dell' [**\_ utente MIDL \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e l' [**\_ utente MIDL \_ Free**](/windows/desktop/Midl/midl-user-free-1), anche se i nomi di queste funzioni potrebbero non essere visualizzati in modo esplicito negli stub. L'unica eccezione si verifica quando si esegue la compilazione in modalità OSF-Compatibility (/OSF). Queste funzioni fornite dall'utente devono corrispondere a un prototipo di funzione specifico definito, ma in caso contrario, possono essere implementate in qualsiasi modo pratico o utile per l'applicazione. In alternativa, le applicazioni possono utilizzare il pacchetto di gestione della memoria RpcSs. La libreria run-time di Microsoft RPC fornisce questo gruppo di funzioni.

Nelle sezioni seguenti vengono descritte le funzioni di gestione della memoria RPC.

-   [**\_alloca utente \_ MIDL**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**\_utente MIDL \_ gratuito**](/windows/desktop/Midl/midl-user-free-1)
-   [Pacchetto di gestione della memoria RpcSs](rpcss-memory-management-package.md)

 

 