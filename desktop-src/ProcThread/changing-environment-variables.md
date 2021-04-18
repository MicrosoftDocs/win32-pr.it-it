---
description: A ogni processo è associato un blocco di ambiente.
ms.assetid: b428688c-7b16-48c7-8d89-55d066496d1c
title: Modifica delle variabili di ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13054afff996c4f8128fdc58f9d6dfadc35cc84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312001"
---
# <a name="changing-environment-variables"></a><span data-ttu-id="299cc-103">Modifica delle variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="299cc-103">Changing Environment Variables</span></span>

<span data-ttu-id="299cc-104">A ogni processo è associato un blocco di ambiente.</span><span class="sxs-lookup"><span data-stu-id="299cc-104">Each process has an environment block associated with it.</span></span> <span data-ttu-id="299cc-105">Il blocco dell'ambiente è costituito da un blocco con terminazione null di stringhe con terminazione null (ovvero sono presenti due byte null alla fine del blocco), in cui ogni stringa è nel formato:</span><span class="sxs-lookup"><span data-stu-id="299cc-105">The environment block consists of a null-terminated block of null-terminated strings (meaning there are two null bytes at the end of the block), where each string is in the form:</span></span>

<span data-ttu-id="299cc-106">*nome* = *valore* di</span><span class="sxs-lookup"><span data-stu-id="299cc-106">*name*=*value*</span></span>

<span data-ttu-id="299cc-107">Tutte le stringhe nel blocco Environment devono essere ordinate in ordine alfabetico in base al nome.</span><span class="sxs-lookup"><span data-stu-id="299cc-107">All strings in the environment block must be sorted alphabetically by name.</span></span> <span data-ttu-id="299cc-108">L'ordinamento non fa distinzione tra maiuscole e minuscole, ovvero l'ordine Unicode, indipendentemente dalle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="299cc-108">The sort is case-insensitive, Unicode order, without regard to locale.</span></span> <span data-ttu-id="299cc-109">Poiché il segno di uguale è un separatore, non deve essere utilizzato nel nome di una variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="299cc-109">Because the equal sign is a separator, it must not be used in the name of an environment variable.</span></span>

## <a name="example-1"></a><span data-ttu-id="299cc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="299cc-110">Example 1</span></span>

<span data-ttu-id="299cc-111">Per impostazione predefinita, un processo figlio eredita una copia del blocco dell'ambiente del processo padre.</span><span class="sxs-lookup"><span data-stu-id="299cc-111">By default, a child process inherits a copy of the environment block of the parent process.</span></span> <span data-ttu-id="299cc-112">Nell'esempio seguente viene illustrato come creare un nuovo blocco di ambiente da passare a un processo figlio utilizzando [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="299cc-112">The following example demonstrates how to create a new environment block to pass to a child process using [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

<span data-ttu-id="299cc-113">Questo esempio usa il codice riportato nell'esempio tre come processo figlio, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="299cc-113">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFSIZE 4096

int _tmain()
{
    TCHAR chNewEnv[BUFSIZE];
    LPTSTR lpszCurrentVariable; 
    DWORD dwFlags=0;
    TCHAR szAppName[]=TEXT("ex3.exe");
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fSuccess; 
 
    // Copy environment strings into an environment block. 
 
    lpszCurrentVariable = (LPTSTR) chNewEnv;
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MySetting=A"))))
    {
        printf("String copy failed\n"); 
        return FALSE;
    }

    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MyVersion=2")))) 
    {
        printf("String copy failed\n"); 
        return FALSE;
    }
 
    // Terminate the block with a NULL byte. 
 
    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    *lpszCurrentVariable = (TCHAR)0; 

    // Create the child process, specifying a new environment block. 
 
    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);

#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags,
        (LPVOID) chNewEnv,   // new environment block
        NULL, &si, &pi); 
 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError());
        return FALSE;
    }
    WaitForSingleObject(pi.hProcess, INFINITE);
    return TRUE;
}
```



## <a name="example-2"></a><span data-ttu-id="299cc-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="299cc-114">Example 2</span></span>

<span data-ttu-id="299cc-115">La modifica delle variabili di ambiente di un processo figlio durante la creazione del processo è l'unico modo in cui un processo può modificare direttamente le variabili di ambiente di un altro processo.</span><span class="sxs-lookup"><span data-stu-id="299cc-115">Altering the environment variables of a child process during process creation is the only way one process can directly change the environment variables of another process.</span></span> <span data-ttu-id="299cc-116">Un processo non può mai modificare direttamente le variabili di ambiente di un altro processo che non è figlio di tale processo.</span><span class="sxs-lookup"><span data-stu-id="299cc-116">A process can never directly change the environment variables of another process that is not a child of that process.</span></span>

<span data-ttu-id="299cc-117">Se si vuole che il processo figlio erediti la maggior parte dell'ambiente padre con solo alcune modifiche, recuperare i valori correnti usando [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), salvare questi valori, creare un blocco aggiornato per il processo figlio da ereditare, creare il processo figlio e quindi ripristinare i valori salvati usando [**nell'SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="299cc-117">If you want the child process to inherit most of the parent's environment with only a few changes, retrieve the current values using [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), save these values, create an updated block for the child process to inherit, create the child process, and then restore the saved values using [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), as shown in the following example.</span></span>

<span data-ttu-id="299cc-118">Questo esempio usa il codice riportato nell'esempio tre come processo figlio, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="299cc-118">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define VARNAME TEXT("MyVariable")

int _tmain()
{
    DWORD dwRet, dwErr;
    LPTSTR pszOldVal; 
    TCHAR szAppName[]=TEXT("ex3.exe");
    DWORD dwFlags=0;
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fExist, fSuccess; 
 
    // Retrieves the current value of the variable if it exists.
    // Sets the variable to a new value, creates a child process,
    // then uses SetEnvironmentVariable to restore the original
    // value or delete it if it did not exist previously. 
 
    pszOldVal = (LPTSTR) malloc(BUFSIZE*sizeof(TCHAR));
    if(NULL == pszOldVal)
    {
        printf("Out of memory\n");
        return FALSE;
    }

    dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, BUFSIZE);

    if(0 == dwRet)
    {
        dwErr = GetLastError();
        if( ERROR_ENVVAR_NOT_FOUND == dwErr )
        {
            printf("Environment variable does not exist.\n");
            fExist=FALSE;
        }
    }
    else if(BUFSIZE < dwRet)
    {
        pszOldVal = (LPTSTR) realloc(pszOldVal, dwRet*sizeof(TCHAR));   
        if(NULL == pszOldVal)
        {
            printf("Out of memory\n");
            return FALSE;
        }
        dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, dwRet);
        if(!dwRet)
        {
            printf("GetEnvironmentVariable failed (%d)\n", GetLastError());
            return FALSE;
        }
        else fExist=TRUE;
    }
    else fExist=TRUE;

    // Set a value for the child process to inherit. 
 
    if (! SetEnvironmentVariable(VARNAME, TEXT("Test"))) 
    {
        printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
        return FALSE;
    }
 
    // Create a child process. 

    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);
 
#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags, 
        NULL,     // inherit parent's environment 
        NULL, &si, &pi); 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError()); 
    }
    WaitForSingleObject(pi.hProcess, INFINITE);

    // Restore the original environment variable. 
 
    if(fExist)
    {
        if (! SetEnvironmentVariable(VARNAME, pszOldVal)) 
        {
            printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
            return FALSE;
        }
    }
    else SetEnvironmentVariable(VARNAME, NULL);

    free(pszOldVal);
    
    return fSuccess;
}
```



## <a name="example-3"></a><span data-ttu-id="299cc-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="299cc-119">Example 3</span></span>

<span data-ttu-id="299cc-120">Nell'esempio seguente viene recuperato il blocco dell'ambiente del processo utilizzando [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) e il contenuto viene stampato nella console.</span><span class="sxs-lookup"><span data-stu-id="299cc-120">The following example retrieves the process's environment block using [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) and prints the contents to the console.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int _tmain()
{
    LPTSTR lpszVariable; 
    LPTCH lpvEnv; 
 
    // Get a pointer to the environment block. 
 
    lpvEnv = GetEnvironmentStrings();

    // If the returned pointer is NULL, exit.
    if (lpvEnv == NULL)
    {
        printf("GetEnvironmentStrings failed (%d)\n", GetLastError()); 
        return 0;
    }
 
    // Variable strings are separated by NULL byte, and the block is 
    // terminated by a NULL byte. 

    lpszVariable = (LPTSTR) lpvEnv;

    while (*lpszVariable)
    {
        _tprintf(TEXT("%s\n"), lpszVariable);
        lpszVariable += lstrlen(lpszVariable) + 1;
    }
    FreeEnvironmentStrings(lpvEnv);
    return 1;
}
```



 

 
