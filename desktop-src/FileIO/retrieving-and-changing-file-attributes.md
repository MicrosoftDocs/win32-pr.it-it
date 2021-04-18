---
description: Codice di esempio che illustra come usare la funzione GetFileAttributesEx per recuperare gli attributi del file.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Recupero e modifica degli attributi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316280"
---
# <a name="retrieving-and-changing-file-attributes"></a><span data-ttu-id="f8a05-103">Recupero e modifica degli attributi di file</span><span class="sxs-lookup"><span data-stu-id="f8a05-103">Retrieving and Changing File Attributes</span></span>

<span data-ttu-id="f8a05-104">Un'applicazione può recuperare gli attributi del file tramite la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) .</span><span class="sxs-lookup"><span data-stu-id="f8a05-104">An application can retrieve the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function.</span></span> <span data-ttu-id="f8a05-105">Le funzioni [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) possono impostare molti degli attributi.</span><span class="sxs-lookup"><span data-stu-id="f8a05-105">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) functions can set many of the attributes.</span></span> <span data-ttu-id="f8a05-106">Tuttavia, le applicazioni non possono impostare tutti gli attributi.</span><span class="sxs-lookup"><span data-stu-id="f8a05-106">However, applications cannot set all attributes.</span></span>

<span data-ttu-id="f8a05-107">Nell'esempio di codice in questo argomento viene utilizzata la funzione [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) per copiare tutti i file di testo (con estensione txt) nella directory corrente in una nuova directory di file di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f8a05-107">The code example in this topic uses the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) function to copy all text files (.txt) in the current directory to a new directory of read-only files.</span></span> <span data-ttu-id="f8a05-108">I file nella nuova directory vengono modificati in sola lettura, se necessario.</span><span class="sxs-lookup"><span data-stu-id="f8a05-108">Files in the new directory are changed to read only, if necessary.</span></span>

<span data-ttu-id="f8a05-109">L'applicazione crea la directory specificata come parametro tramite la funzione [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="f8a05-109">The application creates the directory specified as a parameter by using the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) function.</span></span> <span data-ttu-id="f8a05-110">La directory non deve esistere già.</span><span class="sxs-lookup"><span data-stu-id="f8a05-110">The directory must not exist already.</span></span>

<span data-ttu-id="f8a05-111">L'applicazione Cerca tutti i file di testo nella directory corrente usando le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="f8a05-111">The application searches the current directory for all text files by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions.</span></span> <span data-ttu-id="f8a05-112">Ogni file di testo viene copiato nella \\ directory TextRO</span><span class="sxs-lookup"><span data-stu-id="f8a05-112">Each text file is copied to the \\TextRO directory.</span></span> <span data-ttu-id="f8a05-113">Dopo la copia di un file, la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) determina se un file è di sola lettura o meno.</span><span class="sxs-lookup"><span data-stu-id="f8a05-113">After a file is copied, the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function determines whether or not a file is read only.</span></span> <span data-ttu-id="f8a05-114">Se il file non è di sola lettura, l'applicazione modifica le directory in \\ TextRO e converte il file copiato in sola lettura tramite la funzione [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="f8a05-114">If the file is not read only, the application changes directories to \\TextRO and converts the copied file to read only by using the [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) function.</span></span>

<span data-ttu-id="f8a05-115">Dopo la copia di tutti i file di testo nella directory corrente, l'applicazione chiude l'handle di ricerca usando la funzione [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="f8a05-115">After all text files in the current directory are copied, the application closes the search handle by using the [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f8a05-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8a05-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8a05-117">**Costanti di attributi file**</span><span class="sxs-lookup"><span data-stu-id="f8a05-117">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> <dt>

[<span data-ttu-id="f8a05-118">Nomi file, percorsi e spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8a05-118">File Names, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



