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
# <a name="appending-one-file-to-another-file"></a>Aggiunta di un file a un altro file

Nell'esempio di codice in questo argomento viene illustrato come aprire e chiudere i file, leggere e scrivere nei file e bloccare e sbloccare i file.

Nell'esempio, l'applicazione aggiunge un file alla fine di un altro file. In primo luogo, l'applicazione apre il file aggiunto con le autorizzazioni che consentono solo all'applicazione di scrivervi. Tuttavia, durante il processo di Accodamento, altri processi possono aprire il file con l'autorizzazione di sola lettura, che fornisce una visualizzazione snapshot del file accodato. Il file viene quindi bloccato durante il processo di Accodamento effettivo per garantire l'integrità dei dati scritti nel file.

Questo esempio non usa le transazioni. Se si utilizzano operazioni transazionali, sarà possibile accedere solo in sola lettura. In questo caso, verranno visualizzati solo i dati accodati dopo il completamento dell'operazione di commit della transazione.

Nell'esempio viene inoltre illustrato che l'applicazione apre due file utilizzando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):

-   One.txt viene aperto per la lettura.
-   Two.txt viene aperto per la scrittura e la lettura condivisa.

L'applicazione usa quindi [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) per aggiungere il contenuto di One.txt alla fine di Two.txt leggendo e scrivendo i blocchi da 4 KB. Tuttavia, prima di scrivere nel secondo file, l'applicazione usa [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) per impostare il puntatore del secondo file alla fine del file e USA [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) per bloccare l'area da scrivere. In questo modo si impedisce a un altro thread o processo con un handle duplicato di accedere all'area mentre è in corso l'operazione di scrittura. Al termine di ogni operazione di scrittura, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) viene usato per sbloccare l'area bloccata.


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



 

 



