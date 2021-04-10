---
title: Attributi ACF di gestione della memoria
description: Gli attributi elencati nella tabella seguente consentono di eseguire la gestione della memoria dal lato client.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- MIDL, attributi, gestione della memoria di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963028"
---
# <a name="memory-management-acf-attributes"></a><span data-ttu-id="57a75-104">Attributi ACF di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="57a75-104">Memory Management ACF Attributes</span></span>

<span data-ttu-id="57a75-105">Gli attributi elencati nella tabella seguente consentono di eseguire la gestione della memoria dal lato client.</span><span class="sxs-lookup"><span data-stu-id="57a75-105">The attributes listed in the following table enable you to perform memory management from the client side.</span></span>



| <span data-ttu-id="57a75-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="57a75-106">Attribute</span></span>                                   | <span data-ttu-id="57a75-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="57a75-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57a75-108">**allocare**</span><span class="sxs-lookup"><span data-stu-id="57a75-108">**allocate**</span></span>](allocate.md)                | <span data-ttu-id="57a75-109">Specifica il modo in cui l'applicazione client e lo stub allocano e rilasciano memoria per i puntatori.</span><span class="sxs-lookup"><span data-stu-id="57a75-109">Specifies the way the client application and stub allocate and release memory for pointers.</span></span> <span data-ttu-id="57a75-110">Questo attributo è particolarmente utile quando si desidera che determinate strutture del puntatore rimangano accessibili all'applicazione server dopo che la chiamata RPC viene restituita al client.</span><span class="sxs-lookup"><span data-stu-id="57a75-110">This attribute is particularly useful when you want certain pointer structures to remain accessible to the server application after the remote procedure call returns to the client.</span></span> <span data-ttu-id="57a75-111">È anche possibile usare l'attributo [**allocate**](allocate.md) per indirizzare lo stub per calcolare le dimensioni di tutta la memoria a cui viene fatto riferimento tramite il puntatore del tipo specificato e per eseguire una singola chiamata all' [**\_ utente MIDL \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="57a75-111">You can also use the [**allocate**](allocate.md) attribute to direct the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span> |
| [<span data-ttu-id="57a75-112">**\_conteggio byte**</span><span class="sxs-lookup"><span data-stu-id="57a75-112">**byte\_count**</span></span>](byte-count.md)           | <span data-ttu-id="57a75-113">Consente di creare un blocco di memoria persistente e contiguo che può essere riutilizzato in più chiamate di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="57a75-113">Enables you to create a persistent, contiguous block of memory that can be reused over multiple remote procedure calls.</span></span> <span data-ttu-id="57a75-114">In questo modo l'applicazione client evita l'overhead di allocare e rilasciare ripetutamente memoria che può includere più puntatori e altre strutture di dati complesse.</span><span class="sxs-lookup"><span data-stu-id="57a75-114">This frees the client application from the overhead of repeatedly allocating and releasing memory that may include multiple pointers and other complex data structures.</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="57a75-115">**Abilita \_ allocazione**</span><span class="sxs-lookup"><span data-stu-id="57a75-115">**enable\_allocate**</span></span>](enable-allocate.md) | <span data-ttu-id="57a75-116">Specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.</span><span class="sxs-lookup"><span data-stu-id="57a75-116">Specifies that the server stub code should enable the stub memory-management environment.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 