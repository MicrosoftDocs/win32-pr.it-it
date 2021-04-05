---
description: Un'applicazione può monitorare il contenuto di una directory e delle relative sottodirectory usando le notifiche di modifica.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Acquisizione delle notifiche di modifica della directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44375c334c3630aee09bf4a13fc23f87cc91e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753562"
---
# <a name="obtaining-directory-change-notifications"></a><span data-ttu-id="ad67e-103">Acquisizione delle notifiche di modifica della directory</span><span class="sxs-lookup"><span data-stu-id="ad67e-103">Obtaining Directory Change Notifications</span></span>

<span data-ttu-id="ad67e-104">Un'applicazione può monitorare il contenuto di una directory e delle relative sottodirectory usando le notifiche di modifica.</span><span class="sxs-lookup"><span data-stu-id="ad67e-104">An application can monitor the contents of a directory and its subdirectories by using change notifications.</span></span> <span data-ttu-id="ad67e-105">L'attesa di una notifica di modifica è simile alla presenza di un'operazione di lettura in sospeso in una directory e, se necessario, delle relative sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="ad67e-105">Waiting for a change notification is similar to having a read operation pending against a directory and, if necessary, its subdirectories.</span></span> <span data-ttu-id="ad67e-106">Quando viene apportata una modifica all'interno della directory, l'operazione di lettura viene completata.</span><span class="sxs-lookup"><span data-stu-id="ad67e-106">When something changes within the directory being watched, the read operation is completed.</span></span> <span data-ttu-id="ad67e-107">Ad esempio, un'applicazione può usare queste funzioni per aggiornare un elenco di directory ogni volta che viene modificato un nome di file all'interno della directory monitorata.</span><span class="sxs-lookup"><span data-stu-id="ad67e-107">For example, an application can use these functions to update a directory listing whenever a file name within the monitored directory changes.</span></span>

<span data-ttu-id="ad67e-108">Un'applicazione può specificare un set di condizioni che attivano una notifica di modifica tramite la funzione [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="ad67e-108">An application can specify a set of conditions that trigger a change notification by using the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function.</span></span> <span data-ttu-id="ad67e-109">Le condizioni includono modifiche ai nomi di file, nomi di directory, attributi, dimensioni del file, ora dell'ultima scrittura e sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ad67e-109">The conditions include changes to file names, directory names, attributes, file size, time of last write, and security.</span></span> <span data-ttu-id="ad67e-110">Questa funzione restituisce anche un handle che può essere atteso tramite le [funzioni di attesa](/windows/desktop/Sync/wait-functions).</span><span class="sxs-lookup"><span data-stu-id="ad67e-110">This function also returns a handle that can be waited on by using the [wait functions](/windows/desktop/Sync/wait-functions).</span></span> <span data-ttu-id="ad67e-111">Se la condizione di attesa viene soddisfatta, è possibile utilizzare [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) per fornire un handle di notifica per attendere le modifiche successive.</span><span class="sxs-lookup"><span data-stu-id="ad67e-111">If the wait condition is satisfied, [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) can be used to provide a notification handle to wait on subsequent changes.</span></span> <span data-ttu-id="ad67e-112">Tuttavia, queste funzioni non indicano la modifica effettiva che soddisfa la condizione di attesa.</span><span class="sxs-lookup"><span data-stu-id="ad67e-112">However, these functions do not indicate the actual change that satisfied the wait condition.</span></span>

<span data-ttu-id="ad67e-113">Usare [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) per chiudere l'handle di notifica.</span><span class="sxs-lookup"><span data-stu-id="ad67e-113">Use [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) to close the notification handle.</span></span>

<span data-ttu-id="ad67e-114">Per recuperare informazioni sulla modifica specifica come parte della notifica, usare la funzione [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) .</span><span class="sxs-lookup"><span data-stu-id="ad67e-114">To retrieve information about the specific change as part of the notification, use the [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) function.</span></span> <span data-ttu-id="ad67e-115">Questa funzione consente inoltre di fornire una routine di completamento.</span><span class="sxs-lookup"><span data-stu-id="ad67e-115">This function also enables you to provide a completion routine.</span></span>

<span data-ttu-id="ad67e-116">Per tenere traccia delle modifiche apportate a un volume, vedere [Journal](change-journals.md)delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="ad67e-116">To track changes on a volume, see [change journals](change-journals.md).</span></span>

<span data-ttu-id="ad67e-117">Nell'esempio seguente viene monitorato l'albero di directory per le modifiche al nome della directory.</span><span class="sxs-lookup"><span data-stu-id="ad67e-117">The following example monitors the directory tree for directory name changes.</span></span> <span data-ttu-id="ad67e-118">Monitora inoltre una directory per le modifiche del nome file.</span><span class="sxs-lookup"><span data-stu-id="ad67e-118">It also monitors a directory for file name changes.</span></span> <span data-ttu-id="ad67e-119">Nell'esempio viene utilizzata la funzione [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) per creare due handle di notifica e la funzione [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) per attendere gli handle.</span><span class="sxs-lookup"><span data-stu-id="ad67e-119">The example uses the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function to create two notification handles and the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to wait on the handles.</span></span> <span data-ttu-id="ad67e-120">Ogni volta che viene creata o eliminata una directory nella struttura ad albero, l'esempio deve aggiornare l'intero albero di directory.</span><span class="sxs-lookup"><span data-stu-id="ad67e-120">Whenever a directory is created or deleted in the tree, the example should update the entire directory tree.</span></span> <span data-ttu-id="ad67e-121">Ogni volta che un file viene creato o eliminato nella directory, l'esempio dovrebbe aggiornare la directory.</span><span class="sxs-lookup"><span data-stu-id="ad67e-121">Whenever a file is created or deleted in the directory, the example should refresh the directory.</span></span>

> [!Note]
>
> <span data-ttu-id="ad67e-122">Questo esempio semplicistico usa la funzione [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) per la terminazione e la pulizia, ma le applicazioni più complesse devono usare sempre la gestione delle risorse appropriata, ad esempio [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) , laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="ad67e-122">This simplistic example uses the [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) function for termination and cleanup, but more complex applications should always use proper resource management such as [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) where appropriate.</span></span>

 


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>

void RefreshDirectory(LPTSTR);
void RefreshTree(LPTSTR);
void WatchDirectory(LPTSTR);

void _tmain(int argc, TCHAR *argv[])
{
    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
        return;
    }

    WatchDirectory(argv[1]);
}

void WatchDirectory(LPTSTR lpDir)
{
   DWORD dwWaitStatus; 
   HANDLE dwChangeHandles[2]; 
   TCHAR lpDrive[4];
   TCHAR lpFile[_MAX_FNAME];
   TCHAR lpExt[_MAX_EXT];

   _tsplitpath_s(lpDir, lpDrive, 4, NULL, 0, lpFile, _MAX_FNAME, lpExt, _MAX_EXT);

   lpDrive[2] = (TCHAR)'\\';
   lpDrive[3] = (TCHAR)'\0';
 
// Watch the directory for file creation and deletion. 
 
   dwChangeHandles[0] = FindFirstChangeNotification( 
      lpDir,                         // directory to watch 
      FALSE,                         // do not watch subtree 
      FILE_NOTIFY_CHANGE_FILE_NAME); // watch file name changes 
 
   if (dwChangeHandles[0] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 
// Watch the subtree for directory creation and deletion. 
 
   dwChangeHandles[1] = FindFirstChangeNotification( 
      lpDrive,                       // directory to watch 
      TRUE,                          // watch the subtree 
      FILE_NOTIFY_CHANGE_DIR_NAME);  // watch dir name changes 
 
   if (dwChangeHandles[1] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 

// Make a final validation check on our handles.

   if ((dwChangeHandles[0] == NULL) || (dwChangeHandles[1] == NULL))
   {
     printf("\n ERROR: Unexpected NULL from FindFirstChangeNotification.\n");
     ExitProcess(GetLastError()); 
   }

// Change notification is set. Now wait on both notification 
// handles and refresh accordingly. 
 
   while (TRUE) 
   { 
   // Wait for notification.
 
      printf("\nWaiting for notification...\n");

      dwWaitStatus = WaitForMultipleObjects(2, dwChangeHandles, 
         FALSE, INFINITE); 
 
      switch (dwWaitStatus) 
      { 
         case WAIT_OBJECT_0: 
 
         // A file was created, renamed, or deleted in the directory.
         // Refresh this directory and restart the notification.
 
             RefreshDirectory(lpDir); 
             if ( FindNextChangeNotification(dwChangeHandles[0]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_OBJECT_0 + 1: 
 
         // A directory was created, renamed, or deleted.
         // Refresh the tree and restart the notification.
 
             RefreshTree(lpDrive); 
             if (FindNextChangeNotification(dwChangeHandles[1]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_TIMEOUT:

         // A timeout occurred, this would happen if some value other 
         // than INFINITE is used in the Wait call and no changes occur.
         // In a single-threaded environment you might not want an
         // INFINITE wait.
 
            printf("\nNo changes in the timeout period.\n");
            break;

         default: 
            printf("\n ERROR: Unhandled dwWaitStatus.\n");
            ExitProcess(GetLastError());
            break;
      }
   }
}

void RefreshDirectory(LPTSTR lpDir)
{
   // This is where you might place code to refresh your
   // directory listing, but not the subtree because it
   // would not be necessary.

   _tprintf(TEXT("Directory (%s) changed.\n"), lpDir);
}

void RefreshTree(LPTSTR lpDrive)
{
   // This is where you might place code to refresh your
   // directory listing, including the subtree.

   _tprintf(TEXT("Directory tree (%s) changed.\n"), lpDrive);
}
```



 

 
