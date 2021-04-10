---
description: Codice di esempio che illustra come verificare la fine del file durante un'operazione di lettura sincrona e durante un'operazione di lettura asincrona.
ms.assetid: 93fa9e29-1ff1-496d-9551-99ae88ba7253
title: Test per la fine di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e6b60f8e17fc452b0638b820be5978775ea5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967160"
---
# <a name="testing-for-the-end-of-a-file"></a><span data-ttu-id="dbc93-103">Test per la fine di un file</span><span class="sxs-lookup"><span data-stu-id="dbc93-103">Testing for the End of a File</span></span>

<span data-ttu-id="dbc93-104">La funzione [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) verifica la presenza di una condizione di fine file (EOF) in modo diverso per le operazioni di lettura sincrona e asincrona.</span><span class="sxs-lookup"><span data-stu-id="dbc93-104">The [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) function checks for the end-of-file condition (EOF) differently for synchronous and asynchronous read operations.</span></span> <span data-ttu-id="dbc93-105">Quando un'operazione di lettura sincrona raggiunge la fine di un file, **ReadFile** restituisce **true** e imposta la variabile a cui punta il parametro *lpNumberOfBytesRead* su zero.</span><span class="sxs-lookup"><span data-stu-id="dbc93-105">When a synchronous read operation gets to the end of a file, **ReadFile** returns **TRUE** and sets the variable pointed to by the *lpNumberOfBytesRead* parameter to zero.</span></span> <span data-ttu-id="dbc93-106">Un'operazione di lettura asincrona può rilevare la fine di un file durante la chiamata di avvio a **ReadFile** o durante le successive operazioni asincrone se il puntatore del file è avanzato a livello di codice oltre la fine del file.</span><span class="sxs-lookup"><span data-stu-id="dbc93-106">An asynchronous read operation can encounter the end of a file during the initiating call to **ReadFile** or during subsequent asynchronous operations if the file pointer is programmatically advanced beyond the end of the file.</span></span>

<span data-ttu-id="dbc93-107">Nell'esempio C++ riportato di seguito viene illustrato come verificare la fine di un file durante un'operazione di lettura sincrona.</span><span class="sxs-lookup"><span data-stu-id="dbc93-107">The following C++ example shows how to test for the end of a file during a synchronous read operation.</span></span>


```C++
  // Attempt a synchronous read operation.
  bResult = ReadFile(hFile, &inBuffer, nBytesToRead, &nBytesRead, NULL);

  // Check for eof.
  if (bResult &&  nBytesRead == 0) 
   {
    // at the end of the file
   }
```



<span data-ttu-id="dbc93-108">Il test per la fine del file durante un'operazione di lettura asincrona è leggermente più impegnativo rispetto a un'operazione di lettura sincrona simile.</span><span class="sxs-lookup"><span data-stu-id="dbc93-108">The test for end-of-file during an asynchronous read operation is slightly more involved than for a similar synchronous read operation.</span></span> <span data-ttu-id="dbc93-109">L'indicatore di fine del file per le operazioni di lettura asincrona è quando [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) restituisce **false** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **handle di errore \_ \_ EOF**.</span><span class="sxs-lookup"><span data-stu-id="dbc93-109">The end-of-file indicator for asynchronous read operations is when [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_HANDLE\_EOF**.</span></span>

<span data-ttu-id="dbc93-110">Nell'esempio C++ riportato di seguito viene illustrato come verificare la fine del file durante un'operazione di lettura asincrona.</span><span class="sxs-lookup"><span data-stu-id="dbc93-110">The following C++ example shows how to test for the end of file during an asynchronous read operation.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUF_SIZE (61)

LPCTSTR ErrorMessage( DWORD error ) 

// Routine Description:
//      Retrieve the system error message for the last-error code
{ 

    LPVOID lpMsgBuf;

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        error,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    return((LPCTSTR)lpMsgBuf);
}

void GoDoSomethingElse(void)

// Routine Description:
//     Placeholder to demo when async I/O might want to do
//     other processing.
{
    printf("Inside GoDoSomethingElse()\n");
}

DWORD AsyncTestForEnd( HANDLE hEvent, HANDLE hFile )

// Routine Description:
//      Demonstrate async ReadFile operations that can catch
//      End-of-file conditions. Unless the operation completes
//      synchronously or the file size happens to be an exact
//      multiple of BUF_SIZE, this routine will eventually force
//      an EOF condition on any file.

// Parameters:
//      hEvent - pre-made manual-reset event.
//
//      hFile - pre-opened file handle, overlapped.
//
//      inBuffer - the buffer to read in the data to.
//
//      nBytesToRead - how much to read (usually the buffer size).

// Return Value:
//      Number of bytes read.
{
    char inBuffer[BUF_SIZE];
    DWORD nBytesToRead      = BUF_SIZE;
    DWORD dwBytesRead       = 0;
    DWORD dwFileSize        = GetFileSize(hFile, NULL);
    OVERLAPPED stOverlapped = {0};

    DWORD dwError  = 0;
    LPCTSTR errMsg = NULL;

    BOOL bResult   = FALSE;
    BOOL bContinue = TRUE;

    // Set up overlapped structure event. Other members are already 
    // initialized to zero.
    stOverlapped.hEvent = hEvent; 

    // This is an intentionally brute-force loop to force the EOF trigger.
    // A properly designed loop for this simple file read would use the
    // GetFileSize API to regulate execution. However, the purpose here
    // is to demonstrate how to trigger the EOF error and handle it.

    while(bContinue)
    {
        // Default to ending the loop.
        bContinue = FALSE;
        
        // Attempt an asynchronous read operation.
        bResult = ReadFile(hFile,
                           inBuffer,
                           nBytesToRead,
                           &dwBytesRead,
                           &stOverlapped); 
     
        dwError = GetLastError();

        // Check for a problem or pending operation. 
        if (!bResult) 
        { 
            switch (dwError) 
            { 
                 
                case ERROR_HANDLE_EOF:
                {
                    printf("\nReadFile returned FALSE and EOF condition, async EOF not triggered.\n");
                    break;
                }
                case ERROR_IO_PENDING: 
                { 
                    BOOL bPending=TRUE;

                    // Loop until the I/O is complete, that is: the overlapped 
                    // event is signaled.

                    while( bPending )
                    {
                        bPending = FALSE;
                        
                        // Pending asynchronous I/O, do something else
                        // and re-check overlapped structure.
                        printf("\nReadFile operation is pending\n");
     
                        // Do something else then come back to check. 
                        GoDoSomethingElse(); 
     
                        // Check the result of the asynchronous read
                        // without waiting (forth parameter FALSE). 
                        bResult = GetOverlappedResult(hFile,
                                                      &stOverlapped,
                                                      &dwBytesRead,
                                                      FALSE) ; 
     
                        if (!bResult) 
                        { 
                            switch (dwError = GetLastError()) 
                            { 
                                case ERROR_HANDLE_EOF: 
                                { 
                                    // Handle an end of file
                                    printf("GetOverlappedResult found EOF\n");
                                    break;
                                } 

                                case ERROR_IO_INCOMPLETE:
                                {
                                    // Operation is still pending, allow while loop
                                    // to loop again after printing a little progress.
                                    printf("GetOverlappedResult I/O Incomplete\n");
                                    bPending = TRUE;
                                    bContinue = TRUE;
                                    break;
                                }

                                default:
                                {
                                    // Decode any other errors codes.
                                    errMsg = ErrorMessage(dwError);
                                    _tprintf(TEXT("GetOverlappedResult failed (%d): %s\n"), 
                                        dwError, errMsg);
                                    LocalFree((LPVOID)errMsg);
                                }
                            }
                        } 
                        else
                        {
                            printf("ReadFile operation completed\n");

                            // Manual-reset event should be reset since it is now signaled.
                            ResetEvent(stOverlapped.hEvent);
                        }
                    }
                    break;
                }

                default:
                {
                    // Decode any other errors codes.
                    errMsg = ErrorMessage(dwError);
                    printf("ReadFile GLE unhandled (%d): %s\n", dwError, errMsg); 
                    LocalFree((LPVOID)errMsg);
                    break;
                }
            }
        }
        else
        {
            // EOF demo did not trigger for the given file.
            // Note that system caching may cause this condition on most files
            // after the first read. CreateFile can be called using the
            // FILE_FLAG_NOBUFFERING parameter but it would require reads are
            // always aligned to the volume's sector boundary. This is beyond
            // the scope of this example. See comments in the main() function.

            printf("ReadFile completed synchronously\n");
        }

        // The following operation assumes the file is not extremely large, otherwise 
        // logic would need to be included to adequately account for very large
        // files and manipulate the OffsetHigh member of the OVERLAPPED structure.

        stOverlapped.Offset += dwBytesRead;
        if ( stOverlapped.Offset < dwFileSize )             
            bContinue = TRUE;
    }

    return stOverlapped.Offset;
}

int __cdecl _tmain(int argc, TCHAR *argv[])

// To force an EOF condition, execute this application specifying a
// zero-length file. This is because the offset (file pointer) must be
// at or beyond the end-of-file marker when ReadFile is called. For
// more information, see the comments for the AsyncTestForEnd routine.

{
    HANDLE hEvent;
    HANDLE hFile;
    DWORD dwReturnValue;

    printf("\n");
    if( argc != 2 )
    {
        printf("ERROR:\tIncorrect number of arguments\n\n");
        printf("%s <file_name>\n", argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],                // file to open
                       GENERIC_READ,           // open for reading
                       FILE_SHARE_READ,        // share for reading
                       NULL,                   // default security
                       OPEN_EXISTING,          // existing file only
                       FILE_FLAG_OVERLAPPED,   // overlapped operation
                       NULL);                  // no attr. template
 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DWORD dwError = GetLastError();
        LPCTSTR errMsg = ErrorMessage(dwError);
        printf("Could not open file (%d): %s\n", dwError, errMsg); 
        LocalFree((LPVOID)errMsg);
        return; 
    }

    hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

    if (hEvent == NULL) 
    { 
        DWORD dwError = GetLastError();
        LPCTSTR errMsg = ErrorMessage(dwError);
        printf("Could not CreateEvent: %d %s\n", dwError, errMsg); 
        LocalFree((LPVOID)errMsg);
        return; 
    }

    dwReturnValue = AsyncTestForEnd(hEvent, hFile);

    printf( "\nRead complete. Bytes read: %d\n", dwReturnValue);

    CloseHandle(hFile);
    CloseHandle(hEvent);
}
```



<span data-ttu-id="dbc93-111">L'output di questo codice di esempio è il seguente.</span><span class="sxs-lookup"><span data-stu-id="dbc93-111">The output from this sample code is as follows.</span></span>

``` syntax
ReadFile operation is pending
Inside GoDoSomethingElse()
GetOverlappedResult I/O Incomplete

ReadFile operation is pending
Inside GoDoSomethingElse()
ReadFile operation completed

Complete. Bytes read: 541
```

 

 
