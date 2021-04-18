---
description: Codice di esempio che illustra come un'applicazione può accodare un file alla fine di un altro file, incluse le modalità di apertura e chiusura dei file, di lettura e scrittura nei file e di blocco e sblocco di file.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Aggiunta di un file a un altro file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546d24fe88a2bbf22c190a0caca3b3f98e753720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312941"
---
# <a name="appending-one-file-to-another-file"></a><span data-ttu-id="41c41-103">Aggiunta di un file a un altro file</span><span class="sxs-lookup"><span data-stu-id="41c41-103">Appending One File to Another File</span></span>

<span data-ttu-id="41c41-104">Nell'esempio di codice in questo argomento viene illustrato come aprire e chiudere i file, leggere e scrivere nei file e bloccare e sbloccare i file.</span><span class="sxs-lookup"><span data-stu-id="41c41-104">The code example in this topic shows you how to open and close files, read and write to files, and lock and unlock files.</span></span>

<span data-ttu-id="41c41-105">Nell'esempio, l'applicazione aggiunge un file alla fine di un altro file.</span><span class="sxs-lookup"><span data-stu-id="41c41-105">In the example, the application appends one file to the end of another file.</span></span> <span data-ttu-id="41c41-106">In primo luogo, l'applicazione apre il file aggiunto con le autorizzazioni che consentono solo all'applicazione di scrivervi.</span><span class="sxs-lookup"><span data-stu-id="41c41-106">First, the application opens the file being appended with permissions that allow only the application to write to it.</span></span> <span data-ttu-id="41c41-107">Tuttavia, durante il processo di Accodamento, altri processi possono aprire il file con l'autorizzazione di sola lettura, che fornisce una visualizzazione snapshot del file accodato.</span><span class="sxs-lookup"><span data-stu-id="41c41-107">However, during the append process other processes can open the file with read-only permission, which provides a snapshot view of the file being appended.</span></span> <span data-ttu-id="41c41-108">Il file viene quindi bloccato durante il processo di Accodamento effettivo per garantire l'integrità dei dati scritti nel file.</span><span class="sxs-lookup"><span data-stu-id="41c41-108">Then, the file is locked during the actual append process to ensure the integrity of the data being written to the file.</span></span>

<span data-ttu-id="41c41-109">Questo esempio non usa le transazioni.</span><span class="sxs-lookup"><span data-stu-id="41c41-109">This example does not use transactions.</span></span> <span data-ttu-id="41c41-110">Se si utilizzano operazioni transazionali, sarà possibile accedere solo in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="41c41-110">If you were using transacted operations, you would only be able have read-only access.</span></span> <span data-ttu-id="41c41-111">In questo caso, verranno visualizzati solo i dati accodati dopo il completamento dell'operazione di commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="41c41-111">In this case, you would only see the appended data after the transaction commit operation completed.</span></span>

<span data-ttu-id="41c41-112">Nell'esempio viene inoltre illustrato che l'applicazione apre due file utilizzando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span><span class="sxs-lookup"><span data-stu-id="41c41-112">The example also shows that the application opens two files by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span></span>

-   <span data-ttu-id="41c41-113">One.txt viene aperto per la lettura.</span><span class="sxs-lookup"><span data-stu-id="41c41-113">One.txt is opened for reading.</span></span>
-   <span data-ttu-id="41c41-114">Two.txt viene aperto per la scrittura e la lettura condivisa.</span><span class="sxs-lookup"><span data-stu-id="41c41-114">Two.txt is opened for writing and shared reading.</span></span>

<span data-ttu-id="41c41-115">L'applicazione usa quindi [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) per aggiungere il contenuto di One.txt alla fine di Two.txt leggendo e scrivendo i blocchi da 4 KB.</span><span class="sxs-lookup"><span data-stu-id="41c41-115">Then the application uses [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to append the contents of One.txt to the end of Two.txt by reading and writing the 4 KB blocks.</span></span> <span data-ttu-id="41c41-116">Tuttavia, prima di scrivere nel secondo file, l'applicazione usa [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) per impostare il puntatore del secondo file alla fine del file e USA [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) per bloccare l'area da scrivere.</span><span class="sxs-lookup"><span data-stu-id="41c41-116">However, before writing to the second file, the application uses [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) to set the pointer of the second file to the end of that file, and uses [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) to lock the area to be written.</span></span> <span data-ttu-id="41c41-117">In questo modo si impedisce a un altro thread o processo con un handle duplicato di accedere all'area mentre è in corso l'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="41c41-117">This prevents another thread or process with a duplicate handle from accessing the area while the write operation is in progress.</span></span> <span data-ttu-id="41c41-118">Al termine di ogni operazione di scrittura, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) viene usato per sbloccare l'area bloccata.</span><span class="sxs-lookup"><span data-stu-id="41c41-118">When each write operation is complete, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) is used to unlock the locked area.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main()
{
  HANDLE hFile;
  HANDLE hAppend;
  DWORD  dwBytesRead, dwBytesWritten, dwPos;
  BYTE   buff[4096];

  // Open the existing file.

  hFile = CreateFile(TEXT("one.txt"), // open One.txt
            GENERIC_READ,             // open for reading
            0,                        // do not share
            NULL,                     // no security
            OPEN_EXISTING,            // existing file only
            FILE_ATTRIBUTE_NORMAL,    // normal file
            NULL);                    // no attr. template

  if (hFile == INVALID_HANDLE_VALUE)
  {
     printf("Could not open One.txt."); 
     return;
  }

  // Open the existing file, or if the file does not exist,
  // create a new file.

  hAppend = CreateFile(TEXT("two.txt"), // open Two.txt
              FILE_APPEND_DATA,         // open for writing
              FILE_SHARE_READ,          // allow multiple readers
              NULL,                     // no security
              OPEN_ALWAYS,              // open or create
              FILE_ATTRIBUTE_NORMAL,    // normal file
              NULL);                    // no attr. template

  if (hAppend == INVALID_HANDLE_VALUE)
  {
     printf("Could not open Two.txt."); 
     return;
  }

  // Append the first file to the end of the second file.
  // Lock the second file to prevent another process from
  // accessing it while writing to it. Unlock the
  // file when writing is complete.

  while (ReadFile(hFile, buff, sizeof(buff), &dwBytesRead, NULL)
      && dwBytesRead > 0)
    {
    dwPos = SetFilePointer(hAppend, 0, NULL, FILE_END);
    LockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    WriteFile(hAppend, buff, dwBytesRead, &dwBytesWritten, NULL);
    UnlockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    }

  // Close both files.

  CloseHandle(hFile);
  CloseHandle(hAppend);
}
```



 

 



