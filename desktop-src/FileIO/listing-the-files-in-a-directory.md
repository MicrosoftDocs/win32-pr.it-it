---
description: Per elencare i file in una directory specificata, chiamare FindFirstFile, FindNextFile e FindClose.
ms.assetid: ab0d977d-f71c-4a18-9b1d-2221169324f0
title: Visualizzazione di un elenco di file in una directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ef872917656957253498c54560971ca87ddaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317774"
---
# <a name="listing-the-files-in-a-directory"></a><span data-ttu-id="49c63-103">Visualizzazione di un elenco di file in una directory</span><span class="sxs-lookup"><span data-stu-id="49c63-103">Listing the Files in a Directory</span></span>

<span data-ttu-id="49c63-104">Nell'esempio seguente vengono chiamati [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) per elencare i file in una directory specificata.</span><span class="sxs-lookup"><span data-stu-id="49c63-104">The following example calls [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) to list files in a specified directory.</span></span>


```C++
#include <windows.h>
#include <tchar.h> 
#include <stdio.h>
#include <strsafe.h>
#pragma comment(lib, "User32.lib")

void DisplayErrorBox(LPTSTR lpszFunction);

int _tmain(int argc, TCHAR *argv[])
{
   WIN32_FIND_DATA ffd;
   LARGE_INTEGER filesize;
   TCHAR szDir[MAX_PATH];
   size_t length_of_arg;
   HANDLE hFind = INVALID_HANDLE_VALUE;
   DWORD dwError=0;
   
   // If the directory is not specified as a command-line argument,
   // print usage.

   if(argc != 2)
   {
      _tprintf(TEXT("\nUsage: %s <directory name>\n"), argv[0]);
      return (-1);
   }

   // Check that the input path plus 3 is not longer than MAX_PATH.
   // Three characters are for the "\*" plus NULL appended below.

   StringCchLength(argv[1], MAX_PATH, &length_of_arg);

   if (length_of_arg > (MAX_PATH - 3))
   {
      _tprintf(TEXT("\nDirectory path is too long.\n"));
      return (-1);
   }

   _tprintf(TEXT("\nTarget directory is %s\n\n"), argv[1]);

   // Prepare string for use with FindFile functions.  First, copy the
   // string to a buffer, then append '\*' to the directory name.

   StringCchCopy(szDir, MAX_PATH, argv[1]);
   StringCchCat(szDir, MAX_PATH, TEXT("\\*"));

   // Find the first file in the directory.

   hFind = FindFirstFile(szDir, &ffd);

   if (INVALID_HANDLE_VALUE == hFind) 
   {
      DisplayErrorBox(TEXT("FindFirstFile"));
      return dwError;
   } 
   
   // List all the files in the directory with some info about them.

   do
   {
      if (ffd.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY)
      {
         _tprintf(TEXT("  %s   <DIR>\n"), ffd.cFileName);
      }
      else
      {
         filesize.LowPart = ffd.nFileSizeLow;
         filesize.HighPart = ffd.nFileSizeHigh;
         _tprintf(TEXT("  %s   %ld bytes\n"), ffd.cFileName, filesize.QuadPart);
      }
   }
   while (FindNextFile(hFind, &ffd) != 0);
 
   dwError = GetLastError();
   if (dwError != ERROR_NO_MORE_FILES) 
   {
      DisplayErrorBox(TEXT("FindFirstFile"));
   }

   FindClose(hFind);
   return dwError;
}


void DisplayErrorBox(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code

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

    // Display the error message and clean up

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR)lpMsgBuf)+lstrlen((LPCTSTR)lpszFunction)+40)*sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR)lpDisplayBuf, TEXT("Error"), MB_OK); 

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}

```



 

 



