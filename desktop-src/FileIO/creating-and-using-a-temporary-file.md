---
description: Codice di esempio che illustra come creare un file temporaneo per scopi di manipolazione dei dati tramite le funzioni GetTempFileName e GetTempPath.
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: Creazione e utilizzo di un file temporaneo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca18b7b72aab7c53bea95c38147af66f2b7fef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306644"
---
# <a name="creating-and-using-a-temporary-file"></a><span data-ttu-id="9fb25-103">Creazione e utilizzo di un file temporaneo</span><span class="sxs-lookup"><span data-stu-id="9fb25-103">Creating and Using a Temporary File</span></span>

<span data-ttu-id="9fb25-104">Le applicazioni possono ottenere nomi di file e percorsi univoci per i file temporanei usando le funzioni [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) e [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) .</span><span class="sxs-lookup"><span data-stu-id="9fb25-104">Applications can obtain unique file and path names for temporary files by using the [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) and [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) functions.</span></span> <span data-ttu-id="9fb25-105">La funzione **GetTempFileName** genera un nome file univoco e la funzione **GetTempPath** Recupera il percorso di una directory in cui devono essere creati i file temporanei.</span><span class="sxs-lookup"><span data-stu-id="9fb25-105">The **GetTempFileName** function generates a unique file name, and the **GetTempPath** function retrieves the path to a directory where temporary files should be created.</span></span>

<span data-ttu-id="9fb25-106">Nella procedura seguente viene descritto il modo in cui un'applicazione crea un file temporaneo per scopi di manipolazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="9fb25-106">The following procedure describes how an application creates a temporary file for data manipulation purposes.</span></span>

<span data-ttu-id="9fb25-107">**Per creare e usare un file temporaneo**</span><span class="sxs-lookup"><span data-stu-id="9fb25-107">**To create and use a temporary file**</span></span>

1.  <span data-ttu-id="9fb25-108">L'applicazione apre il file di testo di origine fornito dall'utente tramite [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="9fb25-108">The application opens the user-provided source text file by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span>
2.  <span data-ttu-id="9fb25-109">L'applicazione recupera un percorso e un nome file temporanei utilizzando le funzioni [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) e [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) , quindi utilizza [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per creare il file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="9fb25-109">The application retrieves a temporary file path and file name by using the [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) and [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) functions, and then uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to create the temporary file.</span></span>
3.  <span data-ttu-id="9fb25-110">L'applicazione legge i blocchi di dati di testo in un buffer, converte il contenuto del buffer in maiuscolo usando la funzione [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) e scrive il buffer convertito nel file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="9fb25-110">The application reads blocks of text data into a buffer, converts the buffer contents to uppercase using the [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) function, and writes the converted buffer to the temporary file.</span></span>
4.  <span data-ttu-id="9fb25-111">Quando tutti i file di origine vengono scritti nel file temporaneo, l'applicazione chiude entrambi i file e Rinomina il file temporaneo in "allcaps.txt" utilizzando la funzione [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) .</span><span class="sxs-lookup"><span data-stu-id="9fb25-111">When all of the source file is written to the temporary file, the application closes both files, and renames the temporary file to "allcaps.txt" by using the [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) function.</span></span>

<span data-ttu-id="9fb25-112">Prima di procedere al passaggio successivo, viene verificata l'esito positivo di ognuno dei passaggi precedenti e viene visualizzata una descrizione dell'errore se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="9fb25-112">Each of the previous steps is checked for success before moving to the next step, and a failure description is displayed if an error occurs.</span></span> <span data-ttu-id="9fb25-113">L'applicazione verrà terminata immediatamente dopo la visualizzazione del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="9fb25-113">The application will terminate immediately after displaying the error message.</span></span>

<span data-ttu-id="9fb25-114">Si noti che la manipolazione dei file di testo è stata scelta solo per semplicità di dimostrazione e può essere sostituita con qualsiasi procedura di manipolazione dei dati desiderata.</span><span class="sxs-lookup"><span data-stu-id="9fb25-114">Note that text file manipulation was chosen for ease of demonstration only and can be replaced with any desired data manipulation procedure required.</span></span> <span data-ttu-id="9fb25-115">Il file di dati può essere di qualsiasi tipo di dati, non solo di testo.</span><span class="sxs-lookup"><span data-stu-id="9fb25-115">The data file can be of any data type, not only text.</span></span>

<span data-ttu-id="9fb25-116">La funzione [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) recupera una stringa di percorso completa da una variabile di ambiente, ma non verifica in anticipo l'esistenza del percorso o diritti di accesso appropriati a tale percorso, che è responsabilità dello sviluppatore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9fb25-116">The [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) function retrieves a fully qualified path string from an environment variable but does not check in advance for the existence of the path or adequate access rights to that path, which is the responsibility of the application developer.</span></span> <span data-ttu-id="9fb25-117">Per ulteriori informazioni, vedere [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha).</span><span class="sxs-lookup"><span data-stu-id="9fb25-117">For more information, see [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha).</span></span> <span data-ttu-id="9fb25-118">Nell'esempio seguente un errore viene considerato una condizione terminale e l'applicazione viene chiusa dopo l'invio di un messaggio descrittivo all'output standard.</span><span class="sxs-lookup"><span data-stu-id="9fb25-118">In the following example, an error is regarded as a terminal condition and the application exits after sending a descriptive message to standard output.</span></span> <span data-ttu-id="9fb25-119">Tuttavia, esistono molte altre opzioni, ad esempio richiedere all'utente una directory temporanea o semplicemente provare a utilizzare la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="9fb25-119">However, many other options exist, such as prompting the user for a temporary directory or simply attempting to use the current directory.</span></span>

> [!Note]  
> <span data-ttu-id="9fb25-120">La funzione [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) non richiede l'uso della funzione [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) .</span><span class="sxs-lookup"><span data-stu-id="9fb25-120">The [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) function does not require that the [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) function be used.</span></span>

 

<span data-ttu-id="9fb25-121">Nell'esempio C++ riportato di seguito viene illustrato come creare un file temporaneo per scopi di manipolazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="9fb25-121">The following C++ example shows how to create a temporary file for data manipulation purposes.</span></span>


```C++
//
//  This application opens a file specified by the user and uses
//  a temporary file to convert the file to upper case letters.
//  Note that the given source file is assumed to be an ASCII text file
//  and the new file created is overwritten each time the application is
//  run.
//

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 1024

void PrintError(LPCTSTR errDesc);

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile     = INVALID_HANDLE_VALUE;
    HANDLE hTempFile = INVALID_HANDLE_VALUE; 

    BOOL fSuccess  = FALSE;
    DWORD dwRetVal = 0;
    UINT uRetVal   = 0;

    DWORD dwBytesRead    = 0;
    DWORD dwBytesWritten = 0; 

    TCHAR szTempFileName[MAX_PATH];  
    TCHAR lpTempPathBuffer[MAX_PATH];
    char  chBuffer[BUFSIZE]; 

    LPCTSTR errMsg;

    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <file>\n"), argv[0]);
        return -1;
    }

    //  Opens the existing file. 
    hFile = CreateFile(argv[1],               // file name 
                       GENERIC_READ,          // open for reading 
                       0,                     // do not share 
                       NULL,                  // default security 
                       OPEN_EXISTING,         // existing file only 
                       FILE_ATTRIBUTE_NORMAL, // normal file 
                       NULL);                 // no template 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("First CreateFile failed"));
        return (1);
    } 

     //  Gets the temp path env string (no guarantee it's a valid path).
    dwRetVal = GetTempPath(MAX_PATH,          // length of the buffer
                           lpTempPathBuffer); // buffer for path 
    if (dwRetVal > MAX_PATH || (dwRetVal == 0))
    {
        PrintError(TEXT("GetTempPath failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (2);
    }

    //  Generates a temporary file name. 
    uRetVal = GetTempFileName(lpTempPathBuffer, // directory for tmp files
                              TEXT("DEMO"),     // temp file name prefix 
                              0,                // create unique name 
                              szTempFileName);  // buffer for name 
    if (uRetVal == 0)
    {
        PrintError(TEXT("GetTempFileName failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (3);
    }

    //  Creates the new file to write to for the upper-case version.
    hTempFile = CreateFile((LPTSTR) szTempFileName, // file name 
                           GENERIC_WRITE,        // open for write 
                           0,                    // do not share 
                           NULL,                 // default security 
                           CREATE_ALWAYS,        // overwrite existing
                           FILE_ATTRIBUTE_NORMAL,// normal file 
                           NULL);                // no template 
    if (hTempFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("Second CreateFile failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (4);
    } 

    //  Reads BUFSIZE blocks to the buffer and converts all characters in 
    //  the buffer to upper case, then writes the buffer to the temporary 
    //  file. 
    do 
    {
        if (ReadFile(hFile, chBuffer, BUFSIZE, &dwBytesRead, NULL)) 
        {
            //  Replaces lower case letters with upper case
            //  in place (using the same buffer). The return
            //  value is the number of replacements performed,
            //  which we aren't interested in for this demo.
            CharUpperBuffA(chBuffer, dwBytesRead); 

            fSuccess = WriteFile(hTempFile, 
                                 chBuffer, 
                                 dwBytesRead,
                                 &dwBytesWritten, 
                                 NULL); 
            if (!fSuccess) 
            {
                PrintError(TEXT("WriteFile failed"));
                return (5);
            }
        } 
        else
        {
            PrintError(TEXT("ReadFile failed"));
            return (6);
        }
    //  Continues until the whole file is processed.
    } while (dwBytesRead == BUFSIZE); 

    //  The handles to the files are no longer needed, so
    //  they are closed prior to moving the new file.
    if (!CloseHandle(hFile)) 
    {
       PrintError(TEXT("CloseHandle(hFile) failed"));
       return (7);
    }
    
    if (!CloseHandle(hTempFile)) 
    {
       PrintError(TEXT("CloseHandle(hTempFile) failed"));
       return (8);
    }

    //  Moves the temporary file to the new text file, allowing for differnt
    //  drive letters or volume names.
    fSuccess = MoveFileEx(szTempFileName, 
                          TEXT("AllCaps.txt"), 
                          MOVEFILE_REPLACE_EXISTING | MOVEFILE_COPY_ALLOWED);
    if (!fSuccess)
    { 
        PrintError(TEXT("MoveFileEx failed"));
        return (9);
    }
    else 
        _tprintf(TEXT("All-caps version of %s written to AllCaps.txt\n"), argv[1]);
    return (0);
}

//  ErrorMessage support function.
//  Retrieves the system error message for the GetLastError() code.
//  Note: caller must use LocalFree() on the returned LPCTSTR buffer.
LPCTSTR ErrorMessage(DWORD error) 
{ 
    LPVOID lpMsgBuf;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER 
                   | FORMAT_MESSAGE_FROM_SYSTEM 
                   | FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL,
                  error,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR) &lpMsgBuf,
                  0,
                  NULL);

    return((LPCTSTR)lpMsgBuf);
}

//  PrintError support function.
//  Simple wrapper function for error output.
void PrintError(LPCTSTR errDesc)
{
        LPCTSTR errMsg = ErrorMessage(GetLastError());
        _tprintf(TEXT("\n** ERROR ** %s: %s\n"), errDesc, errMsg);
        LocalFree((LPVOID)errMsg);
}
```



 

 
