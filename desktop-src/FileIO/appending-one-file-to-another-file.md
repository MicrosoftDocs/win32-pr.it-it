---
description: Codice di esempio che illustra come un'applicazione può aggiungere un file alla fine di un altro file, tra cui come aprire e chiudere i file, leggere e scrivere nei file e bloccare e sbloccare i file.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Aggiunta di un file a un altro file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585521c1d0bb85c41806ba83c2c0940dc3523035731279d4da3f06af45334984
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766229"
---
# <a name="appending-one-file-to-another-file"></a>Aggiunta di un file a un altro file

L'esempio di codice in questo argomento illustra come aprire e chiudere file, leggere e scrivere nei file e come bloccare e sbloccare i file.

Nell'esempio, l'applicazione aggiunge un file alla fine di un altro file. In primo luogo, l'applicazione apre il file a cui vengono aggiunte le autorizzazioni che consentono solo all'applicazione di scrivere in esso. Durante il processo di accodamento, tuttavia, altri processi possono aprire il file con l'autorizzazione di sola lettura, che fornisce una visualizzazione snapshot del file aggiunto. Il file viene quindi bloccato durante il processo di accodamento effettivo per garantire l'integrità dei dati scritti nel file.

In questo esempio non vengono utilizzate transazioni. Se si usavano operazioni transazione, sarebbe possibile accedere solo in sola lettura. In questo caso, i dati accodati verranno visualizzati solo dopo il completamento dell'operazione di commit della transazione.

L'esempio mostra anche che l'applicazione apre due file usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):

-   One.txt viene aperto per la lettura.
-   Two.txt viene aperto per la scrittura e la lettura condivisa.

L'applicazione usa [**quindi ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) per aggiungere il contenuto di One.txt alla fine del Two.txt leggendo e scrivendo i blocchi da 4 KB. Tuttavia, prima di scrivere nel secondo file, l'applicazione usa [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) per impostare il puntatore del secondo file alla fine del file e usa [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) per bloccare l'area da scrivere. In questo modo si impedisce a un altro thread o processo con un handle duplicato di accedere all'area mentre è in corso l'operazione di scrittura. Al termine di ogni operazione di scrittura, [**viene usato UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) per sbloccare l'area bloccata.


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



 

 



