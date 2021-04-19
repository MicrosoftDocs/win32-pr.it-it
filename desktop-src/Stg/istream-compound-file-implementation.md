---
title: Implementazione del file composto IStream
description: L'interfaccia IStream supporta la lettura e la scrittura di dati negli oggetti flusso. In un oggetto di archiviazione strutturato gli oggetti flusso contengono i dati e le archiviazioni forniscono la struttura.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320215"
---
# <a name="istream---compound-file-implementation"></a><span data-ttu-id="488c7-105">Implementazione del file composto IStream</span><span class="sxs-lookup"><span data-stu-id="488c7-105">IStream - Compound File Implementation</span></span>

<span data-ttu-id="488c7-106">L'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supporta la lettura e la scrittura di dati negli oggetti flusso.</span><span class="sxs-lookup"><span data-stu-id="488c7-106">The [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface supports reading and writing data to stream objects.</span></span> <span data-ttu-id="488c7-107">In un oggetto di archiviazione strutturato gli oggetti flusso contengono i dati e le archiviazioni forniscono la struttura.</span><span class="sxs-lookup"><span data-stu-id="488c7-107">In a structured storage object, stream objects contain the data and storages provide the structure.</span></span> <span data-ttu-id="488c7-108">I dati semplici possono essere scritti direttamente in un flusso, ma con maggiore frequenza, i flussi sono elementi annidati all'interno di un oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="488c7-108">Simple data can be written directly to a stream, but more frequently, streams are elements nested within a storage object.</span></span> <span data-ttu-id="488c7-109">Sono simili ai file standard.</span><span class="sxs-lookup"><span data-stu-id="488c7-109">They are similar to standard files.</span></span>

<span data-ttu-id="488c7-110">La specifica di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) definisce più funzionalità rispetto a quelle supportate dall'implementazione com.</span><span class="sxs-lookup"><span data-stu-id="488c7-110">The specification of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) defines more functionality than the COM implementation supports.</span></span> <span data-ttu-id="488c7-111">Ad esempio, l'interfaccia **IStream** definisce i flussi fino a 2 ⁶ ⁴ byte di lunghezza che richiedono un puntatore di ricerca a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="488c7-111">For example, the **IStream** interface defines streams up to 2⁶⁴ bytes in length requiring a 64-bit seek pointer.</span></span> <span data-ttu-id="488c7-112">Tuttavia, l'implementazione COM supporta solo flussi fino a 2 ³ ² di lunghezza (4 GB), mentre le operazioni di lettura e scrittura sono sempre limitate a 2 ³ ² byte alla volta.</span><span class="sxs-lookup"><span data-stu-id="488c7-112">However, the COM implementation only supports streams up to 2³² bytes in length (4 GB) and read and write operations are always limited to 2³² bytes at a time.</span></span> <span data-ttu-id="488c7-113">Anche l'implementazione COM non supporta la transazione di flusso o il blocco dell'area.</span><span class="sxs-lookup"><span data-stu-id="488c7-113">The COM implementation also does not support stream transactioning or region locking.</span></span>

<span data-ttu-id="488c7-114">Per creare un flusso semplice basato sulla memoria globale, ottenere un puntatore [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) chiamando la funzione API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span><span class="sxs-lookup"><span data-stu-id="488c7-114">To create a simple stream based on global memory, get an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer by calling the API function [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span></span> <span data-ttu-id="488c7-115">Per ottenere un puntatore **IStream** in un oggetto file composto, chiamare [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span><span class="sxs-lookup"><span data-stu-id="488c7-115">To get an **IStream** pointer within a compound file object, call either [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) or [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span></span> <span data-ttu-id="488c7-116">Queste funzioni recuperano un puntatore [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , con cui è possibile chiamare [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) per un puntatore **IStream** .</span><span class="sxs-lookup"><span data-stu-id="488c7-116">These functions retrieve an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer, with which you can then call [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) for an **IStream** pointer.</span></span> <span data-ttu-id="488c7-117">In entrambi i casi, viene usato lo stesso codice di implementazione di **IStream** .</span><span class="sxs-lookup"><span data-stu-id="488c7-117">In either case, the same **IStream** implementation code is used.</span></span>

> [!Note]  
> <span data-ttu-id="488c7-118">L'implementazione del file composto di archiviazione strutturata non ha esito positivo su un metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), ma include i metodi [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) e [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) tramite il puntatore all'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="488c7-118">The compound file implementation of structured storage does not succeed on a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method for [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), but it includes the [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) and [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) methods through the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer.</span></span>

 

## <a name="when-to-use"></a><span data-ttu-id="488c7-119">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="488c7-119">When to Use</span></span>

<span data-ttu-id="488c7-120">Chiamare i metodi di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per leggere e scrivere dati in un flusso.</span><span class="sxs-lookup"><span data-stu-id="488c7-120">Call the methods of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) to read and write data to a stream.</span></span>

<span data-ttu-id="488c7-121">Poiché è possibile effettuare il marshalling di oggetti flusso ad altri processi, le applicazioni possono condividere i dati negli oggetti di archiviazione senza dover usare la memoria globale.</span><span class="sxs-lookup"><span data-stu-id="488c7-121">Because stream objects can be marshaled to other processes, applications can share the data in storage objects without having to use global memory.</span></span> <span data-ttu-id="488c7-122">Nell'implementazione del file composto COM di oggetti Stream, le funzionalità di marshalling personalizzate in COM creano una versione remota dell'oggetto originale nel nuovo processo quando i due processi hanno accesso a memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="488c7-122">In the COM compound file implementation of stream objects, the custom marshaling facilities in COM create a remote version of the original object in the new process when the two processes have shared-memory access.</span></span> <span data-ttu-id="488c7-123">Quindi, non è necessario che la versione remota comunichi con il processo originale per eseguire le relative funzioni.</span><span class="sxs-lookup"><span data-stu-id="488c7-123">Thus, the remote version does not need to communicate with the original process to carry out its functions.</span></span>

<span data-ttu-id="488c7-124">La versione remota dell'oggetto flusso condivide lo stesso puntatore di ricerca del flusso originale.</span><span class="sxs-lookup"><span data-stu-id="488c7-124">The remote version of the stream object shares the same seek pointer as the original stream.</span></span> <span data-ttu-id="488c7-125">Se non si desidera condividere il puntatore Seek, utilizzare il metodo [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) per fornire una copia dell'oggetto flusso per il processo remoto.</span><span class="sxs-lookup"><span data-stu-id="488c7-125">If you do not want to share the seek pointer, use the [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) method to provide a copy of the stream object for the remote process.</span></span>

> [!Note]
> <span data-ttu-id="488c7-126">Se si crea un oggetto flusso di dimensioni maggiori dell'heap nella memoria del computer e si usa un handle **HGLOBAL** per un oggetto memoria globale, l'oggetto flusso chiama il metodo [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente, in modo che richieda più memoria.</span><span class="sxs-lookup"><span data-stu-id="488c7-126">If creating a stream object that is larger than the heap in your computer's memory and you are using an **HGLOBAL** handle to a global memory object, the stream object calls the [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) method internally whe it requires more memory.</span></span> <span data-ttu-id="488c7-127">Poiché **GlobalReAlloc** copia sempre i dati dall'origine alla destinazione, l'aumento di un oggetto flusso da 20 MB a 25 MB, ad esempio, richiede una notevole quantità di tempo.</span><span class="sxs-lookup"><span data-stu-id="488c7-127">Because **GlobalRealloc** always copies data from the source to the destination, increasing a stream object from 20 MB to 25 MB, for example, requires large amounts of time.</span></span> <span data-ttu-id="488c7-128">Ciò è dovuto alla dimensione degli incrementi copiati e viene peggiorata se nel computer sono presenti meno di 45 MB di memoria a causa dello scambio del disco.</span><span class="sxs-lookup"><span data-stu-id="488c7-128">This is due to the size of the increments copied and is worsened if there is less than 45 MB of memory on the computer because of disk swapping.</span></span>
>
> <span data-ttu-id="488c7-129">La soluzione migliore consiste nell'implementare un metodo [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) che utilizza la memoria allocata da [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) anziché [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="488c7-129">The preferred solution is to implement an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) method that uses memory allocated by [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) instead of [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span></span> <span data-ttu-id="488c7-130">Questo può riservare una grande quantità di spazio degli indirizzi virtuali e quindi eseguire il commit della memoria all'interno di tale spazio di indirizzi in modo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="488c7-130">This can reserve a large chunk of virtual address space and then commit memory within that address space as required.</span></span> <span data-ttu-id="488c7-131">Non viene eseguita la copia dei dati e viene eseguito il commit della memoria solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="488c7-131">No data copying occurs and memory is committed only as it is required.</span></span>
>
> <span data-ttu-id="488c7-132">Un'alternativa a [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) consiste nel chiamare il metodo [**IStream:: sesize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) sull'oggetto Stream per aumentare in anticipo l'allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="488c7-132">An alternative to [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) is to call the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method on the stream object to increase the memory allocation in advance.</span></span> <span data-ttu-id="488c7-133">Questa operazione non è tuttavia efficace quanto l'utilizzo di [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="488c7-133">This is not, however, as efficient as using [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), as described above.</span></span>

 

## <a name="methods"></a><span data-ttu-id="488c7-134">Metodi</span><span class="sxs-lookup"><span data-stu-id="488c7-134">Methods</span></span>

<dl> <dt>

<span data-ttu-id="488c7-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span><span class="sxs-lookup"><span data-stu-id="488c7-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-136">Legge un numero specificato di byte dall'oggetto flusso in memoria a partire dal puntatore di posizionamento corrente.</span><span class="sxs-lookup"><span data-stu-id="488c7-136">Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</span></span> <span data-ttu-id="488c7-137">Questa implementazione restituisce \_ OK se è stata raggiunta la fine del flusso durante la lettura.</span><span class="sxs-lookup"><span data-stu-id="488c7-137">This implementation returns S\_OK if the end of the stream was reached during the read.</span></span> <span data-ttu-id="488c7-138">Questo comportamento è identico a quello del "fine del file" trovato nella file system FAT di MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="488c7-138">(This is the same as the "end of file" behavior found in the MS-DOS FAT file system.)</span></span>

</dd> <dt>

<span data-ttu-id="488c7-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span><span class="sxs-lookup"><span data-stu-id="488c7-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-140">Scrive un numero specificato da byte nell'oggetto flusso a partire dal puntatore di ricerca corrente.</span><span class="sxs-lookup"><span data-stu-id="488c7-140">Writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span> <span data-ttu-id="488c7-141">In questa implementazione gli oggetti flusso non sono di tipo sparse.</span><span class="sxs-lookup"><span data-stu-id="488c7-141">In this implementation, stream objects are not sparse.</span></span> <span data-ttu-id="488c7-142">Tutti i byte di riempimento vengono infine allocati sul disco e assegnati al flusso.</span><span class="sxs-lookup"><span data-stu-id="488c7-142">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

</dd> <dt>

<span data-ttu-id="488c7-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span><span class="sxs-lookup"><span data-stu-id="488c7-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-144">Sposta il puntatore di posizionamento su un nuovo percorso relativo all'inizio del flusso, alla fine del flusso o al puntatore di posizionamento corrente.</span><span class="sxs-lookup"><span data-stu-id="488c7-144">Changes the seek pointer to a new location relative to the beginning of the stream, to the end of the stream, or to the current seek pointer.</span></span>

</dd> <dt>

<span data-ttu-id="488c7-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: sesize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span><span class="sxs-lookup"><span data-stu-id="488c7-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-146">Modifica la dimensione dell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="488c7-146">Changes the size of the stream object.</span></span> <span data-ttu-id="488c7-147">In questa implementazione, non vi è alcuna garanzia che lo spazio allocato sarà contiguo.</span><span class="sxs-lookup"><span data-stu-id="488c7-147">In this implementation, there is no guarantee that the space allocated will be contiguous.</span></span>

</dd> <dt>

<span data-ttu-id="488c7-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span><span class="sxs-lookup"><span data-stu-id="488c7-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-149">Copia un numero specificato di byte dal puntatore di posizionamento corrente nel flusso al puntatore di posizionamento corrente in un altro flusso.</span><span class="sxs-lookup"><span data-stu-id="488c7-149">Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.</span></span>

</dd> <dt>

<span data-ttu-id="488c7-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span><span class="sxs-lookup"><span data-stu-id="488c7-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-151">L'implementazione del file composto di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supporta l'apertura dei flussi solo in modalità diretta, non in modalità transazionale.</span><span class="sxs-lookup"><span data-stu-id="488c7-151">The compound file implementation of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supports opening streams only in direct mode, not transacted mode.</span></span> <span data-ttu-id="488c7-152">Pertanto, il metodo non ha alcun effetto quando viene chiamato diverso da per svuotare tutti i buffer di memoria al livello di archiviazione successivo.</span><span class="sxs-lookup"><span data-stu-id="488c7-152">Therefore, the method has no effect when called other than to flush all memory buffers to the next storage level.</span></span>

<span data-ttu-id="488c7-153">In questa implementazione, non è importante se si esegue il commit delle modifiche nei flussi, è necessario eseguire solo le modifiche di commit per gli oggetti di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="488c7-153">In this implementation, it does not matter if you commit changes to streams, you need only commit changes for storage objects.</span></span>

</dd> <dt>

<span data-ttu-id="488c7-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span><span class="sxs-lookup"><span data-stu-id="488c7-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-155">Questa implementazione non supporta i flussi transazionali, pertanto una chiamata a questo metodo non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="488c7-155">This implementation does not support transacted streams, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="488c7-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span><span class="sxs-lookup"><span data-stu-id="488c7-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-157">Il blocco dell'intervallo non è supportato da questa implementazione, quindi una chiamata a questo metodo non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="488c7-157">Range-locking is not supported by this implementation, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="488c7-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span><span class="sxs-lookup"><span data-stu-id="488c7-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-159">Rimuove la restrizione di accesso in un intervallo di byte precedentemente limitati con [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span><span class="sxs-lookup"><span data-stu-id="488c7-159">Removes the access restriction on a range of bytes previously restricted with [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="488c7-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span><span class="sxs-lookup"><span data-stu-id="488c7-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-161">Recupera la struttura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) per questo flusso</span><span class="sxs-lookup"><span data-stu-id="488c7-161">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this stream</span></span>

</dd> <dt>

<span data-ttu-id="488c7-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span><span class="sxs-lookup"><span data-stu-id="488c7-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span></span>
</dt> <dd>

<span data-ttu-id="488c7-163">Crea un nuovo oggetto flusso con il proprio puntatore di posizionamento che fa riferimento agli stessi byte del flusso originale.</span><span class="sxs-lookup"><span data-stu-id="488c7-163">Creates a new stream object with its own seek pointer that references the same bytes as the original stream.</span></span>

</dd> </dl>

<span data-ttu-id="488c7-164">Un [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) in modalità semplice è soggetto ai vincoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="488c7-164">A simple-mode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is subject to the following constraints.</span></span>

-   <span data-ttu-id="488c7-165">Un flusso è una modalità semplice se è stato creato o aperto da un'archiviazione in modalità semplice.</span><span class="sxs-lookup"><span data-stu-id="488c7-165">A stream is simple mode if it was created or opened from a simple-mode storage.</span></span> <span data-ttu-id="488c7-166">Un archivio è una modalità semplice se viene creato o aperto con il \_ flag semplice STGM impostato nel parametro *grfMode* .</span><span class="sxs-lookup"><span data-stu-id="488c7-166">A storage is simple mode if it is created or opened with the STGM\_SIMPLE flag set in the *grfMode* parameter.</span></span>
-   <span data-ttu-id="488c7-167">I metodi [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) e [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="488c7-167">The [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) and [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) methods are not supported.</span></span>
-   <span data-ttu-id="488c7-168">Il metodo [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) è supportato, ma è \_ necessario specificare il valore StatFlag Noname.</span><span class="sxs-lookup"><span data-stu-id="488c7-168">The [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method is supported, but the STATFLAG\_NONAME value must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="488c7-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="488c7-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="488c7-170">**IStream**</span><span class="sxs-lookup"><span data-stu-id="488c7-170">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="488c7-171">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="488c7-171">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="488c7-172">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="488c7-172">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[<span data-ttu-id="488c7-173">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="488c7-173">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="488c7-174">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="488c7-174">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 