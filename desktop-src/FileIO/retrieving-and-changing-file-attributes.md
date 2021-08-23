---
description: Codice di esempio che illustra come usare la funzione GetFileAttributesEx per recuperare gli attributi del file.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Recupero e modifica degli attributi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2609030d1657b78c266ed6b10841159e0df4d40a2e3b07b0fce42e98b45d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015139"
---
# <a name="retrieving-and-changing-file-attributes"></a>Recupero e modifica degli attributi di file

Un'applicazione può recuperare gli attributi del file usando [**la funzione GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) [**o GetFileAttributesEx.**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) Le [**funzioni CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**e SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) possono impostare molti attributi. Tuttavia, le applicazioni non possono impostare tutti gli attributi.

L'esempio di codice in questo argomento usa la funzione [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) per copiare tutti i file di testo (.txt) nella directory corrente in una nuova directory di file di sola lettura. I file nella nuova directory vengono modificati in sola lettura, se necessario.

L'applicazione crea la directory specificata come parametro usando la [**funzione CreateDirectory.**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) La directory non deve esistere già.

L'applicazione cerca tutti i file di testo nella directory corrente usando le [**funzioni FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) [**e FindNextFile.**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) Ogni file di testo viene copiato nella \\ directory TextRO. Dopo la copia di un file, [**la funzione GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) determina se un file è di sola lettura o meno. Se il file non è di sola lettura, l'applicazione cambia directory in TextRO e converte il file copiato in sola lettura usando \\ la [**funzione SetFileAttributes.**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)

Dopo aver copiato tutti i file di testo nella directory corrente, l'applicazione chiude l'handle di ricerca usando la [**funzione FindClose.**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void _tmain(int argc, TCHAR* argv[])
{
   WIN32_FIND_DATA FileData;
   HANDLE          hSearch;
   DWORD           dwAttrs;
   TCHAR           szNewPath[MAX_PATH];   
 
   BOOL            fFinished = FALSE; 

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }
 
// Create a new directory. 
 
   if (!CreateDirectory(argv[1], NULL)) 
   { 
      printf("CreateDirectory failed (%d)\n", GetLastError()); 
      return;
   } 
 
// Start searching for text files in the current directory. 
 
   hSearch = FindFirstFile(TEXT("*.txt"), &FileData); 
   if (hSearch == INVALID_HANDLE_VALUE) 
   { 
      printf("No text files found.\n"); 
      return;
   } 
 
// Copy each .TXT file to the new directory 
// and change it to read only, if not already. 
 
   while (!fFinished) 
   { 
      StringCchPrintf(szNewPath, sizeof(szNewPath)/sizeof(szNewPath[0]), TEXT("%s\\%s"), argv[1], FileData.cFileName);

      if (CopyFile(FileData.cFileName, szNewPath, FALSE))
      { 
         dwAttrs = GetFileAttributes(FileData.cFileName); 
         if (dwAttrs==INVALID_FILE_ATTRIBUTES) return; 

         if (!(dwAttrs & FILE_ATTRIBUTE_READONLY)) 
         { 
            SetFileAttributes(szNewPath, 
                dwAttrs | FILE_ATTRIBUTE_READONLY); 
         } 
      } 
      else 
      { 
         printf("Could not copy file.\n"); 
         return;
      } 
 
      if (!FindNextFile(hSearch, &FileData)) 
      {
         if (GetLastError() == ERROR_NO_MORE_FILES) 
         { 
            _tprintf(TEXT("Copied *.txt to %s\n"), argv[1]); 
            fFinished = TRUE; 
         } 
         else 
         { 
            printf("Could not find next file.\n"); 
            return;
         } 
      }
   } 
 
// Close the search handle. 
 
   FindClose(hSearch);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti di attributi file**](file-attribute-constants.md)
</dt> <dt>

[Nomi di file, percorsi e spazi dei nomi](naming-a-file.md)
</dt> </dl>

 

 



