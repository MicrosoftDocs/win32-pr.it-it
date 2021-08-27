---
description: Codice di esempio che illustra come usare i flussi di file system NTFS di base.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Uso di Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ebb6e2297c82e8643eb79ce66991b32fdf27e46fc723113a2866c79b2f8377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078391"
---
# <a name="using-streams"></a>Uso di Flussi

L'esempio in questo argomento illustra come usare i flussi di file system NTFS di base.

In questo esempio viene creato un file denominato "TestFile" con dimensioni di 16 byte. Tuttavia, il file ha anche un tipo di flusso aggiuntivo ::$DATA, denominato "Stream", che aggiunge altri 23 byte non segnalati dal sistema operativo. Pertanto, quando si visualizza la proprietà delle dimensioni del file, vengono visualizzate solo le dimensioni del flusso predefinito ::$DATA per il file.


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



Se si digita **Digitare TestFile** al prompt dei comandi, viene visualizzato l'output seguente:

``` syntax
This is TestFile
```

Tuttavia, se si digitano le parole **Type TestFile:Stream**, viene generato l'errore seguente:

"Il nome file, il nome della directory o la sintassi dell'etichetta di volume non sono corretti."

Per visualizzare il contenuto di TestFile:stream, usare uno dei comandi seguenti:

**Altre < TestFile:Stream**

**Altre < TestFile:Stream:$DATA**

Il testo visualizzato è il seguente:

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File Flussi](file-streams.md)
</dt> </dl>

 

 



