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
# <a name="obtaining-directory-change-notifications"></a>Acquisizione delle notifiche di modifica della directory

Un'applicazione può monitorare il contenuto di una directory e delle relative sottodirectory usando le notifiche di modifica. L'attesa di una notifica di modifica è simile alla presenza di un'operazione di lettura in sospeso in una directory e, se necessario, delle relative sottodirectory. Quando viene apportata una modifica all'interno della directory, l'operazione di lettura viene completata. Ad esempio, un'applicazione può usare queste funzioni per aggiornare un elenco di directory ogni volta che viene modificato un nome di file all'interno della directory monitorata.

Un'applicazione può specificare un set di condizioni che attivano una notifica di modifica tramite la funzione [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) . Le condizioni includono modifiche ai nomi di file, nomi di directory, attributi, dimensioni del file, ora dell'ultima scrittura e sicurezza. Questa funzione restituisce anche un handle che può essere atteso tramite le [funzioni di attesa](/windows/desktop/Sync/wait-functions). Se la condizione di attesa viene soddisfatta, è possibile utilizzare [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) per fornire un handle di notifica per attendere le modifiche successive. Tuttavia, queste funzioni non indicano la modifica effettiva che soddisfa la condizione di attesa.

Usare [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) per chiudere l'handle di notifica.

Per recuperare informazioni sulla modifica specifica come parte della notifica, usare la funzione [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) . Questa funzione consente inoltre di fornire una routine di completamento.

Per tenere traccia delle modifiche apportate a un volume, vedere [Journal](change-journals.md)delle modifiche.

Nell'esempio seguente viene monitorato l'albero di directory per le modifiche al nome della directory. Monitora inoltre una directory per le modifiche del nome file. Nell'esempio viene utilizzata la funzione [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) per creare due handle di notifica e la funzione [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) per attendere gli handle. Ogni volta che viene creata o eliminata una directory nella struttura ad albero, l'esempio deve aggiornare l'intero albero di directory. Ogni volta che un file viene creato o eliminato nella directory, l'esempio dovrebbe aggiornare la directory.

> [!Note]
>
> Questo esempio semplicistico usa la funzione [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) per la terminazione e la pulizia, ma le applicazioni più complesse devono usare sempre la gestione delle risorse appropriata, ad esempio [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) , laddove appropriato.

 


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



 

 
