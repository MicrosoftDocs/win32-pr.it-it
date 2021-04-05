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
# <a name="memory-management-models"></a><span data-ttu-id="28cfd-103">Modelli di Memory-Management</span><span class="sxs-lookup"><span data-stu-id="28cfd-103">Memory-Management Models</span></span>

<span data-ttu-id="28cfd-104">Gli sviluppatori hanno diverse opzioni per l'allocazione e la liberazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="28cfd-104">As a developer, you have several choices for how memory is allocated and freed.</span></span> <span data-ttu-id="28cfd-105">Si consideri una struttura di dati complessa costituita da nodi connessi con puntatori, ad esempio un elenco collegato o un albero.</span><span class="sxs-lookup"><span data-stu-id="28cfd-105">Consider a complex data structure that consists of nodes connected with pointers, such as a linked list or a tree.</span></span> <span data-ttu-id="28cfd-106">È possibile applicare attributi che consentono di selezionare uno dei modelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="28cfd-106">You can apply attributes that select one of the following models:</span></span>

-   <span data-ttu-id="28cfd-107">Allocazione [e deallocazione di nodi per nodo](node-by-node-allocation-and-deallocation.md).</span><span class="sxs-lookup"><span data-stu-id="28cfd-107">[Node-by-node allocation and deallocation](node-by-node-allocation-and-deallocation.md).</span></span>
-   <span data-ttu-id="28cfd-108">[Singolo buffer lineare allocato dallo stub per l'intero albero](stub-allocated-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="28cfd-108">[A single linear buffer allocated by the stub for the entire tree](stub-allocated-buffers.md).</span></span>
-   [<span data-ttu-id="28cfd-109">Gestione della memoria stub server</span><span class="sxs-lookup"><span data-stu-id="28cfd-109">Server stub memory management</span></span>](server-stub-memory-management.md)
-   <span data-ttu-id="28cfd-110">[Singolo buffer lineare allocato dall'applicazione client per l'intero albero](application-allocated-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="28cfd-110">[A single linear buffer allocated by the client application for the entire tree](application-allocated-buffer.md).</span></span>
-   <span data-ttu-id="28cfd-111">[Archiviazione permanente sul server](persistent-storage-on-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="28cfd-111">[Persistent storage on the server](persistent-storage-on-the-server.md).</span></span>

 

 




