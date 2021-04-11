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
# <a name="using-streams"></a>Uso di flussi

Nell'esempio riportato in questo argomento viene illustrato come utilizzare i flussi di file system NTFS di base.

Questo esempio crea un file denominato "TestFile" con una dimensione di 16 byte. Tuttavia, il file dispone anche di un tipo di flusso:: $DATA aggiuntivo, denominato "Stream", che aggiunge altri 23 byte non segnalati dal sistema operativo. Pertanto, quando si visualizza la proprietà dimensioni file per il file, vengono visualizzate solo le dimensioni del flusso default:: $DATA per il file.


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



Se si digita **digitare TestFile** al prompt dei comandi, viene visualizzato l'output seguente:

``` syntax
This is TestFile
```

Tuttavia, se si digita il testo **digitare testfile: Stream**, viene generato l'errore seguente:

"La sintassi del nome file, della directory o dell'etichetta di volume non è corretta".

Per visualizzare le informazioni presenti in TestFile: Stream, usare uno dei comandi seguenti:

**Altre < TestFile: Stream**

**Altre < TestFile: Stream: $DATA**

Il testo visualizzato è il seguente:

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flussi di file](file-streams.md)
</dt> </dl>

 

 



