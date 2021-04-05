---
description: Trovare e stampare il nome del proprietario di un file.
ms.assetid: b0dbc785-58a7-4f39-ab39-b96abece5b93
title: Ricerca del proprietario di un oggetto file in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5518617db099d3580ce0e82b5376df5f4f3eaf58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883861"
---
# <a name="finding-the-owner-of-a-file-object-in-c"></a><span data-ttu-id="a49cd-103">Ricerca del proprietario di un oggetto file in C++</span><span class="sxs-lookup"><span data-stu-id="a49cd-103">Finding the Owner of a File Object in C++</span></span>

<span data-ttu-id="a49cd-104">Nell'esempio seguente vengono utilizzate le funzioni [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) e [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida) per trovare e stampare il nome del proprietario di un file.</span><span class="sxs-lookup"><span data-stu-id="a49cd-104">The following example uses the [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) and [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida) functions to find and print the name of the owner of a file.</span></span> <span data-ttu-id="a49cd-105">Il file esiste nella directory di lavoro corrente nel server locale.</span><span class="sxs-lookup"><span data-stu-id="a49cd-105">The file exists in the current working directory on the local server.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>
#include "accctrl.h"
#include "aclapi.h"
#pragma comment(lib, "advapi32.lib")

int main(void)
{
DWORD dwRtnCode = 0;
PSID pSidOwner = NULL;
BOOL bRtnBool = TRUE;
LPTSTR AcctName = NULL;
LPTSTR DomainName = NULL;
DWORD dwAcctName = 1, dwDomainName = 1;
SID_NAME_USE eUse = SidTypeUnknown;
HANDLE hFile;
PSECURITY_DESCRIPTOR pSD = NULL;


// Get the handle of the file object.
hFile = CreateFile(
                  TEXT("myfile.txt"),
                  GENERIC_READ,
                  FILE_SHARE_READ,
                  NULL,
                  OPEN_EXISTING,
                  FILE_ATTRIBUTE_NORMAL,
                  NULL);

// Check GetLastError for CreateFile error code.
if (hFile == INVALID_HANDLE_VALUE) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("CreateFile error = %d\n"), dwErrorCode);
          return -1;
}



// Get the owner SID of the file.
dwRtnCode = GetSecurityInfo(
                  hFile,
                  SE_FILE_OBJECT,
                  OWNER_SECURITY_INFORMATION,
                  &pSidOwner,
                  NULL,
                  NULL,
                  NULL,
                  &pSD);

// Check GetLastError for GetSecurityInfo error condition.
if (dwRtnCode != ERROR_SUCCESS) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("GetSecurityInfo error = %d\n"), dwErrorCode);
          return -1;
}

// First call to LookupAccountSid to get the buffer sizes.
bRtnBool = LookupAccountSid(
                  NULL,           // local computer
                  pSidOwner,
                  AcctName,
                  (LPDWORD)&dwAcctName,
                  DomainName,
                  (LPDWORD)&dwDomainName,
                  &eUse);

// Reallocate memory for the buffers.
AcctName = (LPTSTR)GlobalAlloc(
          GMEM_FIXED,
          dwAcctName);

// Check GetLastError for GlobalAlloc error condition.
if (AcctName == NULL) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("GlobalAlloc error = %d\n"), dwErrorCode);
          return -1;
}

    DomainName = (LPTSTR)GlobalAlloc(
           GMEM_FIXED,
           dwDomainName);

    // Check GetLastError for GlobalAlloc error condition.
    if (DomainName == NULL) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("GlobalAlloc error = %d\n"), dwErrorCode);
          return -1;

    }

    // Second call to LookupAccountSid to get the account name.
    bRtnBool = LookupAccountSid(
          NULL,                   // name of local or remote computer
          pSidOwner,              // security identifier
          AcctName,               // account name buffer
          (LPDWORD)&dwAcctName,   // size of account name buffer 
          DomainName,             // domain name
          (LPDWORD)&dwDomainName, // size of domain name buffer
          &eUse);                 // SID type

    // Check GetLastError for LookupAccountSid error condition.
    if (bRtnBool == FALSE) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();

          if (dwErrorCode == ERROR_NONE_MAPPED)
              _tprintf(TEXT
                  ("Account owner not found for specified SID.\n"));
          else 
              _tprintf(TEXT("Error in LookupAccountSid.\n"));
          return -1;

    } else if (bRtnBool == TRUE) 

        // Print the account name.
        _tprintf(TEXT("Account owner = %s\n"), AcctName);

    return 0;
}
```



 

 



