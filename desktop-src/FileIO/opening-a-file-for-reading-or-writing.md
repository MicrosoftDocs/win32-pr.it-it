---
description: Codice di esempio che illustra come utilizzare la funzione CreateFile per creare un nuovo file o aprire un file esistente.
ms.assetid: 04e089a7-c559-4a35-a38b-e1acdf3438d1
title: Apertura di un file per la lettura o la scrittura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254684538a64a37cd94841812df84808da8374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752823"
---
# <a name="opening-a-file-for-reading-or-writing"></a><span data-ttu-id="4948b-103">Apertura di un file per la lettura o la scrittura</span><span class="sxs-lookup"><span data-stu-id="4948b-103">Opening a File for Reading or Writing</span></span>

<span data-ttu-id="4948b-104">La funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) può creare un nuovo file o aprire un file esistente.</span><span class="sxs-lookup"><span data-stu-id="4948b-104">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function can create a new file or open an existing file.</span></span> <span data-ttu-id="4948b-105">È necessario specificare il nome del file, le istruzioni per la creazione e altri attributi.</span><span class="sxs-lookup"><span data-stu-id="4948b-105">You must specify the file name, creation instructions, and other attributes.</span></span> <span data-ttu-id="4948b-106">Quando un'applicazione crea un nuovo file, il sistema operativo lo aggiunge alla directory specificata.</span><span class="sxs-lookup"><span data-stu-id="4948b-106">When an application creates a new file, the operating system adds it to the specified directory.</span></span>

## <a name="example-open-a-file-for-writing"></a><span data-ttu-id="4948b-107">Esempio: aprire un file per la scrittura</span><span class="sxs-lookup"><span data-stu-id="4948b-107">Example: Open a File for Writing</span></span>

<span data-ttu-id="4948b-108">Nell'esempio seguente viene utilizzato [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per creare un nuovo file e aprirlo per scrivere e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) per scrivere una stringa semplice in modo sincrono nel file.</span><span class="sxs-lookup"><span data-stu-id="4948b-108">The following example uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to create a new file and open it for writing and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to write a simple string synchronously to the file.</span></span>

<span data-ttu-id="4948b-109">Una chiamata successiva per aprire il file con [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avrà esito negativo fino a quando l'handle non viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="4948b-109">A subsequent call to open this file with [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) will fail until the handle is closed.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void DisplayError(LPTSTR lpszFunction);

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    char DataBuffer[] = "This is some test data to write to the file.";
    DWORD dwBytesToWrite = (DWORD)strlen(DataBuffer);
    DWORD dwBytesWritten = 0;
    BOOL bErrorFlag = FALSE;

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error:\tIncorrect number of arguments\n\n");
        _tprintf(TEXT("%s <file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],                // name of the write
                       GENERIC_WRITE,          // open for writing
                       0,                      // do not share
                       NULL,                   // default security
                       CREATE_NEW,             // create new file only
                       FILE_ATTRIBUTE_NORMAL,  // normal file
                       NULL);                  // no attr. template

    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: Unable to open file \"%s\" for write.\n"), argv[1]);
        return;
    }

    _tprintf(TEXT("Writing %d bytes to %s.\n"), dwBytesToWrite, argv[1]);

    bErrorFlag = WriteFile( 
                    hFile,           // open file handle
                    DataBuffer,      // start of data to write
                    dwBytesToWrite,  // number of bytes to write
                    &dwBytesWritten, // number of bytes that were written
                    NULL);            // no overlapped structure

    if (FALSE == bErrorFlag)
    {
        DisplayError(TEXT("WriteFile"));
        printf("Terminal failure: Unable to write to file.\n");
    }
    else
    {
        if (dwBytesWritten != dwBytesToWrite)
        {
            // This is an error because a synchronous write that results in
            // success (WriteFile returns TRUE) should write all data as
            // requested. This would not necessarily be the case for
            // asynchronous writes.
            printf("Error: dwBytesWritten != dwBytesToWrite\n");
        }
        else
        {
            _tprintf(TEXT("Wrote %d bytes to %s successfully.\n"), dwBytesWritten, argv[1]);
        }
    }

    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
```



## <a name="example-open-a-file-for-reading"></a><span data-ttu-id="4948b-110">Esempio: aprire un file per la lettura</span><span class="sxs-lookup"><span data-stu-id="4948b-110">Example: Open a File for Reading</span></span>

<span data-ttu-id="4948b-111">Nell'esempio seguente viene utilizzato [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire un file esistente per la lettura e [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) per leggere in modo sincrono fino a 80 caratteri dal file.</span><span class="sxs-lookup"><span data-stu-id="4948b-111">The following example uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open an existing file for reading and [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) to read up to 80 characters synchronously from the file.</span></span>

<span data-ttu-id="4948b-112">In questo caso, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ha esito positivo solo se il file specificato esiste già nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="4948b-112">In this case, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) succeeds only if the specified file already exists in the current directory.</span></span> <span data-ttu-id="4948b-113">Una chiamata successiva per aprire il file con **CreateFile** avrà esito positivo se la chiamata utilizza le stesse modalità di accesso e condivisione.</span><span class="sxs-lookup"><span data-stu-id="4948b-113">A subsequent call to open this file with **CreateFile** will succeed if the call uses the same access and sharing modes.</span></span>

<span data-ttu-id="4948b-114">Suggerimento: per testare questo esempio, è possibile usare il file creato con l'esempio precedente di WriteFile.</span><span class="sxs-lookup"><span data-stu-id="4948b-114">Tip: You can use the file you created with the previous WriteFile example to test this example.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFFERSIZE 5
DWORD g_BytesTransferred = 0;

void DisplayError(LPTSTR lpszFunction);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped
);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped )
 {
  _tprintf(TEXT("Error code:\t%x\n"), dwErrorCode);
  _tprintf(TEXT("Number of bytes:\t%x\n"), dwNumberOfBytesTransfered);
  g_BytesTransferred = dwNumberOfBytesTransfered;
 }

//
// Note: this simplified sample assumes the file to read is an ANSI text file
// only for the purposes of output to the screen. CreateFile and ReadFile
// do not use parameters to differentiate between text and binary file types.
//

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    DWORD  dwBytesRead = 0;
    char   ReadBuffer[BUFFERSIZE] = {0};
    OVERLAPPED ol = {0};

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error: Incorrect number of arguments\n\n");
        _tprintf(TEXT("Usage:\n\t%s <text_file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],               // file to open
                       GENERIC_READ,          // open for reading
                       FILE_SHARE_READ,       // share for reading
                       NULL,                  // default security
                       OPEN_EXISTING,         // existing file only
                       FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED, // normal file
                       NULL);                 // no attr. template
 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: unable to open file \"%s\" for read.\n"), argv[1]);
        return; 
    }

    // Read one character less than the buffer size to save room for
    // the terminating NULL character. 

    if( FALSE == ReadFileEx(hFile, ReadBuffer, BUFFERSIZE-1, &ol, FileIOCompletionRoutine) )
    {
        DisplayError(TEXT("ReadFile"));
        printf("Terminal failure: Unable to read from file.\n GetLastError=%08x\n", GetLastError());
        CloseHandle(hFile);
        return;
    }
    SleepEx(5000, TRUE);
    dwBytesRead = g_BytesTransferred;
    // This is the section of code that assumes the file is ANSI text. 
    // Modify this block for other data types if needed.

    if (dwBytesRead > 0 && dwBytesRead <= BUFFERSIZE-1)
    {
        ReadBuffer[dwBytesRead]='\0'; // NULL character

        _tprintf(TEXT("Data read from %s (%d bytes): \n"), argv[1], dwBytesRead);
        printf("%s\n", ReadBuffer);
    }
    else if (dwBytesRead == 0)
    {
        _tprintf(TEXT("No data read from file %s\n"), argv[1]);
    }
    else
    {
        printf("\n ** Unexpected value for dwBytesRead ** \n");
    }

    // It is always good practice to close the open file handles even though
    // the app will exit here and clean up open handles anyway.
    
    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}

```



## <a name="related-topics"></a><span data-ttu-id="4948b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4948b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4948b-116">Creazione e apertura di file</span><span class="sxs-lookup"><span data-stu-id="4948b-116">Creating and Opening Files</span></span>](creating-and-opening-files.md)
</dt> </dl>

 

 



