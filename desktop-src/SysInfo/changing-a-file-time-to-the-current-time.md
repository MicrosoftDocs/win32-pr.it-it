---
description: Nell'esempio seguente l'ora dell'ultima scrittura di un file viene impostata sull'ora di sistema corrente mediante la funzione SetFileTime.
ms.assetid: b4a70c01-d5ce-47e8-9918-9c9176894240
title: Modifica dell'ora del file nell'ora corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3d4b6189514196c5f8a332c259da9f8f8d7417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968747"
---
# <a name="changing-a-file-time-to-the-current-time"></a><span data-ttu-id="7660b-103">Modifica dell'ora del file nell'ora corrente</span><span class="sxs-lookup"><span data-stu-id="7660b-103">Changing a File Time to the Current Time</span></span>

<span data-ttu-id="7660b-104">Nell'esempio seguente l'ora dell'ultima scrittura di un file viene impostata sull'ora di sistema corrente mediante la funzione [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) .</span><span class="sxs-lookup"><span data-stu-id="7660b-104">The following example sets the last-write time for a file to the current system time using the [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) function.</span></span>

<span data-ttu-id="7660b-105">Il file system NTFS archivia i valori di ora in formato UTC, quindi non sono interessati da modifiche nel fuso orario o nell'ora legale.</span><span class="sxs-lookup"><span data-stu-id="7660b-105">The NTFS file system stores time values in UTC format, so they are not affected by changes in time zone or daylight saving time.</span></span> <span data-ttu-id="7660b-106">Il file system FAT archivia i valori temporali in base all'ora locale del computer.</span><span class="sxs-lookup"><span data-stu-id="7660b-106">The FAT file system stores time values based on the local time of the computer.</span></span>

<span data-ttu-id="7660b-107">Il file deve essere aperto con la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) utilizzando l' \_ accesso con attributi di scrittura file \_ .</span><span class="sxs-lookup"><span data-stu-id="7660b-107">The file must be opened with the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function using FILE\_WRITE\_ATTRIBUTES access.</span></span>


```C++
#include <windows.h>

// SetFileToCurrentTime - sets last write time to current system time
// Return value - TRUE if successful, FALSE otherwise
// hFile  - must be a valid file handle

BOOL SetFileToCurrentTime(HANDLE hFile)
{
    FILETIME ft;
    SYSTEMTIME st;
    BOOL f;

    GetSystemTime(&st);              // Gets the current system time
    SystemTimeToFileTime(&st, &ft);  // Converts the current system time to file time format
    f = SetFileTime(hFile,           // Sets last-write time of the file 
        (LPFILETIME) NULL,           // to the converted current system time 
        (LPFILETIME) NULL, 
        &ft);    

    return f;
}
```



 

 
