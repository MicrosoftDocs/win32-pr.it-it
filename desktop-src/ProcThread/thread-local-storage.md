---
description: Con l'archiviazione locale di thread (TLS), è possibile fornire dati univoci per ogni thread a cui il processo può accedere usando un indice globale. Un thread alloca l'indice, che può essere utilizzato dagli altri thread per recuperare i dati univoci associati all'indice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: archiviazione thread-local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104551538"
---
# <a name="thread-local-storage"></a><span data-ttu-id="86482-104">archiviazione thread-local</span><span class="sxs-lookup"><span data-stu-id="86482-104">Thread Local Storage</span></span>

<span data-ttu-id="86482-105">Tutti i thread di un processo ne condividono lo spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="86482-105">All threads of a process share its virtual address space.</span></span> <span data-ttu-id="86482-106">Le variabili locali di una funzione sono univoche per ogni thread che esegue la funzione.</span><span class="sxs-lookup"><span data-stu-id="86482-106">The local variables of a function are unique to each thread that runs the function.</span></span> <span data-ttu-id="86482-107">Tuttavia, le variabili statiche e globali sono condivise da tutti i thread nel processo.</span><span class="sxs-lookup"><span data-stu-id="86482-107">However, the static and global variables are shared by all threads in the process.</span></span> <span data-ttu-id="86482-108">Con l' *archiviazione locale di thread* (TLS), è possibile fornire dati univoci per ogni thread a cui il processo può accedere usando un indice globale.</span><span class="sxs-lookup"><span data-stu-id="86482-108">With *thread local storage* (TLS), you can provide unique data for each thread that the process can access using a global index.</span></span> <span data-ttu-id="86482-109">Un thread alloca l'indice, che può essere utilizzato dagli altri thread per recuperare i dati univoci associati all'indice.</span><span class="sxs-lookup"><span data-stu-id="86482-109">One thread allocates the index, which can be used by the other threads to retrieve the unique data associated with the index.</span></span>

<span data-ttu-id="86482-110">La costante \_ valore minimo TLS \_ disponibile definisce il numero minimo di indici TLS disponibili in ogni processo.</span><span class="sxs-lookup"><span data-stu-id="86482-110">The constant TLS\_MINIMUM\_AVAILABLE defines the minimum number of TLS indexes available in each process.</span></span> <span data-ttu-id="86482-111">Il valore minimo è almeno 64 per tutti i sistemi.</span><span class="sxs-lookup"><span data-stu-id="86482-111">This minimum is guaranteed to be at least 64 for all systems.</span></span> <span data-ttu-id="86482-112">Il numero massimo di indici per processo è 1.088.</span><span class="sxs-lookup"><span data-stu-id="86482-112">The maximum number of indexes per process is 1,088.</span></span>

<span data-ttu-id="86482-113">Quando vengono creati i thread, il sistema alloca una matrice di valori **LPVOID** per TLS, che vengono inizializzati su null.</span><span class="sxs-lookup"><span data-stu-id="86482-113">When the threads are created, the system allocates an array of **LPVOID** values for TLS, which are initialized to NULL.</span></span> <span data-ttu-id="86482-114">Prima di poter utilizzare un indice, è necessario che venga allocato da uno dei thread.</span><span class="sxs-lookup"><span data-stu-id="86482-114">Before an index can be used, it must be allocated by one of the threads.</span></span> <span data-ttu-id="86482-115">Ogni thread archivia i dati per un indice TLS in uno *slot TLS* nella matrice.</span><span class="sxs-lookup"><span data-stu-id="86482-115">Each thread stores its data for a TLS index in a *TLS slot* in the array.</span></span> <span data-ttu-id="86482-116">Se i dati associati a un indice si adattano a un valore **LPVOID** , è possibile archiviare i dati direttamente nello slot TLS.</span><span class="sxs-lookup"><span data-stu-id="86482-116">If the data associated with an index will fit in an **LPVOID** value, you can store the data directly in the TLS slot.</span></span> <span data-ttu-id="86482-117">Tuttavia, se si usa un numero elevato di indici in questo modo, è preferibile allocare spazio di archiviazione separato, consolidare i dati e ridurre al minimo il numero di slot TLS in uso.</span><span class="sxs-lookup"><span data-stu-id="86482-117">However, if you are using a large number of indexes in this way, it is better to allocate separate storage, consolidate the data, and minimize the number of TLS slots in use.</span></span>

<span data-ttu-id="86482-118">Il diagramma seguente illustra il funzionamento di TLS.</span><span class="sxs-lookup"><span data-stu-id="86482-118">The following diagram illustrates how TLS works.</span></span> <span data-ttu-id="86482-119">Per un esempio di codice che illustra l'uso dell'archiviazione locale di thread, vedere [uso dell'archiviazione thread-local](using-thread-local-storage.md).</span><span class="sxs-lookup"><span data-stu-id="86482-119">For a code example illustrating the use of thread local storage, see [Using Thread Local Storage](using-thread-local-storage.md).</span></span>

![Diagramma che illustra il funzionamento del processo T L S.](images/tls.png)

<span data-ttu-id="86482-121">Il processo dispone di due thread, thread 1 e thread 2.</span><span class="sxs-lookup"><span data-stu-id="86482-121">The process has two threads, Thread 1 and Thread 2.</span></span> <span data-ttu-id="86482-122">Alloca due indici da usare con TLS, gdwTlsIndex1 e gdwTlsIndex2.</span><span class="sxs-lookup"><span data-stu-id="86482-122">It allocates two indexes for use with TLS, gdwTlsIndex1 and gdwTlsIndex2.</span></span> <span data-ttu-id="86482-123">Ogni thread alloca due blocchi di memoria (uno per ogni indice) in cui archiviare i dati e archivia i puntatori a questi blocchi di memoria negli slot TLS corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="86482-123">Each thread allocates two memory blocks (one for each index) in which to store the data, and stores the pointers to these memory blocks in the corresponding TLS slots.</span></span> <span data-ttu-id="86482-124">Per accedere ai dati associati a un indice, il thread recupera il puntatore al blocco di memoria dallo slot TLS e lo archivia nella variabile locale lpvData.</span><span class="sxs-lookup"><span data-stu-id="86482-124">To access the data associated with an index, the thread retrieves the pointer to the memory block from the TLS slot and stores it in the lpvData local variable.</span></span>

<span data-ttu-id="86482-125">È ideale usare TLS in una libreria di collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="86482-125">It is ideal to use TLS in a dynamic-link library (DLL).</span></span> <span data-ttu-id="86482-126">Per un esempio, vedere [uso dell'archiviazione locale di thread in una libreria a collegamento dinamico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span><span class="sxs-lookup"><span data-stu-id="86482-126">For an example, see [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86482-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86482-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86482-128">Archiviazione thread-local (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="86482-128">Thread Local Storage (Visual C++)</span></span>](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="86482-129">Uso dell'archiviazione locale di thread</span><span class="sxs-lookup"><span data-stu-id="86482-129">Using Thread Local Storage</span></span>](using-thread-local-storage.md)
</dt> <dt>

[<span data-ttu-id="86482-130">Utilizzo dell'archiviazione locale di thread in una libreria a collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="86482-130">Using Thread Local Storage in a Dynamic Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
