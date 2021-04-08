---
title: Codice di esempio per l'installazione della ridistribuzione
description: Codice di esempio per l'installazione della ridistribuzione
ms.assetid: 480f0da7-68c1-4144-a623-47578ae54acb
keywords:
- Windows Media Format SDK, ridistribuzione software
- ASF (Advanced Systems Format), ridistribuzione del software
- ASF (formato avanzato dei sistemi), ridistribuzione del software
- Windows Media Format SDK, ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ASF (formato avanzato dei sistemi), ridistribuzione
- ridistribuzione del software, codice di esempio
- ridistribuzione del software, esempi di codice
- ridistribuzione, codice di esempio
- ridistribuzione, esempi di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9990b617ed9c3492c0565b794798412f8e8373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855701"
---
# <a name="example-code-for-redistribution-setup"></a><span data-ttu-id="e8bd5-113">Codice di esempio per l'installazione della ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="e8bd5-113">Example Code for Redistribution Setup</span></span>

<span data-ttu-id="e8bd5-114">Quando si include il pacchetto di ridistribuzione nell'applicazione, è possibile utilizzare il flag/Q: A quando si richiama il pacchetto di ridistribuzione nella routine di installazione.</span><span class="sxs-lookup"><span data-stu-id="e8bd5-114">When including the redistribution package in your application, you can use the /Q:A flag when you invoke the redistribution package in your setup routine.</span></span> <span data-ttu-id="e8bd5-115">Viene così evitata l'interfaccia utente (UI).</span><span class="sxs-lookup"><span data-stu-id="e8bd5-115">This suppresses the user interface (UI).</span></span>

<span data-ttu-id="e8bd5-116">Il codice di esempio seguente può essere utilizzato nella routine di installazione per eseguire i pacchetti di ridistribuzione in modalità non interattiva e inviare una notifica alla routine di installazione quando il computer deve essere riavviato.</span><span class="sxs-lookup"><span data-stu-id="e8bd5-116">The following example code can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span>


```C++
#include <windows.h>
#include <shlwapi.h>
#include <TCHAR.H>

// Link to shlwapi.lib.
#pragma comment(lib, "shlwapi")

#define MAX_TIMEOUT_MS 30 * 60 * 1000
#define TIME_INCREMENT 250

// Prototypes
BOOL InstallWMRedist( BOOL );
BOOL SystemNeedsReboot( void );

void main( void )
{
    InstallWMRedist( TRUE );

    printf("Setup is complete.\n");

    if( SystemNeedsReboot() )
    {
        // Write some code here to ensure that your application will 
        // restart the computer, delay dll registrations, and so on 
        // until after the restart, where possible. For example, 
        // set a global flag for use by the application.
        printf("A reboot IS required.");
    }
    else
    {
        printf("A reboot IS NOT required...");
    }
    
}

///////////////////////////////////////////////////////////////////////
// 
// InstallWMRedist
//
// fWaitForCompletion: If TRUE the function waits for completion.
//
///////////////////////////////////////////////////////////////////////
BOOL InstallWMRedist( BOOL fWaitForCompletion )
{
    STARTUPINFO StartUpInfo;
    PROCESS_INFORMATION ProcessInfo;

    StartUpInfo.cb = sizeof( StartUpInfo );
    StartUpInfo.lpReserved = NULL;
    StartUpInfo.dwFlags = 0;
    StartUpInfo.cbReserved2 = 0;
    StartUpInfo.lpReserved2 = NULL; 
    StartUpInfo.lpDesktop = NULL;
    StartUpInfo.lpTitle = NULL;
    StartUpInfo.dwX = 0;
    StartUpInfo.dwY = 0;
    StartUpInfo.dwXSize = 0;
    StartUpInfo.dwYSize = 0;
    StartUpInfo.dwXCountChars = 0;
    StartUpInfo.dwYCountChars = 0;
    StartUpInfo.dwFillAttribute = 0;
    StartUpInfo.dwFlags = 0;
    StartUpInfo.wShowWindow = 0;
    StartUpInfo.hStdInput = NULL;
    StartUpInfo.hStdOutput = NULL;
    StartUpInfo.hStdError = NULL;

    // Run the installer with the Quiet for All dialogs and Reboot:Never 
    // flags. The installation should be silent, and the setup routine  
    // will be notified about whether the computer must be restarted.

    if( !CreateProcess( _T("c:\\temp\\WMFDist.exe"), 
                        _T("c:\\temp\\WMFDist.exe /Q:A"), 
                        NULL, NULL, FALSE, 0, NULL, NULL, 
                        &StartUpInfo, &ProcessInfo ) )
    {
        DWORD myError = GetLastError();
        return( FALSE );
    }

    CloseHandle( ProcessInfo.hThread );

    if( fWaitForCompletion )
    {
        DWORD dwTimePassed = 0;
        while( TRUE )
        {
            if( WAIT_TIMEOUT != WaitForMultipleObjects( 1, 
                                       &ProcessInfo.hProcess, 
                                       FALSE, TIME_INCREMENT ) )
                break;

            if( dwTimePassed > MAX_TIMEOUT_MS )
            {
                TerminateProcess( ProcessInfo.hProcess, E_FAIL );
                break;
            }
            dwTimePassed += TIME_INCREMENT;
        }
    }
    CloseHandle( ProcessInfo.hProcess);

    return( TRUE );
}

///////////////////////////////////////////////////////////////////////
//
// Used to determine whether the system should be restarted.
//
///////////////////////////////////////////////////////////////////////
BOOL SystemNeedsReboot( void )
{
    BOOL fNeedExists = FALSE;
    OSVERSIONINFO osvi;

    osvi.dwOSVersionInfoSize = sizeof( OSVERSIONINFO );
    GetVersionEx( &osvi );

    if( VER_PLATFORM_WIN32_NT != osvi.dwPlatformId )
    {
        TCHAR szIniPath[MAX_PATH];

        GetWindowsDirectory(szIniPath, sizeof(szIniPath)/sizeof(TCHAR));

        // PathAppend automatically inserts a backslash if needed.
        PathAppend( szIniPath, _T("wininit.ini") );

        if( 0xFFFFFFFF != GetFileAttributes( szIniPath ) )
        {
            HANDLE hFile = INVALID_HANDLE_VALUE;

            hFile = CreateFile(
                szIniPath, 
                GENERIC_READ, 
                FILE_SHARE_READ | FILE_SHARE_WRITE, 
                NULL,
                OPEN_EXISTING,
                0, NULL
                );

            if (hFile != INVALID_HANDLE_VALUE)
            {
                DWORD cbFileSize = GetFileSize(hFile, NULL);

                if ((cbFileSize > 0) && (cbFileSize != INVALID_FILE_SIZE))
                {
                    fNeedExists = TRUE;
                }
                CloseHandle(hFile);
            }
        }
    }
    else
    {
        HKEY hKey = NULL;

        if( ERROR_SUCCESS == RegOpenKeyEx( HKEY_LOCAL_MACHINE, 
                _T("System\\CurrentControlSet\\Control\\Session Manager"), 
                 0, KEY_READ, &hKey ) )
        {
            if( ERROR_SUCCESS == RegQueryValueEx( hKey, 
                _T("PendingFileRenameOperations"), 
                 NULL, NULL, NULL, NULL))
            {
                fNeedExists = TRUE;
            }

            RegCloseKey( hKey );
        }
    }

    return( fNeedExists );
}
```



## <a name="related-topics"></a><span data-ttu-id="e8bd5-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8bd5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8bd5-118">**Ridistribuzione del software**</span><span class="sxs-lookup"><span data-stu-id="e8bd5-118">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




