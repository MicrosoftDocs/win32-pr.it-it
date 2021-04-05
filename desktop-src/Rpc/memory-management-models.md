---
title: Modelli di Memory-Management
description: Modelli di Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955853"
---
# <a name="memory-management-models"></a>Modelli di Memory-Management

Gli sviluppatori hanno diverse opzioni per l'allocazione e la liberazione della memoria. Si consideri una struttura di dati complessa costituita da nodi connessi con puntatori, ad esempio un elenco collegato o un albero. È possibile applicare attributi che consentono di selezionare uno dei modelli seguenti:

-   Allocazione [e deallocazione di nodi per nodo](node-by-node-allocation-and-deallocation.md).
-   [Singolo buffer lineare allocato dallo stub per l'intero albero](stub-allocated-buffers.md).
-   [Gestione della memoria stub server](server-stub-memory-management.md)
-   [Singolo buffer lineare allocato dall'applicazione client per l'intero albero](application-allocated-buffer.md).
-   [Archiviazione permanente sul server](persistent-storage-on-the-server.md).

 

 




