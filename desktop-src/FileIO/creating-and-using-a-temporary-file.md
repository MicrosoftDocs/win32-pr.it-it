---
description: Codice di esempio che illustra come creare un file temporaneo a scopo di manipolazione dei dati usando le funzioni GetTempFileName e GetTempPath.
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: Creazione e utilizzo di un file temporaneo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f242b9b021744c42e7e1b8745c7eec2b6388249246872192ecfd6308bdab55af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650421"
---
# <a name="creating-and-using-a-temporary-file"></a>Creazione e utilizzo di un file temporaneo

Le applicazioni possono ottenere nomi di file e percorsi univoci per i file temporanei usando [**le funzioni GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) [**e GetTempPath.**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) La **funzione GetTempFileName** genera un nome file univoco e la **funzione GetTempPath** recupera il percorso di una directory in cui devono essere creati i file temporanei.

La procedura seguente descrive come un'applicazione crea un file temporaneo a scopo di manipolazione dei dati.

**Per creare e usare un file temporaneo**

1.  L'applicazione apre il file di testo di origine fornito dall'utente usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
2.  L'applicazione recupera un percorso e un nome file temporanei usando le funzioni [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) e [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) e quindi usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per creare il file temporaneo.
3.  L'applicazione legge blocchi di dati di testo in un buffer, converte il contenuto del buffer in caratteri maiuscoli usando la [funzione CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) e scrive il buffer convertito nel file temporaneo.
4.  Quando tutto il file di origine viene scritto nel file temporaneo, l'applicazione chiude entrambi i file e rinomina il file temporaneo in "allcaps.txt" usando la funzione [**MoveFileEx.**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)

Prima di passare al passaggio successivo, viene verificata l'esito positivo di ognuno dei passaggi precedenti. Se si verifica un errore, viene visualizzata una descrizione dell'errore. L'applicazione verrà terminata immediatamente dopo la visualizzazione del messaggio di errore.

Si noti che la modifica del file di testo è stata scelta solo per semplificare la dimostrazione e può essere sostituita con qualsiasi procedura di manipolazione dei dati desiderata. Il file di dati può essere di qualsiasi tipo, non solo di testo.

La [**funzione GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) recupera una stringa di percorso completa da una variabile di ambiente, ma non verifica in anticipo l'esistenza del percorso o i diritti di accesso adeguati a tale percorso, responsabilità dello sviluppatore dell'applicazione. Per altre informazioni, vedere [**GetTempPath.**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) Nell'esempio seguente un errore viene considerato una condizione terminale e l'applicazione viene chiusa dopo l'invio di un messaggio descrittivo all'output standard. Esistono tuttavia molte altre opzioni, ad esempio la richiesta all'utente di una directory temporanea o semplicemente il tentativo di usare la directory corrente.

> [!Note]  
> La [**funzione GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) non richiede l'uso della funzione [**GetTempPath.**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)

 

Nell'esempio C++ seguente viene illustrato come creare un file temporaneo a scopo di manipolazione dei dati.


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



 

 
