---
description: L'esempio in questo argomento illustra come creare un processo figlio usando la funzione CreateProcess da un processo console.
ms.assetid: a4e37069-2b3a-4b6d-9cfd-eb1700ab3bc6
title: Creazione di un processo figlio con input e output reindirizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec7c7761bd73386285a4e911be13ff3ab46a479cb78442b1d8b14ac9e1b1368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081441"
---
# <a name="creating-a-child-process-with-redirected-input-and-output"></a>Creazione di un processo figlio con input e output reindirizzati

L'esempio in questo argomento illustra come creare un processo figlio usando la [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) da un processo console. Illustra anche una tecnica per l'uso di pipe anonime per reindirizzare gli handle di input e output standard del processo figlio. Si noti che le named pipe possono essere usate anche per reindirizzare l'I/O del processo.

La [**funzione CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe) usa la [**struttura SECURITY \_ ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) per creare handle ereditabili alle estremità di lettura e scrittura di due pipe. La fine di lettura di una pipe funge da input standard per il processo figlio e la fine di scrittura dell'altra pipe è l'output standard per il processo figlio. Questi handle di pipe vengono specificati nella [**struttura STARTUPINFO,**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) che li rende gli handle standard ereditati dal processo figlio.

Il processo padre usa le estremità opposte di queste due pipe per scrivere nell'input del processo figlio e leggere dall'output del processo figlio. Come specificato nella struttura [**SECURITY \_ ATTRIBUTES,**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) anche questi handle sono ereditabili. Tuttavia, questi handle non devono essere ereditati. Pertanto, prima di creare il processo figlio, il processo padre usa la funzione [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation) per garantire che l'handle di scrittura per l'input standard del processo figlio e l'handle di lettura per l'output standard del processo figlio non siano ereditati. Per altre informazioni, vedere [Pipe.](/windows/desktop/ipc/pipes)

Di seguito è riportato il codice per il processo padre. Accetta un singolo argomento della riga di comando: il nome di un file di testo.


```C++
#include <windows.h> 
#include <tchar.h>
#include <stdio.h> 
#include <strsafe.h>

#define BUFSIZE 4096 
 
HANDLE g_hChildStd_IN_Rd = NULL;
HANDLE g_hChildStd_IN_Wr = NULL;
HANDLE g_hChildStd_OUT_Rd = NULL;
HANDLE g_hChildStd_OUT_Wr = NULL;

HANDLE g_hInputFile = NULL;
 
void CreateChildProcess(void); 
void WriteToPipe(void); 
void ReadFromPipe(void); 
void ErrorExit(PTSTR); 
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   SECURITY_ATTRIBUTES saAttr; 
 
   printf("\n->Start of parent execution.\n");

// Set the bInheritHandle flag so pipe handles are inherited. 
 
   saAttr.nLength = sizeof(SECURITY_ATTRIBUTES); 
   saAttr.bInheritHandle = TRUE; 
   saAttr.lpSecurityDescriptor = NULL; 

// Create a pipe for the child process's STDOUT. 
 
   if ( ! CreatePipe(&g_hChildStd_OUT_Rd, &g_hChildStd_OUT_Wr, &saAttr, 0) ) 
      ErrorExit(TEXT("StdoutRd CreatePipe")); 

// Ensure the read handle to the pipe for STDOUT is not inherited.

   if ( ! SetHandleInformation(g_hChildStd_OUT_Rd, HANDLE_FLAG_INHERIT, 0) )
      ErrorExit(TEXT("Stdout SetHandleInformation")); 

// Create a pipe for the child process's STDIN. 
 
   if (! CreatePipe(&g_hChildStd_IN_Rd, &g_hChildStd_IN_Wr, &saAttr, 0)) 
      ErrorExit(TEXT("Stdin CreatePipe")); 

// Ensure the write handle to the pipe for STDIN is not inherited. 
 
   if ( ! SetHandleInformation(g_hChildStd_IN_Wr, HANDLE_FLAG_INHERIT, 0) )
      ErrorExit(TEXT("Stdin SetHandleInformation")); 
 
// Create the child process. 
   
   CreateChildProcess();

// Get a handle to an input file for the parent. 
// This example assumes a plain text file and uses string output to verify data flow. 
 
   if (argc == 1) 
      ErrorExit(TEXT("Please specify an input file.\n")); 

   g_hInputFile = CreateFile(
       argv[1], 
       GENERIC_READ, 
       0, 
       NULL, 
       OPEN_EXISTING, 
       FILE_ATTRIBUTE_READONLY, 
       NULL); 

   if ( g_hInputFile == INVALID_HANDLE_VALUE ) 
      ErrorExit(TEXT("CreateFile")); 
 
// Write to the pipe that is the standard input for a child process. 
// Data is written to the pipe's buffers, so it is not necessary to wait
// until the child process is running before writing data.
 
   WriteToPipe(); 
   printf( "\n->Contents of %S written to child STDIN pipe.\n", argv[1]);
 
// Read from pipe that is the standard output for child process. 
 
   printf( "\n->Contents of child process STDOUT:\n\n");
   ReadFromPipe(); 

   printf("\n->End of parent execution.\n");

// The remaining open handles are cleaned up when this process terminates. 
// To avoid resource leaks in a larger application, close handles explicitly. 

   return 0; 
} 
 
void CreateChildProcess()
// Create a child process that uses the previously created pipes for STDIN and STDOUT.
{ 
   TCHAR szCmdline[]=TEXT("child");
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bSuccess = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
// This structure specifies the STDIN and STDOUT handles for redirection.
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
   siStartInfo.hStdError = g_hChildStd_OUT_Wr;
   siStartInfo.hStdOutput = g_hChildStd_OUT_Wr;
   siStartInfo.hStdInput = g_hChildStd_IN_Rd;
   siStartInfo.dwFlags |= STARTF_USESTDHANDLES;
 
// Create the child process. 
    
   bSuccess = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   // If an error occurs, exit the application. 
   if ( ! bSuccess ) 
      ErrorExit(TEXT("CreateProcess"));
   else 
   {
      // Close handles to the child process and its primary thread.
      // Some applications might keep these handles to monitor the status
      // of the child process, for example. 

      CloseHandle(piProcInfo.hProcess);
      CloseHandle(piProcInfo.hThread);
      
      // Close handles to the stdin and stdout pipes no longer needed by the child process.
      // If they are not explicitly closed, there is no way to recognize that the child process has ended.
      
      CloseHandle(g_hChildStd_OUT_Wr);
      CloseHandle(g_hChildStd_IN_Rd);
   }
}
 
void WriteToPipe(void) 

// Read from a file and write its contents to the pipe for the child's STDIN.
// Stop when there is no more data. 
{ 
   DWORD dwRead, dwWritten; 
   CHAR chBuf[BUFSIZE];
   BOOL bSuccess = FALSE;
 
   for (;;) 
   { 
      bSuccess = ReadFile(g_hInputFile, chBuf, BUFSIZE, &dwRead, NULL);
      if ( ! bSuccess || dwRead == 0 ) break; 
      
      bSuccess = WriteFile(g_hChildStd_IN_Wr, chBuf, dwRead, &dwWritten, NULL);
      if ( ! bSuccess ) break; 
   } 
 
// Close the pipe handle so the child process stops reading. 
 
   if ( ! CloseHandle(g_hChildStd_IN_Wr) ) 
      ErrorExit(TEXT("StdInWr CloseHandle")); 
} 
 
void ReadFromPipe(void) 

// Read output from the child process's pipe for STDOUT
// and write to the parent process's pipe for STDOUT. 
// Stop when there is no more data. 
{ 
   DWORD dwRead, dwWritten; 
   CHAR chBuf[BUFSIZE]; 
   BOOL bSuccess = FALSE;
   HANDLE hParentStdOut = GetStdHandle(STD_OUTPUT_HANDLE);

   for (;;) 
   { 
      bSuccess = ReadFile( g_hChildStd_OUT_Rd, chBuf, BUFSIZE, &dwRead, NULL);
      if( ! bSuccess || dwRead == 0 ) break; 

      bSuccess = WriteFile(hParentStdOut, chBuf, 
                           dwRead, &dwWritten, NULL);
      if (! bSuccess ) break; 
   } 
} 
 
void ErrorExit(PTSTR lpszFunction) 

// Format a readable error message, display a message box, 
// and exit from the application.
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
        0, NULL );

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR)lpMsgBuf)+lstrlen((LPCTSTR)lpszFunction)+40)*sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR)lpDisplayBuf, TEXT("Error"), MB_OK); 

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
    ExitProcess(1);
}
```



Di seguito è riportato il codice per il processo figlio. Usa gli handle ereditati per STDIN e STDOUT per accedere alla pipe creata dall'elemento padre. Il processo padre legge dal file di input e scrive le informazioni in una pipe. L'elemento figlio riceve testo tramite la pipe usando STDIN e scrive nella pipe tramite STDOUT. L'elemento padre legge dall'estremità di lettura della pipe e visualizza le informazioni nel relativo STDOUT.


```C++
#include <windows.h>
#include <stdio.h>

#define BUFSIZE 4096 
 
int main(void) 
{ 
   CHAR chBuf[BUFSIZE]; 
   DWORD dwRead, dwWritten; 
   HANDLE hStdin, hStdout; 
   BOOL bSuccess; 
 
   hStdout = GetStdHandle(STD_OUTPUT_HANDLE); 
   hStdin = GetStdHandle(STD_INPUT_HANDLE); 
   if ( 
       (hStdout == INVALID_HANDLE_VALUE) || 
       (hStdin == INVALID_HANDLE_VALUE) 
      ) 
      ExitProcess(1); 
 
   // Send something to this process's stdout using printf.
   printf("\n ** This is a message from the child process. ** \n");

   // This simple algorithm uses the existence of the pipes to control execution.
   // It relies on the pipe buffers to ensure that no data is lost.
   // Larger applications would use more advanced process control.

   for (;;) 
   { 
   // Read from standard input and stop on error or no data.
      bSuccess = ReadFile(hStdin, chBuf, BUFSIZE, &dwRead, NULL); 
      
      if (! bSuccess || dwRead == 0) 
         break; 
 
   // Write to standard output and stop on error.
      bSuccess = WriteFile(hStdout, chBuf, dwRead, &dwWritten, NULL); 
      
      if (! bSuccess) 
         break; 
   } 
   return 0;
}
```



 

 
