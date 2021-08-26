---
description: Per condividere i dati, più processi possono usare file mappati alla memoria archiviati dal file di paging di sistema.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Creazione di memoria condivisa denominata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc5ec3d9865d310807d01ac9f76967d4378fc92e4c9588d00b2933a08c953f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869921"
---
# <a name="creating-named-shared-memory"></a>Creazione di memoria condivisa denominata

Per condividere i dati, più processi possono usare file mappati alla memoria archiviati dal file di paging di sistema.

## <a name="first-process"></a>Primo processo

Il primo processo crea l'oggetto mapping di file chiamando la [**funzione CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) con **INVALID HANDLE \_ \_ VALUE** e un nome per l'oggetto. Usando il flag **PAGE \_ READWRITE,** il processo dispone dell'autorizzazione di lettura/scrittura per la memoria tramite qualsiasi visualizzazione file creata.

Il processo usa quindi l'handle dell'oggetto mapping di file restituito da [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) in una chiamata a [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) per creare una visualizzazione del file nello spazio degli indirizzi del processo. La **funzione MapViewOfFile** restituisce un puntatore alla visualizzazione file, `pBuf` . Il processo usa quindi la [**funzione CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) per scrivere una stringa nella vista accessibile da altri processi.

Il prefisso "Global" per i nomi degli oggetti di mapping dei file consente ai processi di comunicare tra loro anche se si \\ verificano in sessioni di terminal server diverse. A questo scopo, è necessario che il primo processo abbia [**il privilegio SeCreateGlobalPrivilege.**](../secauthz/privilege-constants.md)

Quando il processo non necessita più dell'accesso all'oggetto di mapping dei file, deve chiamare la [**funzione CloseHandle.**](/windows/win32/api/handleapi/nf-handleapi-closehandle) Quando tutti gli handle vengono chiusi, il sistema può liberare la sezione del file di paging utilizzata dall'oggetto .


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



## <a name="second-process"></a>Secondo processo

Un secondo processo può accedere alla stringa scritta nella memoria condivisa dal primo processo chiamando la funzione [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) specificando lo stesso nome del primo processo per l'oggetto mapping. Può quindi usare la [**funzione MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) per ottenere un puntatore alla visualizzazione file, `pBuf` . Il processo può visualizzare questa stringa come qualsiasi altra stringa. In questo esempio la finestra di messaggio visualizzata contiene il messaggio "Message from first process" scritto dal primo processo.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Condivisione di file e memoria](sharing-files-and-memory.md)
</dt> </dl>

 

 
