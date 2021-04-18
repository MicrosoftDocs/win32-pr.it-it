---
description: Per condividere i dati, più processi possono usare file mappati alla memoria archiviati dal file di paging del sistema.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Creazione di una memoria condivisa denominata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ac708497ceb12ed099c7a9c0b3788d7a05a925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306587"
---
# <a name="creating-named-shared-memory"></a><span data-ttu-id="cdc97-103">Creazione di una memoria condivisa denominata</span><span class="sxs-lookup"><span data-stu-id="cdc97-103">Creating Named Shared Memory</span></span>

<span data-ttu-id="cdc97-104">Per condividere i dati, più processi possono usare file mappati alla memoria archiviati dal file di paging del sistema.</span><span class="sxs-lookup"><span data-stu-id="cdc97-104">To share data, multiple processes can use memory-mapped files that the system paging file stores.</span></span>

## <a name="first-process"></a><span data-ttu-id="cdc97-105">Primo processo</span><span class="sxs-lookup"><span data-stu-id="cdc97-105">First Process</span></span>

<span data-ttu-id="cdc97-106">Il primo processo crea l'oggetto di mapping dei file chiamando la funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) con il **\_ \_ valore di handle non valido** e un nome per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdc97-106">The first process creates the file mapping object by calling the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with **INVALID\_HANDLE\_VALUE** and a name for the object.</span></span> <span data-ttu-id="cdc97-107">Utilizzando il flag **\_ ReadWrite della pagina** , il processo dispone dell'autorizzazione di lettura/scrittura per la memoria tramite qualsiasi visualizzazione di file creata.</span><span class="sxs-lookup"><span data-stu-id="cdc97-107">By using the **PAGE\_READWRITE** flag, the process has read/write permission to the memory through any file views that are created.</span></span>

<span data-ttu-id="cdc97-108">Il processo usa quindi l'handle dell'oggetto di mapping dei file restituito da [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) in una chiamata a [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) per creare una visualizzazione del file nello spazio degli indirizzi del processo.</span><span class="sxs-lookup"><span data-stu-id="cdc97-108">Then the process uses the file mapping object handle that [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) returns in a call to [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) to create a view of the file in the process address space.</span></span> <span data-ttu-id="cdc97-109">La funzione **MapViewOfFile** restituisce un puntatore alla visualizzazione file `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="cdc97-109">The **MapViewOfFile** function returns a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="cdc97-110">Il processo usa quindi la funzione [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) per scrivere una stringa nella visualizzazione a cui è possibile accedere da altri processi.</span><span class="sxs-lookup"><span data-stu-id="cdc97-110">The process then uses the [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) function to write a string to the view that can be accessed by other processes.</span></span>

<span data-ttu-id="cdc97-111">Il prefisso dei nomi degli oggetti di mapping dei file con "globale \\ " consente ai processi di comunicare tra loro anche se si trovano in sessioni Terminal Server diverse.</span><span class="sxs-lookup"><span data-stu-id="cdc97-111">Prefixing the file mapping object names with "Global\\" allows processes to communicate with each other even if they are in different terminal server sessions.</span></span> <span data-ttu-id="cdc97-112">Questa operazione richiede che il primo processo disponga del privilegio [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc97-112">This requires that the first process must have the [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) privilege.</span></span>

<span data-ttu-id="cdc97-113">Quando il processo non necessita più dell'accesso all'oggetto mapping dei file, deve chiamare la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="cdc97-113">When the process no longer needs access to the file mapping object, it should call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="cdc97-114">Quando tutti gli handle sono chiusi, il sistema può liberare la sezione del file di paging usato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdc97-114">When all handles are closed, the system can free the section of the paging file that the object uses.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");
TCHAR szMsg[]=TEXT("Message from first process.");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = CreateFileMapping(
                 INVALID_HANDLE_VALUE,    // use paging file
                 NULL,                    // default security
                 PAGE_READWRITE,          // read/write access
                 0,                       // maximum object size (high-order DWORD)
                 BUF_SIZE,                // maximum object size (low-order DWORD)
                 szName);                 // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not create file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }
   pBuf = (LPTSTR) MapViewOfFile(hMapFile,   // handle to map object
                        FILE_MAP_ALL_ACCESS, // read/write permission
                        0,
                        0,
                        BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

       CloseHandle(hMapFile);

      return 1;
   }


   CopyMemory((PVOID)pBuf, szMsg, (_tcslen(szMsg) * sizeof(TCHAR)));
    _getch();

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="cdc97-115">Secondo processo</span><span class="sxs-lookup"><span data-stu-id="cdc97-115">Second Process</span></span>

<span data-ttu-id="cdc97-116">Un secondo processo può accedere alla stringa scritta nella memoria condivisa dal primo processo chiamando la funzione [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) specificando lo stesso nome per l'oggetto di mapping del primo processo.</span><span class="sxs-lookup"><span data-stu-id="cdc97-116">A second process can access the string written to the shared memory by the first process by calling the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function specifying the same name for the mapping object as the first process.</span></span> <span data-ttu-id="cdc97-117">Quindi, può usare la funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) per ottenere un puntatore alla visualizzazione file `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="cdc97-117">Then it can use the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to obtain a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="cdc97-118">Il processo può visualizzare questa stringa come qualsiasi altra stringa.</span><span class="sxs-lookup"><span data-stu-id="cdc97-118">The process can display this string as it would any other string.</span></span> <span data-ttu-id="cdc97-119">In questo esempio, la finestra di messaggio visualizzata contiene il messaggio "messaggio dal primo processo" scritto dal primo processo.</span><span class="sxs-lookup"><span data-stu-id="cdc97-119">In this example, the message box displayed contains the message "Message from first process" that was written by the first process.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#pragma comment(lib, "user32.lib")

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = OpenFileMapping(
                   FILE_MAP_ALL_ACCESS,   // read/write access
                   FALSE,                 // do not inherit the name
                   szName);               // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not open file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }

   pBuf = (LPTSTR) MapViewOfFile(hMapFile, // handle to map object
               FILE_MAP_ALL_ACCESS,  // read/write permission
               0,
               0,
               BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

      CloseHandle(hMapFile);

      return 1;
   }

   MessageBox(NULL, pBuf, TEXT("Process2"), MB_OK);

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="cdc97-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdc97-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdc97-121">Condivisione di file e memoria</span><span class="sxs-lookup"><span data-stu-id="cdc97-121">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
</dt> </dl>

 

 
