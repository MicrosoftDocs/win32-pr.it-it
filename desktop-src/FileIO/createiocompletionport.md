---
description: Crea una porta di completamento di I/O (input/output) e la associa a un handle di file specificato oppure crea una porta di completamento di I/O che non è ancora associata a un handle di file, consentendo l'associazione in un secondo momento.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Funzione CreateIoCompletionPort (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312935"
---
# <a name="createiocompletionport-function"></a><span data-ttu-id="509c3-103">CreateIoCompletionPort (funzione)</span><span class="sxs-lookup"><span data-stu-id="509c3-103">CreateIoCompletionPort function</span></span>

<span data-ttu-id="509c3-104">Crea una porta di completamento di I/O (input/output) e la associa a un handle di file specificato oppure crea una porta di completamento di I/O che non è ancora associata a un handle di file, consentendo l'associazione in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="509c3-104">Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.</span></span>

<span data-ttu-id="509c3-105">L'associazione di un'istanza di un handle di file aperto a una porta di completamento di I/O consente a un processo di ricevere una notifica del completamento delle operazioni di I/O asincrone che interessano tale handle di file.</span><span class="sxs-lookup"><span data-stu-id="509c3-105">Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.</span></span>

> [!Note]
>
> <span data-ttu-id="509c3-106">Il termine *handle di file* usato qui si riferisce a un'astrazione del sistema che rappresenta un endpoint di I/O sovrapposto, non solo un file su disco.</span><span class="sxs-lookup"><span data-stu-id="509c3-106">The term *file handle* as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk.</span></span> <span data-ttu-id="509c3-107">Tutti gli oggetti di sistema che supportano I/O sovrapposti, ad esempio endpoint di rete, socket TCP, named pipe e slot di posta elettronica, possono essere usati come handle di file.</span><span class="sxs-lookup"><span data-stu-id="509c3-107">Any system objects that support overlapped I/O such as network endpoints, TCP sockets, named pipes, and mail slots can be used as file handles.</span></span> <span data-ttu-id="509c3-108">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="509c3-108">For additional information, see the Remarks section.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="509c3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="509c3-109">Syntax</span></span>


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a><span data-ttu-id="509c3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="509c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="509c3-111">*Filehandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="509c3-111">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="509c3-112">Un handle di file aperto o un **\_ \_ valore di handle non valido**.</span><span class="sxs-lookup"><span data-stu-id="509c3-112">An open file handle or **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="509c3-113">L'handle deve essere a un oggetto che supporta l'I/O sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="509c3-113">The handle must be to an object that supports overlapped I/O.</span></span>

<span data-ttu-id="509c3-114">Se viene fornito un handle, è necessario che sia stato aperto per il completamento I/O sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="509c3-114">If a handle is provided, it has to have been opened for overlapped I/O completion.</span></span> <span data-ttu-id="509c3-115">È ad esempio necessario specificare il flag **\_ \_ OVERLAPPED del flag file** quando si utilizza la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per ottenere l'handle.</span><span class="sxs-lookup"><span data-stu-id="509c3-115">For example, you must specify the **FILE\_FLAG\_OVERLAPPED** flag when using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function to obtain the handle.</span></span>

<span data-ttu-id="509c3-116">Se viene specificato un **\_ \_ valore di handle non valido** , la funzione crea una porta di completamento di I/O senza associarla a un handle di file.</span><span class="sxs-lookup"><span data-stu-id="509c3-116">If **INVALID\_HANDLE\_VALUE** is specified, the function creates an I/O completion port without associating it with a file handle.</span></span> <span data-ttu-id="509c3-117">In questo caso, il parametro *ExistingCompletionPort* deve essere **null** e il parametro *CompletionKey* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="509c3-117">In this case, the *ExistingCompletionPort* parameter must be **NULL** and the *CompletionKey* parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="509c3-118">*ExistingCompletionPort* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="509c3-118">*ExistingCompletionPort* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="509c3-119">Handle per una porta di completamento di I/O esistente o **null**.</span><span class="sxs-lookup"><span data-stu-id="509c3-119">A handle to an existing I/O completion port or **NULL**.</span></span>

<span data-ttu-id="509c3-120">Se questo parametro specifica una porta di completamento di I/O esistente, la funzione la associa all'handle specificato dal parametro *filehandle* .</span><span class="sxs-lookup"><span data-stu-id="509c3-120">If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the *FileHandle* parameter.</span></span> <span data-ttu-id="509c3-121">Se ha esito positivo, la funzione restituisce l'handle della porta di completamento I/O esistente. non crea una nuova porta di completamento I/O.</span><span class="sxs-lookup"><span data-stu-id="509c3-121">The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.</span></span>

<span data-ttu-id="509c3-122">Se questo parametro è **null**, la funzione crea una nuova porta di completamento di i/o e, se il parametro *filehandle* è valido, lo associa alla nuova porta di completamento i/o.</span><span class="sxs-lookup"><span data-stu-id="509c3-122">If this parameter is **NULL**, the function creates a new I/O completion port and, if the *FileHandle* parameter is valid, associates it with the new I/O completion port.</span></span> <span data-ttu-id="509c3-123">In caso contrario non viene eseguita alcuna associazione di handle di file</span><span class="sxs-lookup"><span data-stu-id="509c3-123">Otherwise no file handle association occurs.</span></span> <span data-ttu-id="509c3-124">Se ha esito positivo, la funzione restituisce l'handle alla nuova porta di completamento I/O.</span><span class="sxs-lookup"><span data-stu-id="509c3-124">The function returns the handle to the new I/O completion port if successful.</span></span>

</dd> <dt>

<span data-ttu-id="509c3-125">*CompletionKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="509c3-125">*CompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="509c3-126">Chiave di completamento definita dall'utente per handle inclusa in ogni pacchetto di completamento I/O per l'handle di file specificato.</span><span class="sxs-lookup"><span data-stu-id="509c3-126">The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle.</span></span> <span data-ttu-id="509c3-127">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="509c3-127">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="509c3-128">*NumberOfConcurrentThreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="509c3-128">*NumberOfConcurrentThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="509c3-129">Il numero massimo di thread che il sistema operativo è in grado di consentire per elaborare contemporaneamente i pacchetti di completamento i/O per la porta di completamento I/O.</span><span class="sxs-lookup"><span data-stu-id="509c3-129">The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port.</span></span> <span data-ttu-id="509c3-130">Questo parametro viene ignorato se il parametro *ExistingCompletionPort* non è **null**.</span><span class="sxs-lookup"><span data-stu-id="509c3-130">This parameter is ignored if the *ExistingCompletionPort* parameter is not **NULL**.</span></span>

<span data-ttu-id="509c3-131">Se questo parametro è zero, il sistema consente il numero di thread in esecuzione simultanea quanti sono i processori del sistema.</span><span class="sxs-lookup"><span data-stu-id="509c3-131">If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="509c3-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="509c3-132">Return value</span></span>

<span data-ttu-id="509c3-133">Se la funzione ha esito positivo, il valore restituito è l'handle per una porta di completamento di I/O:</span><span class="sxs-lookup"><span data-stu-id="509c3-133">If the function succeeds, the return value is the handle to an I/O completion port:</span></span>

-   <span data-ttu-id="509c3-134">Se il parametro *ExistingCompletionPort* è **null**, il valore restituito è un nuovo handle.</span><span class="sxs-lookup"><span data-stu-id="509c3-134">If the *ExistingCompletionPort* parameter was **NULL**, the return value is a new handle.</span></span>

-   <span data-ttu-id="509c3-135">Se il parametro *ExistingCompletionPort* è un handle di porta di completamento i/O valido, il valore restituito è lo stesso handle.</span><span class="sxs-lookup"><span data-stu-id="509c3-135">If the *ExistingCompletionPort* parameter was a valid I/O completion port handle, the return value is that same handle.</span></span>

-   <span data-ttu-id="509c3-136">Se il parametro *filehandle* era un handle valido, l'handle di file è ora associato alla porta di completamento i/O restituita.</span><span class="sxs-lookup"><span data-stu-id="509c3-136">If the *FileHandle* parameter was a valid handle, that file handle is now associated with the returned I/O completion port.</span></span>

<span data-ttu-id="509c3-137">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="509c3-137">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="509c3-138">Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="509c3-138">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="509c3-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="509c3-139">Remarks</span></span>

<span data-ttu-id="509c3-140">Il sistema di I/O può ricevere istruzioni per inviare pacchetti di notifiche di completamento I/o alle porte di completamento I/O, in cui vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="509c3-140">The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued.</span></span> <span data-ttu-id="509c3-141">La funzione **CreateIoCompletionPort** fornisce questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="509c3-141">The **CreateIoCompletionPort** function provides this functionality.</span></span>

<span data-ttu-id="509c3-142">Una porta di completamento di I/O e il relativo handle sono associati al processo che lo ha creato e non è condivisibile tra i processi.</span><span class="sxs-lookup"><span data-stu-id="509c3-142">An I/O completion port and its handle are associated with the process that created it and is not sharable between processes.</span></span> <span data-ttu-id="509c3-143">Tuttavia, un singolo handle è condivisibile tra i thread nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="509c3-143">However, a single handle is sharable between threads in the same process.</span></span>

<span data-ttu-id="509c3-144">**CreateIoCompletionPort** può essere usato in tre modalità distinte:</span><span class="sxs-lookup"><span data-stu-id="509c3-144">**CreateIoCompletionPort** can be used in three distinct modes:</span></span>

-   <span data-ttu-id="509c3-145">Creare solo una porta di completamento I/O senza associarla a un handle di file.</span><span class="sxs-lookup"><span data-stu-id="509c3-145">Create only an I/O completion port without associating it with a file handle.</span></span>
-   <span data-ttu-id="509c3-146">Associare una porta di completamento di I/O esistente a un handle di file.</span><span class="sxs-lookup"><span data-stu-id="509c3-146">Associate an existing I/O completion port with a file handle.</span></span>
-   <span data-ttu-id="509c3-147">Eseguire sia la creazione che l'associazione in un'unica chiamata.</span><span class="sxs-lookup"><span data-stu-id="509c3-147">Perform both creation and association in a single call.</span></span>

<span data-ttu-id="509c3-148">Per creare una porta di completamento I/O senza associarla, impostare il *parametro filehandle* su **un \_ \_ valore di handle non valido**, il parametro *ExistingCompletionPort* su **null** e il parametro *CompletionKey* su zero (che in questo caso viene ignorato).</span><span class="sxs-lookup"><span data-stu-id="509c3-148">To create an I/O completion port without associating it, set the *FileHandle* parameter to **INVALID\_HANDLE\_VALUE**, the *ExistingCompletionPort* parameter to **NULL**, and the *CompletionKey* parameter to zero (which is ignored in this case).</span></span> <span data-ttu-id="509c3-149">Impostare il parametro *NumberOfConcurrentThreads* sul valore di concorrenza desiderato per la nuova porta di completamento i/o oppure su zero per l'impostazione predefinita (il numero di processori nel sistema).</span><span class="sxs-lookup"><span data-stu-id="509c3-149">Set the *NumberOfConcurrentThreads* parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).</span></span>

<span data-ttu-id="509c3-150">L'handle passato nel parametro *filehandle* può essere un handle che supporta i/O sovrapposti.</span><span class="sxs-lookup"><span data-stu-id="509c3-150">The handle passed in the *FileHandle* parameter can be any handle that supports overlapped I/O.</span></span> <span data-ttu-id="509c3-151">In genere, si tratta di un handle aperto dalla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando il flag di **file \_ \_ sovrapposto** (ad esempio, file, slot di posta e pipe).</span><span class="sxs-lookup"><span data-stu-id="509c3-151">Most commonly, this is a handle opened by the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function using the **FILE\_FLAG\_OVERLAPPED** flag (for example, files, mail slots, and pipes).</span></span> <span data-ttu-id="509c3-152">Gli oggetti creati da altre funzioni, ad esempio [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) , possono essere associati anche a una porta di completamento di I/O.</span><span class="sxs-lookup"><span data-stu-id="509c3-152">Objects created by other functions such as [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) can also be associated with an I/O completion port.</span></span> <span data-ttu-id="509c3-153">Per un esempio di utilizzo di Sockets, vedere [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span><span class="sxs-lookup"><span data-stu-id="509c3-153">For an example using sockets, see [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span></span> <span data-ttu-id="509c3-154">Un handle può essere associato a una sola porta di completamento di I/O e, dopo aver eseguito l'associazione, il punto di controllo rimane associato alla porta di completamento I/O fino alla chiusura.</span><span class="sxs-lookup"><span data-stu-id="509c3-154">A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.</span></span>

<span data-ttu-id="509c3-155">Per ulteriori informazioni sulla teoria della porta di completamento I/O, sull'utilizzo e sulle funzioni associate, vedere [porte di completamento i/o](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="509c3-155">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="509c3-156">È possibile associare più handle di file a una singola porta di completamento di I/O chiamando **CreateIoCompletionPort** più volte con lo stesso handle di porta di completamento di i/o nel parametro *ExistingCompletionPort* e un handle di file diverso nel parametro *filehandle* ogni volta.</span><span class="sxs-lookup"><span data-stu-id="509c3-156">Multiple file handles can be associated with a single I/O completion port by calling **CreateIoCompletionPort** multiple times with the same I/O completion port handle in the *ExistingCompletionPort* parameter and a different file handle in the *FileHandle* parameter each time.</span></span>

<span data-ttu-id="509c3-157">Usare il parametro *CompletionKey* per consentire all'applicazione di tenere traccia delle operazioni di I/O completate.</span><span class="sxs-lookup"><span data-stu-id="509c3-157">Use the *CompletionKey* parameter to help your application track which I/O operations have completed.</span></span> <span data-ttu-id="509c3-158">Questo valore non viene usato da **CreateIoCompletionPort** per il controllo funzionale. viene invece collegato all'handle di file specificato nel parametro *filehandle* al momento dell'associazione con una porta di completamento di I/O.</span><span class="sxs-lookup"><span data-stu-id="509c3-158">This value is not used by **CreateIoCompletionPort** for functional control; rather, it is attached to the file handle specified in the *FileHandle* parameter at the time of association with an I/O completion port.</span></span> <span data-ttu-id="509c3-159">Questa chiave di completamento deve essere univoca per ogni handle di file e accompagna l'handle di file durante il processo di Accodamento di completamento interno.</span><span class="sxs-lookup"><span data-stu-id="509c3-159">This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process.</span></span> <span data-ttu-id="509c3-160">Viene restituito nella chiamata di funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) all'arrivo di un pacchetto di completamento.</span><span class="sxs-lookup"><span data-stu-id="509c3-160">It is returned in the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function call when a completion packet arrives.</span></span> <span data-ttu-id="509c3-161">Il parametro *CompletionKey* viene usato anche dalla funzione [**PostQueuedCompletionStatus ha provocato**](postqueuedcompletionstatus.md) per accodare i pacchetti di completamento per scopi specifici.</span><span class="sxs-lookup"><span data-stu-id="509c3-161">The *CompletionKey* parameter is also used by the [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) function to queue your own special-purpose completion packets.</span></span>

<span data-ttu-id="509c3-162">Dopo che un'istanza di un handle aperto è associata a una porta di completamento di I/O, non può essere usata nella funzione [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) perché queste funzioni hanno meccanismi di i/o asincroni.</span><span class="sxs-lookup"><span data-stu-id="509c3-162">After an instance of an open handle is associated with an I/O completion port, it cannot be used in the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function because these functions have their own asynchronous I/O mechanisms.</span></span>

<span data-ttu-id="509c3-163">È preferibile non condividere un handle di file associato a una porta di completamento di I/O usando l'ereditarietà dell'handle o una chiamata alla funzione [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="509c3-163">It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="509c3-164">Le operazioni eseguite con tali handle duplicati generano notifiche di completamento.</span><span class="sxs-lookup"><span data-stu-id="509c3-164">Operations performed with such duplicate handles generate completion notifications.</span></span> <span data-ttu-id="509c3-165">Si consiglia di considerare attentamente.</span><span class="sxs-lookup"><span data-stu-id="509c3-165">Careful consideration is advised.</span></span>

<span data-ttu-id="509c3-166">Il punto di controllo della porta di completamento I/O e ogni handle di file associato alla porta di completamento I/O specifica sono noti come *riferimenti alla porta di completamento i/o*.</span><span class="sxs-lookup"><span data-stu-id="509c3-166">The I/O completion port handle and every file handle associated with that particular I/O completion port are known as *references to the I/O completion port*.</span></span> <span data-ttu-id="509c3-167">La porta di completamento I/O viene rilasciata quando non vi sono altri riferimenti.</span><span class="sxs-lookup"><span data-stu-id="509c3-167">The I/O completion port is released when there are no more references to it.</span></span> <span data-ttu-id="509c3-168">È pertanto necessario chiudere correttamente tutti questi handle per rilasciare la porta di completamento I/O e le risorse di sistema associate.</span><span class="sxs-lookup"><span data-stu-id="509c3-168">Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources.</span></span> <span data-ttu-id="509c3-169">Una volta soddisfatte queste condizioni, chiudere l'handle della porta di completamento I/O chiamando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="509c3-169">After these conditions are satisfied, close the I/O completion port handle by calling the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="509c3-170">In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.</span><span class="sxs-lookup"><span data-stu-id="509c3-170">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="509c3-171">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="509c3-171">Technology</span></span>                                           | <span data-ttu-id="509c3-172">Supportato</span><span class="sxs-lookup"><span data-stu-id="509c3-172">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="509c3-173">Protocollo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="509c3-173">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="509c3-174">Sì</span><span class="sxs-lookup"><span data-stu-id="509c3-174">Yes</span></span><br/> |
| <span data-ttu-id="509c3-175">Failover trasparente SMB 3,0 (failover)</span><span class="sxs-lookup"><span data-stu-id="509c3-175">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="509c3-176">Sì</span><span class="sxs-lookup"><span data-stu-id="509c3-176">Yes</span></span><br/> |
| <span data-ttu-id="509c3-177">SMB 3,0 con condivisioni file di scalabilità orizzontale (quindi)</span><span class="sxs-lookup"><span data-stu-id="509c3-177">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="509c3-178">Sì</span><span class="sxs-lookup"><span data-stu-id="509c3-178">Yes</span></span><br/> |
| <span data-ttu-id="509c3-179">File System Volume condiviso cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="509c3-179">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="509c3-180">Sì</span><span class="sxs-lookup"><span data-stu-id="509c3-180">Yes</span></span><br/> |
| <span data-ttu-id="509c3-181">Resilient file System (ReFS)</span><span class="sxs-lookup"><span data-stu-id="509c3-181">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="509c3-182">Sì</span><span class="sxs-lookup"><span data-stu-id="509c3-182">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="509c3-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="509c3-183">Requirements</span></span>



| <span data-ttu-id="509c3-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="509c3-184">Requirement</span></span> | <span data-ttu-id="509c3-185">Valore</span><span class="sxs-lookup"><span data-stu-id="509c3-185">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="509c3-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="509c3-186">Minimum supported client</span></span><br/> | <span data-ttu-id="509c3-187">App desktop di Windows XP \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="509c3-187">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="509c3-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="509c3-188">Minimum supported server</span></span><br/> | <span data-ttu-id="509c3-189">App UWP per \[ app desktop di Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="509c3-189">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="509c3-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="509c3-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="509c3-191"><dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP (incluso Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="509c3-191"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="509c3-192">Libreria</span><span class="sxs-lookup"><span data-stu-id="509c3-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="509c3-193"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="509c3-193"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="509c3-194">DLL</span><span class="sxs-lookup"><span data-stu-id="509c3-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="509c3-195"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="509c3-195"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="509c3-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="509c3-196">See also</span></span>

<dl> <dt>

<span data-ttu-id="509c3-197">**Argomenti introduttivi**</span><span class="sxs-lookup"><span data-stu-id="509c3-197">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="509c3-198">Funzioni di gestione file</span><span class="sxs-lookup"><span data-stu-id="509c3-198">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="509c3-199">Porte di completamento I/O</span><span class="sxs-lookup"><span data-stu-id="509c3-199">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="509c3-200">Uso delle intestazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="509c3-200">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[<span data-ttu-id="509c3-201">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="509c3-201">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

<span data-ttu-id="509c3-202">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="509c3-202">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="509c3-203">**AcceptEx**</span><span class="sxs-lookup"><span data-stu-id="509c3-203">**AcceptEx**</span></span>](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[<span data-ttu-id="509c3-204">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="509c3-204">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="509c3-205">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="509c3-205">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="509c3-206">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="509c3-206">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="509c3-207">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="509c3-207">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="509c3-208">**PostQueuedCompletionStatus ha provocato**</span><span class="sxs-lookup"><span data-stu-id="509c3-208">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="509c3-209">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="509c3-209">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="509c3-210">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="509c3-210">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

