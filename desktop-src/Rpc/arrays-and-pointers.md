---
title: Matrici e puntatori
description: Remote Procedure Call (RPC) è progettato per essere perlopiù trasparente per gli sviluppatori.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- RPC, descrizione, matrici e puntatori di RPC (Remote Procedure Call)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711335"
---
# <a name="arrays-and-pointers"></a><span data-ttu-id="b28d0-104">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="b28d0-104">Arrays and Pointers</span></span>

<span data-ttu-id="b28d0-105">Remote Procedure Call (RPC) è progettato per essere perlopiù trasparente per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b28d0-105">Remote Procedure Call (RPC) is designed to be mostly transparent to developers.</span></span> <span data-ttu-id="b28d0-106">Per ottenere questa trasparenza, lo stub del client trasmette al server sia il puntatore che l'oggetto dati a cui punta.</span><span class="sxs-lookup"><span data-stu-id="b28d0-106">To achieve this transparency, the client stub transmits to the server both the pointer and the data object to which it points.</span></span> <span data-ttu-id="b28d0-107">Se la procedura remota modifica i dati, il server deve trasmettere nuovamente i nuovi dati al client, in modo che il client possa copiare i nuovi dati sui dati originali.</span><span class="sxs-lookup"><span data-stu-id="b28d0-107">If the remote procedure changes the data, the server must transmit the new data back to the client so that the client can copy the new data over the original data.</span></span>

<span data-ttu-id="b28d0-108">In generale, una chiamata di procedura remota si comporta esattamente come una chiamata di procedura locale.</span><span class="sxs-lookup"><span data-stu-id="b28d0-108">In general, a remote procedure call behaves just like a local procedure call.</span></span> <span data-ttu-id="b28d0-109">Ovvero, quando un puntatore è un parametro, la procedura remota può accedere all'oggetto dati a cui fa riferimento il puntatore in modo analogo a una procedura locale.</span><span class="sxs-lookup"><span data-stu-id="b28d0-109">That is, when a pointer is a parameter, the remote procedure can access the data object the pointer refers to in the same way that a local procedure can.</span></span>

<span data-ttu-id="b28d0-110">Poiché i programmi client e server vengono eseguiti in spazi di indirizzi diversi, gli sviluppatori devono usare gli attributi Microsoft Interface Definition Language (MIDL) per descrivere il modo in cui i dati della matrice e del puntatore vengono trasmessi tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="b28d0-110">Since client and server programs run in different address spaces, developers must use Microsoft Interface Definition Language (MIDL) attributes to describe how array and pointer data is transmitted between the client and the server.</span></span> <span data-ttu-id="b28d0-111">In questa sezione viene presentata una panoramica sull'utilizzo di matrici e puntatori nelle applicazioni distribuite negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b28d0-111">This section presents an overview of how to use arrays and pointers in distributed applications, in the following topics:</span></span>

-   [<span data-ttu-id="b28d0-112">Matrici e RPC</span><span class="sxs-lookup"><span data-stu-id="b28d0-112">Arrays and RPC</span></span>](arrays-and-rpc.md)
-   [<span data-ttu-id="b28d0-113">Puntatori e RPC</span><span class="sxs-lookup"><span data-stu-id="b28d0-113">Pointers and RPC</span></span>](pointers-and-rpc.md)
-   [<span data-ttu-id="b28d0-114">Utilizzo di matrici, stringhe e puntatori</span><span class="sxs-lookup"><span data-stu-id="b28d0-114">Using Arrays, Strings, and Pointers</span></span>](using-arrays-strings-and-pointers.md)

 

 




