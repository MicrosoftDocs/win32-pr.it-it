---
title: Memory-Management modelli
description: Memory-Management modelli
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a985158f54bf09d149e04c7eebc5853417e39191ca0bb854cb7d1ba5de1e5d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019981"
---
# <a name="memory-management-models"></a>Memory-Management modelli

Gli sviluppatori possono scegliere tra diverse modalità di allocazione e di libera della memoria. Si consideri una struttura di dati complessa costituita da nodi connessi con puntatori, ad esempio un elenco collegato o un albero. È possibile applicare attributi che selezionano uno dei modelli seguenti:

-   [Allocazione e deallocazione nodo per nodo](node-by-node-allocation-and-deallocation.md).
-   [Singolo buffer lineare allocato dallo stub per l'intero albero](stub-allocated-buffers.md).
-   [Gestione della memoria stub del server](server-stub-memory-management.md)
-   [Singolo buffer lineare allocato dall'applicazione client per l'intero albero](application-allocated-buffer.md)di .
-   [Archiviazione permanente nel server](persistent-storage-on-the-server.md).

 

 




