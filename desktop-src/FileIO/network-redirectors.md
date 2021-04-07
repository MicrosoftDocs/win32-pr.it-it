---
description: Descrive la funzionalità di un redirector di rete.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirector di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885558"
---
# <a name="network-redirectors"></a><span data-ttu-id="5b33a-103">Redirector di rete</span><span class="sxs-lookup"><span data-stu-id="5b33a-103">Network Redirectors</span></span>

<span data-ttu-id="5b33a-104">Un redirector di rete è un driver file system (o FSD) che funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="5b33a-104">A network redirector is a file system driver (or FSD) that functions in the following manner:</span></span>

-   <span data-ttu-id="5b33a-105">Come client in un'operazione di I/O di rete inviando richieste di I/O ai server ed elaborando le risposte dai server.</span><span class="sxs-lookup"><span data-stu-id="5b33a-105">As a client in a network I/O operation by sending I/O requests to servers and processing the responses from the servers.</span></span>
-   <span data-ttu-id="5b33a-106">Come server in un'operazione di I/O di rete tramite la ricezione di richieste di I/O dai server e l'elaborazione delle richieste.</span><span class="sxs-lookup"><span data-stu-id="5b33a-106">As a server in a network I/O operation by receiving I/O requests from servers and processing the requests.</span></span>

<span data-ttu-id="5b33a-107">Esegue tutte le interazioni di basso livello con il server nella risoluzione del nome file fornito dall'applicazione con il percorso della risorsa nel server remoto.</span><span class="sxs-lookup"><span data-stu-id="5b33a-107">It performs all of the low-level interaction with the server in resolving the file name provided by the application with the location of the resource on the remote server.</span></span> <span data-ttu-id="5b33a-108">In questo modo, il redirector consente all'applicazione di accedere e modificare le risorse nei server remoti come se si trovassero nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="5b33a-108">In this way, the redirector enables the application to access and manipulate resources on remote servers as if they were located on the local machine.</span></span>

<span data-ttu-id="5b33a-109">I redirector funzionano interamente in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="5b33a-109">Redirectors operate entirely within kernel mode.</span></span> <span data-ttu-id="5b33a-110">Ciò offre i vantaggi delle prestazioni seguenti rispetto alle alternative in modalità utente:</span><span class="sxs-lookup"><span data-stu-id="5b33a-110">This provides the following performance advantages over user-mode alternatives:</span></span>

-   <span data-ttu-id="5b33a-111">Può interagire con FSDs in modalità kernel in esecuzione sul server, ad esempio il server FSD, senza la necessità della modalità da utente a kernel e commutatori di contesto in modalità kernel-to-User.</span><span class="sxs-lookup"><span data-stu-id="5b33a-111">It can interact with kernel-mode FSDs running on the server, such as the server FSD, without the need for user-to-kernel mode and kernel-to-user mode context switches.</span></span>
-   <span data-ttu-id="5b33a-112">Può interagire in modalità kernel con gestione cache sul server per memorizzare nella cache i dati di I/O inviati dal gestore della cache del server al client.</span><span class="sxs-lookup"><span data-stu-id="5b33a-112">It can interact in kernel mode with the cache manager on the server to cache I/O data that the server cache manager sends on the client.</span></span>
-   <span data-ttu-id="5b33a-113">Le funzioni API personalizzate per le richieste di I/O remote e le modifiche apportate alle funzioni di I/O dei file standard per fornire questa funzionalità non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="5b33a-113">API functions custom-made for remote I/O requests, and changes to the standard file I/O functions to provide this functionality, are not necessary.</span></span>

 

 



