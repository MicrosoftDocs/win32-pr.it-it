---
description: Per leggere da una visualizzazione file, dereferenziare il puntatore restituito dalla funzione MapViewOfFile, come illustrato negli esempi seguenti.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lettura e scrittura da una visualizzazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319445"
---
# <a name="reading-and-writing-from-a-file-view"></a><span data-ttu-id="3deb0-103">Lettura e scrittura da una visualizzazione file</span><span class="sxs-lookup"><span data-stu-id="3deb0-103">Reading and Writing From a File View</span></span>

<span data-ttu-id="3deb0-104">Per leggere da una visualizzazione file, dereferenziare il puntatore restituito dalla funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3deb0-104">To read from a file view, dereference the pointer returned by the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function as shown in the examples below.</span></span>

<span data-ttu-id="3deb0-105">La lettura o la scrittura in una visualizzazione file di un file diverso dal file di paging può causare un'eccezione in un'eccezione **\_ di \_ \_ errore di pagina** .</span><span class="sxs-lookup"><span data-stu-id="3deb0-105">Reading from or writing to a file view of a file other than the page file can cause an **EXCEPTION\_IN\_PAGE\_ERROR** exception.</span></span> <span data-ttu-id="3deb0-106">Se ad esempio si accede a un file mappato che risiede in un server remoto, è possibile che venga generata un'eccezione in caso di perdita della connessione al server.</span><span class="sxs-lookup"><span data-stu-id="3deb0-106">For example, accessing a mapped file that resides on a remote server can generate an exception if the connection to the server is lost.</span></span> <span data-ttu-id="3deb0-107">Le eccezioni possono anche verificarsi a causa di un disco completo, di un errore di dispositivo sottostante o di un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="3deb0-107">Exceptions can also occur because of a full disk, an underlying device failure, or a memory allocation failure.</span></span> <span data-ttu-id="3deb0-108">Quando si scrive in una visualizzazione file, le eccezioni possono anche verificarsi perché il file è condiviso e un altro processo ha bloccato un intervallo di byte.</span><span class="sxs-lookup"><span data-stu-id="3deb0-108">When writing to a file view, exceptions can also occur because the file is shared and a different process has locked a byte range.</span></span> <span data-ttu-id="3deb0-109">Per evitare eccezioni a causa di errori di input e output (I/O), tutti i tentativi di accesso ai file mappati alla memoria devono essere racchiusi in gestori di eccezioni strutturate.</span><span class="sxs-lookup"><span data-stu-id="3deb0-109">To guard against exceptions due to input and output (I/O) errors, all attempts to access memory mapped files should be wrapped in structured exception handlers.</span></span> <span data-ttu-id="3deb0-110">Quando si riceve **un' \_ eccezione \_ nell' \_ errore di pagina** nel filtro **\_ \_ ad eccezione** , assicurarsi che l'indirizzo sia incluso nel mapping a cui si sta effettuando l'accesso.</span><span class="sxs-lookup"><span data-stu-id="3deb0-110">When you receive **EXCEPTION\_IN\_PAGE\_ERROR** in your **\_\_except** filter, make sure that the address is within the mapping you are currently accessing.</span></span> <span data-ttu-id="3deb0-111">In tal caso, ripristinare o non riuscire normalmente; in caso contrario, non gestire l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="3deb0-111">If so, recover or fail gracefully; otherwise, do not handle the exception.</span></span>

<span data-ttu-id="3deb0-112">Nell'esempio seguente viene usato il puntatore restituito da **MapViewOfFile** per leggere dalla visualizzazione file:</span><span class="sxs-lookup"><span data-stu-id="3deb0-112">The following example uses the pointer returned by **MapViewOfFile** to read from the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



<span data-ttu-id="3deb0-113">Nell'esempio seguente viene usato il puntatore restituito da **MapViewOfFile** per scrivere nella visualizzazione file:</span><span class="sxs-lookup"><span data-stu-id="3deb0-113">The following example uses the pointer returned by **MapViewOfFile** to write to the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



<span data-ttu-id="3deb0-114">La funzione [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia il numero specificato di byte della visualizzazione file nel file fisico, senza attendere che si verifichi l'operazione di scrittura memorizzata nella cache:</span><span class="sxs-lookup"><span data-stu-id="3deb0-114">The [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function copies the specified number of bytes of the file view to the physical file, without waiting for the cached write operation to occur:</span></span>


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



<span data-ttu-id="3deb0-115">Se si esegue il mapping di un file compresso o sparse in una partizione NTFS, è possibile che si verifichi un errore di I/O durante il paging in una parte del file.</span><span class="sxs-lookup"><span data-stu-id="3deb0-115">If you are mapping a compressed or sparse file on an NTFS partition, there is additional potential for an I/O error when paging in a portion of the file.</span></span> <span data-ttu-id="3deb0-116">In questo caso, lo spazio degli indirizzi mappato da [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) potrebbe non essere supportato dallo spazio su disco allocato.</span><span class="sxs-lookup"><span data-stu-id="3deb0-116">In this case, the address space mapped by [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) may not be backed by allocated disk space.</span></span> <span data-ttu-id="3deb0-117">Ciò è dovuto al fatto che un file sparse può avere aree di zero per le quali NTFS non alloca spazio su disco e un file compresso può richiedere meno spazio su disco rispetto ai dati effettivi che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="3deb0-117">This is because a sparse file can have regions of zeros for which NTFS does not allocate disk space, and a compressed file can take up less disk space than the actual data that it represents.</span></span> <span data-ttu-id="3deb0-118">Se si leggono o si scrive in una parte di un file sparse o compresso non supportato da spazio su disco, il sistema operativo potrebbe tentare di allocare spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="3deb0-118">If you read from or write to a portion of a sparse or compressed file that is not backed by disk space, the operating system may try to allocate disk space.</span></span> <span data-ttu-id="3deb0-119">Se il disco è pieno, è possibile che venga generata un'eccezione che indica un errore di I/O.</span><span class="sxs-lookup"><span data-stu-id="3deb0-119">If the disk is full, this can result in an exception indicating an I/O error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3deb0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3deb0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3deb0-121">Gestione strutturata delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="3deb0-121">Structured Exception Handling</span></span>](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
