---
description: Codice di esempio che illustra come usare i flussi di file system NTFS di base.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Uso di flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc73a3524d45eeead4cd6c0d508925e6caa5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232872"
---
# <a name="using-streams"></a><span data-ttu-id="eed32-103">Uso di flussi</span><span class="sxs-lookup"><span data-stu-id="eed32-103">Using Streams</span></span>

<span data-ttu-id="eed32-104">Nell'esempio riportato in questo argomento viene illustrato come utilizzare i flussi di file system NTFS di base.</span><span class="sxs-lookup"><span data-stu-id="eed32-104">The example in this topic demonstrates how to use basic NTFS file system streams.</span></span>

<span data-ttu-id="eed32-105">Questo esempio crea un file denominato "TestFile" con una dimensione di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="eed32-105">This example creates a file, called "TestFile," with a size of 16 bytes.</span></span> <span data-ttu-id="eed32-106">Tuttavia, il file dispone anche di un tipo di flusso:: $DATA aggiuntivo, denominato "Stream", che aggiunge altri 23 byte non segnalati dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eed32-106">However, the file also has an additional ::$DATA stream type, named "Stream" which adds an additional 23 bytes that is not reported by the operating system.</span></span> <span data-ttu-id="eed32-107">Pertanto, quando si visualizza la proprietà dimensioni file per il file, vengono visualizzate solo le dimensioni del flusso default:: $DATA per il file.</span><span class="sxs-lookup"><span data-stu-id="eed32-107">Therefore, when you view the file size property for the file, you see only the size of default ::$DATA stream for the file.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main( )
 {
  HANDLE hFile, hStream;
  DWORD dwRet;

  hFile = CreateFile( TEXT("TestFile"), // Filename
                      GENERIC_WRITE,    // Desired access
                      FILE_SHARE_WRITE, // Share flags
                      NULL,             // Security Attributes
                      OPEN_ALWAYS,      // Creation Disposition
                      0,                // Flags and Attributes
                      NULL );           // OVERLAPPED pointer
  if( hFile == INVALID_HANDLE_VALUE )
   {
    printf( "Cannot open TestFile\n" );
    return;
   }
  else
   {
    WriteFile( hFile,              // Handle
               "This is TestFile", // Data to be written
               16,                 // Size of data, in bytes
               &dwRet,             // Number of bytes written
               NULL );             // OVERLAPPED pointer
    CloseHandle( hFile );
    hFile = INVALID_HANDLE_VALUE;
   }

  hStream = CreateFile( TEXT("TestFile:Stream"), // Filename
                        GENERIC_WRITE,           // Desired access
                        FILE_SHARE_WRITE,        // Share flags
                        NULL,                    // Security Attributes
                        OPEN_ALWAYS,             // Creation Disposition
                        0,                       // Flags and Attributes
                        NULL );                  // OVERLAPPED pointer
  if( hStream == INVALID_HANDLE_VALUE )
    printf( "Cannot open TestFile:Stream\n" );
  else
   {
    WriteFile( hStream,                   // Handle
               "This is TestFile:Stream", // Data to be written
               23,                        // Size of data
               &dwRet,                    // Number of bytes written
               NULL);                     // OVERLAPPED pointer
    CloseHandle( hStream );
    hStream = INVALID_HANDLE_VALUE;
   }
}
```



<span data-ttu-id="eed32-108">Se si digita **digitare TestFile** al prompt dei comandi, viene visualizzato l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="eed32-108">If you type **Type TestFile** at a command prompt, it displays the following output:</span></span>

``` syntax
This is TestFile
```

<span data-ttu-id="eed32-109">Tuttavia, se si digita il testo **digitare testfile: Stream**, viene generato l'errore seguente:</span><span class="sxs-lookup"><span data-stu-id="eed32-109">However, if you type the words **Type TestFile:Stream**, it generates the following error:</span></span>

<span data-ttu-id="eed32-110">"La sintassi del nome file, della directory o dell'etichetta di volume non è corretta".</span><span class="sxs-lookup"><span data-stu-id="eed32-110">"The filename, directory name, or volume label syntax is incorrect."</span></span>

<span data-ttu-id="eed32-111">Per visualizzare le informazioni presenti in TestFile: Stream, usare uno dei comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="eed32-111">To view what is in TestFile:stream, use one of the following commands:</span></span>

<span data-ttu-id="eed32-112">**Altre < TestFile: Stream**</span><span class="sxs-lookup"><span data-stu-id="eed32-112">**More < TestFile:Stream**</span></span>

<span data-ttu-id="eed32-113">**Altre < TestFile: Stream: $DATA**</span><span class="sxs-lookup"><span data-stu-id="eed32-113">**More < TestFile:Stream:$DATA**</span></span>

<span data-ttu-id="eed32-114">Il testo visualizzato è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eed32-114">The text displayed is as follows:</span></span>

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a><span data-ttu-id="eed32-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eed32-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eed32-116">Flussi di file</span><span class="sxs-lookup"><span data-stu-id="eed32-116">File Streams</span></span>](file-streams.md)
</dt> </dl>

 

 



