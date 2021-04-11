---
description: Diverse funzioni del provider di rete accettano l'indirizzo e la dimensione di un buffer in cui la funzione inserisce una struttura di dati a dimensione variabile.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Gestione dei dati memorizzati nel buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232839"
---
# <a name="handling-buffered-data"></a><span data-ttu-id="66d83-103">Gestione dei dati memorizzati nel buffer</span><span class="sxs-lookup"><span data-stu-id="66d83-103">Handling Buffered Data</span></span>

<span data-ttu-id="66d83-104">Diverse funzioni del provider di rete accettano l'indirizzo e la dimensione di un buffer in cui la funzione inserisce una struttura di dati a dimensione variabile.</span><span class="sxs-lookup"><span data-stu-id="66d83-104">Several of the network provider functions take the address and size of a buffer into which the function places a variable-sized data structure.</span></span>

<span data-ttu-id="66d83-105">In ogni caso, il meccanismo usato è lo stesso.</span><span class="sxs-lookup"><span data-stu-id="66d83-105">In each case, the mechanism used is the same.</span></span> <span data-ttu-id="66d83-106">Il chiamante alloca un buffer e passa il relativo indirizzo alla funzione.</span><span class="sxs-lookup"><span data-stu-id="66d83-106">The caller allocates a buffer and passes its address to the function.</span></span> <span data-ttu-id="66d83-107">Passa inoltre l'indirizzo di un **DWORD** che specifica la dimensione del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="66d83-107">It also passes the address of a **DWORD** that specifies the size of the buffer, in bytes.</span></span>

<span data-ttu-id="66d83-108">La funzione copia quindi la maggior parte della struttura di dati richiesta come può essere nel buffer.</span><span class="sxs-lookup"><span data-stu-id="66d83-108">The function then copies as much of the requested data structure as it can into the buffer.</span></span> <span data-ttu-id="66d83-109">Se tutti i dati si integrano nel buffer, la funzione restituisce l' \_ esito positivo.</span><span class="sxs-lookup"><span data-stu-id="66d83-109">If all of the data fits into the buffer, the function returns WN\_SUCCESS.</span></span> <span data-ttu-id="66d83-110">Se i dati non rientrano nel buffer, i dati potrebbero essere incompleti e la funzione imposta l'errore di \_ altri \_ dati.</span><span class="sxs-lookup"><span data-stu-id="66d83-110">If the data does not fit into the buffer, the data may be left incomplete, and the function sets the WN\_MORE\_DATA error.</span></span> <span data-ttu-id="66d83-111">In entrambi i casi, il **valore DWORD** che indica la dimensione del buffer è impostato sul numero di byte effettivamente necessari per la struttura dei dati.</span><span class="sxs-lookup"><span data-stu-id="66d83-111">In either case, the **DWORD** indicating the size of the buffer is set to the number of bytes actually required by the data structure.</span></span> <span data-ttu-id="66d83-112">In questo modo, se il buffer passato era troppo piccolo e la funzione ha esito negativo, il chiamante può allocare un nuovo buffer della dimensione richiesta e chiamare di nuovo la funzione.</span><span class="sxs-lookup"><span data-stu-id="66d83-112">This way, if the buffer passed in was too small and the function failed, the caller may allocate a new buffer of the required size and call the function again.</span></span>

<span data-ttu-id="66d83-113">Quando le strutture di dati restituite includono stringhe a lunghezza variabile, le singole strutture di dati contengono in genere puntatori a queste stringhe.</span><span class="sxs-lookup"><span data-stu-id="66d83-113">When the data structures returned include variable-length strings, the individual data structures typically contain pointers to these strings.</span></span> <span data-ttu-id="66d83-114">Anche le stringhe devono essere posizionate all'interno del buffer.</span><span class="sxs-lookup"><span data-stu-id="66d83-114">The strings themselves should also be placed within the buffer.</span></span> <span data-ttu-id="66d83-115">Tuttavia, è importante posizionarli alla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="66d83-115">However, it is important to place them at the end of the buffer.</span></span> <span data-ttu-id="66d83-116">In caso contrario, non sarà possibile eseguire l'indicizzazione dell'ennesima struttura.</span><span class="sxs-lookup"><span data-stu-id="66d83-116">Otherwise, they will make indexing to the Nth structure impossible.</span></span> <span data-ttu-id="66d83-117">In altre parole, tutte le strutture si trovano in modo contiguo all'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="66d83-117">In other words, all structures are located contiguously at the beginning of the buffer.</span></span> <span data-ttu-id="66d83-118">I puntatori a stringhe o a dati a lunghezza variabile devono essere puntatori effettivi, non offset nel buffer.</span><span class="sxs-lookup"><span data-stu-id="66d83-118">Pointers to strings or variable length data must be actual pointers, not offsets into the buffer.</span></span>

<span data-ttu-id="66d83-119">Quando si utilizza un buffer per passare e restituire dati costituiti solo da stringhe, il **valore DWORD** che specifica la dimensione del buffer deve essere impostato sul numero totale di caratteri che si adattano a tali stringhe, non sul numero di byte.</span><span class="sxs-lookup"><span data-stu-id="66d83-119">When a buffer is used to pass in and return data that consists only of strings, the **DWORD** specifying the size of the buffer should be set to the total number of characters that will fit in these strings, not to the number of bytes.</span></span>

 

 



