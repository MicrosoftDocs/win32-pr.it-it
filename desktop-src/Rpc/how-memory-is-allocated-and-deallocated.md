---
title: Come viene allocata e deallocata la memoria
description: Per impostazione predefinita, il codice stub generato dal compilatore MIDL chiama le funzioni fornite dall'utente per allocare e liberare memoria. Queste funzioni, denominate midl user allocate e midl user free, devono essere fornite dallo sviluppatore e \_ \_ collegate \_ \_ all'applicazione.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e7b4a0fd9a765593fc6f44365e17bc45c10b1244c226abc09ff302e81ec107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929518"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Come viene allocata e deallocata la memoria

Per impostazione predefinita, il codice stub generato dal compilatore MIDL chiama le funzioni fornite dall'utente per allocare e liberare memoria. Queste funzioni, denominate [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e [**midl \_ user \_ free,**](/windows/desktop/Midl/midl-user-free-1)devono essere fornite dallo sviluppatore e collegate all'applicazione.

Tutte le applicazioni devono fornire implementazioni di [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e [**midl \_ user \_ free,**](/windows/desktop/Midl/midl-user-free-1)anche se i nomi di queste funzioni potrebbero non essere visualizzati in modo esplicito negli stub. L'unica eccezione è quando si esegue la compilazione in modalità di compatibilità OSF (/osf). Queste funzioni fornite dall'utente devono corrispondere a un prototipo di funzione definito specifico, ma in caso contrario, possono essere implementate in qualsiasi modo utile o utile per l'applicazione. In alternativa, le applicazioni possono usare rpcSs Memory Management Package. La libreria di runtime RPC Microsoft fornisce questo gruppo di funzioni.

Le sezioni seguenti descrivono le funzioni di gestione della memoria RPC.

-   [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1)
-   [Pacchetto di gestione della memoria RpcSs](rpcss-memory-management-package.md)

 

 