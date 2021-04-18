---
description: Per sincronizzare l'accesso a una risorsa, usare uno degli oggetti di sincronizzazione in una delle funzioni di attesa.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Informazioni sulla sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315315"
---
# <a name="about-synchronization"></a><span data-ttu-id="8f0da-103">Informazioni sulla sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="8f0da-103">About Synchronization</span></span>

<span data-ttu-id="8f0da-104">Per sincronizzare l'accesso a una risorsa, usare uno degli [oggetti di sincronizzazione](synchronization-objects.md) in una delle [funzioni di attesa](wait-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8f0da-104">To synchronize access to a resource, use one of the [synchronization objects](synchronization-objects.md) in one of the [wait functions](wait-functions.md).</span></span> <span data-ttu-id="8f0da-105">Lo stato di un oggetto di sincronizzazione è *segnalato* o non *segnalato*.</span><span class="sxs-lookup"><span data-stu-id="8f0da-105">The state of a synchronization object is either *signaled* or *nonsignaled*.</span></span> <span data-ttu-id="8f0da-106">Le funzioni Wait consentono a un thread di bloccare la propria esecuzione fino a quando un oggetto non segnalato specificato non è impostato sullo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="8f0da-106">The wait functions allow a thread to block its own execution until a specified nonsignaled object is set to the signaled state.</span></span> <span data-ttu-id="8f0da-107">Per ulteriori informazioni, vedere [sincronizzazione interprocesso](interprocess-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="8f0da-107">For more information, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

<span data-ttu-id="8f0da-108">Di seguito sono riportati altri meccanismi di sincronizzazione:</span><span class="sxs-lookup"><span data-stu-id="8f0da-108">The following are other synchronization mechanisms:</span></span>

-   [<span data-ttu-id="8f0da-109">input e output sovrapposti</span><span class="sxs-lookup"><span data-stu-id="8f0da-109">overlapped input and output</span></span>](synchronization-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="8f0da-110">chiamate di procedure asincrone</span><span class="sxs-lookup"><span data-stu-id="8f0da-110">asynchronous procedure calls</span></span>](asynchronous-procedure-calls.md)
-   [<span data-ttu-id="8f0da-111">oggetti sezione critica</span><span class="sxs-lookup"><span data-stu-id="8f0da-111">critical section objects</span></span>](critical-section-objects.md)
-   [<span data-ttu-id="8f0da-112">variabili di condizione</span><span class="sxs-lookup"><span data-stu-id="8f0da-112">condition variables</span></span>](condition-variables.md)
-   [<span data-ttu-id="8f0da-113">blocchi in lettura/scrittura Slim</span><span class="sxs-lookup"><span data-stu-id="8f0da-113">slim reader/writer locks</span></span>](slim-reader-writer--srw--locks.md)
-   [<span data-ttu-id="8f0da-114">inizializzazione unica</span><span class="sxs-lookup"><span data-stu-id="8f0da-114">one-time initialization</span></span>](one-time-initialization.md)
-   [<span data-ttu-id="8f0da-115">accesso a variabili Interlocked</span><span class="sxs-lookup"><span data-stu-id="8f0da-115">interlocked variable access</span></span>](interlocked-variable-access.md)
-   [<span data-ttu-id="8f0da-116">elenchi collegati singolarmente con Interlocking</span><span class="sxs-lookup"><span data-stu-id="8f0da-116">interlocked singly linked lists</span></span>](interlocked-singly-linked-lists.md)
-   [<span data-ttu-id="8f0da-117">Code timer</span><span class="sxs-lookup"><span data-stu-id="8f0da-117">timer queues</span></span>](timer-queues.md)
-   <span data-ttu-id="8f0da-118">macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)</span><span class="sxs-lookup"><span data-stu-id="8f0da-118">the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) macro</span></span>

<span data-ttu-id="8f0da-119">Per ulteriori informazioni sulla sincronizzazione, vedere la pagina relativa ai [problemi di sincronizzazione e multiprocessore](synchronization-and-multiprocessor-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8f0da-119">For additional information on synchronization, see [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).</span></span>

 

 
