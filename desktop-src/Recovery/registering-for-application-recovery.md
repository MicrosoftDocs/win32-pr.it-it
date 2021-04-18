---
title: Registrazione per il ripristino dell'applicazione
ms.assetid: 2940b1b2-a0ca-4f81-a576-ae6d53ffd4a8
description: 'Altre informazioni su: registrazione per il ripristino delle applicazioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056232bc2a8a10857ff07900ce261d95ed719b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311943"
---
# <a name="registering-for-application-recovery"></a><span data-ttu-id="e7521-103">Registrazione per il ripristino dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="e7521-103">Registering for Application Recovery</span></span>

<span data-ttu-id="e7521-104">In questa sezione vengono fornite informazioni dettagliate sull'implementazione di una funzionalità di ripristino nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7521-104">This section provides details on implementing a recovery feature in your application.</span></span> <span data-ttu-id="e7521-105">È consigliabile implementare questa funzionalità per gestire i casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7521-105">You should consider implementing this feature to handle the following cases:</span></span>

-   [<span data-ttu-id="e7521-106">Ripristino quando si verifica un'eccezione non gestita in un'applicazione o si interrompe la risposta</span><span class="sxs-lookup"><span data-stu-id="e7521-106">Recovering when an application experiences an unhandled exception or stops responding</span></span>](#recovering-when-an-application-experiences-an-unhandled-exception-or-stops-responding)

    <span data-ttu-id="e7521-107">Impedisce la perdita di dati quando l'applicazione smette di funzionare in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e7521-107">Prevents loss of data when the application unexpectedly stops working.</span></span>

-   [<span data-ttu-id="e7521-108">Salvataggio dei dati e dello stato dell'applicazione durante la chiusura dell'applicazione a causa di un aggiornamento software</span><span class="sxs-lookup"><span data-stu-id="e7521-108">Saving data and application state when application is being closed due to a software update</span></span>](#saving-data-and-application-state-when-application-is-being-closed-due-to-a-software-update)

    <span data-ttu-id="e7521-109">Consente a un utente di ottenere facilmente i dati dell'applicazione quando l'applicazione viene chiusa a causa di un'installazione dell'aggiornamento software, che può verificarsi senza concedere all'utente la possibilità di salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="e7521-109">Enables a user to seamlessly get back application data when the application is closed due to a software update installation (which may be happening without giving the user a chance to save data).</span></span>

## <a name="recovering-when-an-application-experiences-an-unhandled-exception-or-stops-responding"></a><span data-ttu-id="e7521-110">Ripristino quando si verifica un'eccezione non gestita in un'applicazione o si interrompe la risposta</span><span class="sxs-lookup"><span data-stu-id="e7521-110">Recovering when an application experiences an unhandled exception or stops responding</span></span>

<span data-ttu-id="e7521-111">Per registrare un callback di ripristino, chiamare la funzione [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback) .</span><span class="sxs-lookup"><span data-stu-id="e7521-111">To register a recovery callback, call the [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback) function.</span></span> <span data-ttu-id="e7521-112">[Segnalazione errori Windows (WER)](/windows/desktop/wer/windows-error-reporting) chiama il callback di ripristino prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o se l'applicazione non risponde.</span><span class="sxs-lookup"><span data-stu-id="e7521-112">[Windows Error Reporting (WER)](/windows/desktop/wer/windows-error-reporting) calls your recovery callback before the application exits due to an unhandled exception or the application not responding.</span></span>

<span data-ttu-id="e7521-113">Usare il callback di ripristino per provare a salvare i dati e le informazioni sullo stato prima del termine dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7521-113">You use the recovery callback to try to save data and state information before the application terminates.</span></span> <span data-ttu-id="e7521-114">È quindi possibile usare i dati salvati e le informazioni sullo stato al riavvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7521-114">You could then use the saved data and state information when the application is restarted.</span></span>

<span data-ttu-id="e7521-115">Durante il processo di ripristino, è necessario chiamare la funzione [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress) entro l'intervallo di ping specificato. in caso contrario, il processo di ripristino viene terminato.</span><span class="sxs-lookup"><span data-stu-id="e7521-115">During the recovery process, you must call the [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress) function within the specified ping interval; otherwise, the recovery process is terminated.</span></span> <span data-ttu-id="e7521-116">La chiamata a **ApplicationRecoveryInProgress** consente di tenere presente che è ancora in corso il ripristino dei dati.</span><span class="sxs-lookup"><span data-stu-id="e7521-116">Calling **ApplicationRecoveryInProgress** lets WER know that you are still actively recovering data.</span></span> <span data-ttu-id="e7521-117">Al termine del processo di ripristino, chiamare la funzione [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished) .</span><span class="sxs-lookup"><span data-stu-id="e7521-117">When the recovery process is complete, call the [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished) function.</span></span> <span data-ttu-id="e7521-118">Si noti che la funzione **ApplicationRecoveryFinished** deve essere l'ultima chiamata apportata prima di uscire perché la funzione termina immediatamente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7521-118">Note that the **ApplicationRecoveryFinished** function should be the last call you make before exiting because the function immediately terminates the application.</span></span>

<span data-ttu-id="e7521-119">Si consiglia di salvare periodicamente le copie temporanee dei dati e delle informazioni sullo stato durante il normale svolgimento del processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7521-119">You should consider periodically saving temporary copies of the data and state information during the normal course of the application process.</span></span> <span data-ttu-id="e7521-120">Il salvataggio periodico dei dati può ridurre il tempo necessario per il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e7521-120">Periodically saving the data may save time in the recovery process.</span></span>

## <a name="saving-data-and-application-state-when-application-is-being-closed-due-to-a-software-update"></a><span data-ttu-id="e7521-121">Salvataggio dei dati e dello stato dell'applicazione durante la chiusura dell'applicazione a causa di un aggiornamento software</span><span class="sxs-lookup"><span data-stu-id="e7521-121">Saving data and application state when application is being closed due to a software update</span></span>

<span data-ttu-id="e7521-122">Se è possibile aggiornare un'applicazione Windows, l'applicazione deve elaborare anche i messaggi [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) e [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) .</span><span class="sxs-lookup"><span data-stu-id="e7521-122">If a Windows application can be updated, the application should also process the [**WM\_QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) and [**WM\_ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) messages.</span></span> <span data-ttu-id="e7521-123">Il programma di installazione invia questi messaggi quando il programma di installazione richiede che l'applicazione venga arrestata per completare l'installazione o quando è necessario riavviare il computer per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e7521-123">The installer sends these messages when the installer needs the application to shutdown in order to complete the installation or when a reboot is required to complete the installation.</span></span> <span data-ttu-id="e7521-124">Si noti che in questo caso l'applicazione ha meno tempo per eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="e7521-124">Note that in this case, the application has less time to perform recovery.</span></span> <span data-ttu-id="e7521-125">Ad esempio, l'applicazione deve rispondere a ogni messaggio entro cinque secondi.</span><span class="sxs-lookup"><span data-stu-id="e7521-125">For example, the application must respond to each message within five seconds.</span></span>

<span data-ttu-id="e7521-126">Per le applicazioni console che possono essere aggiornate, è consigliabile considerare la gestione delle notifiche degli eventi di CTRL \_ C \_ .</span><span class="sxs-lookup"><span data-stu-id="e7521-126">For console applications that could be updated, you should consider handling CTRL\_C\_EVENT notifications.</span></span> <span data-ttu-id="e7521-127">Per un esempio, vedere la pagina [relativa alla registrazione per il riavvio dell'applicazione](registering-for-application-restart.md).</span><span class="sxs-lookup"><span data-stu-id="e7521-127">For an example, see [Registering for Application Restart](registering-for-application-restart.md).</span></span> <span data-ttu-id="e7521-128">Il programma di installazione invia questa notifica quando è necessario che l'applicazione venga arrestata per completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e7521-128">The installer sends this notification when it needs the application to shutdown in order to complete the update.</span></span> <span data-ttu-id="e7521-129">L'applicazione ha 30 secondi per gestire la notifica.</span><span class="sxs-lookup"><span data-stu-id="e7521-129">The application has 30 seconds to handle the notification.</span></span>

<span data-ttu-id="e7521-130">Nell'esempio seguente viene illustrato come eseguire la registrazione per il ripristino, un'implementazione di callback di ripristino semplice e come elaborare i messaggi [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) e [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) .</span><span class="sxs-lookup"><span data-stu-id="e7521-130">The following example shows how to register for recovery, a simple recovery callback implementation, and how to process the [**WM\_QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) and [**WM\_ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) messages.</span></span>


```C++
#define UNICODE
#include <windows.h>
#include <stdio.h>
#include <commctrl.h>
#include <strsafe.h>
#include "recover.h"

#pragma comment(lib, "comctl32.lib") // For common controls
#pragma comment(lib, "user32.lib")

#define RESTART_SWITCH L"/restart"
#define RESTART_SWITCH_LEN 8

HINSTANCE g_hinst;
HWND g_hwnd;
HWND g_hwndStatus;

DWORD g_dwRecordId = 0;

// Prototypes
BOOL CreateWindows(void);
LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);
BOOL InitInstance(LPWSTR pwsCommandLine);
DWORD WINAPI Recover(PVOID pContext);
BOOL IsRestartSelected(void);

// A simple example to show how to use application recovery in a window application.
// For simplicity, the state information (record ID) is passed as part of the command line. 
int APIENTRY wWinMain(
    HINSTANCE hInstance,
    HINSTANCE hPrevInstance,
    LPWSTR    lpCmdLine,
    int       nCmdShow)
{
    MSG msg;

    g_hinst = hInstance;

    if (!CreateWindows())
    {
        return 0;
    }

    if (!InitInstance(lpCmdLine))
    {
        return 0;
    }

    ShowWindow(g_hwnd, nCmdShow);
    UpdateWindow(g_hwnd);

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return (int)msg.wParam;
}


// Initialize this instance of the application.
BOOL InitInstance(LPWSTR pwsCommandLine)
{
    BOOL fSuccess = TRUE;
    BOOL fIsRestart = FALSE;
    DWORD len = 0;
    LPWSTR pch = NULL;
    WCHAR wsStatusMsg[128];
    //WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    if (len = wcslen(pwsCommandLine))
    {
        // Get the restart info from the command line. The command line is 
        // of the form, /restart -r:<RecordId>. The application 
        // is being restarted if the first argument is /restart.
        if (!wcsncmp(RESTART_SWITCH, pwsCommandLine, RESTART_SWITCH_LEN))
        {
            fIsRestart = TRUE;

            pch = pwsCommandLine + len;
            while (*--pch != ':' && pch >= pwsCommandLine)
                ;

            g_dwRecordId = _wtoi(pch+1);
        }
    }

    if (fIsRestart)
    {
        // TODO: Use the record ID to initialize the application.
        RtlZeroMemory(wsStatusMsg, sizeof(wsStatusMsg));
        StringCchPrintf(wsStatusMsg, 128, L"Initializing after restart (record ID is %lu)", g_dwRecordId);
        SetWindowText(g_hwndStatus, wsStatusMsg);
    }
    else
    {
        // This is not a restart, so initialize the application accordingly.
        SetWindowText(g_hwndStatus, L"Initializing application");
    }


    // You could call the RegisterApplicationRestart and 
    // RegisterApplicationRecovery functions here to register for
    // application recovery and restart, but this example uses menu 
    // items to toggle these features on and off for testing purposes.

    //// Register for restart. The command line is updated in the recovery callback.
    //RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    //StringCchPrintf(wsCommandLine, RESTART_MAX_CMD_LINE, L"/restart -r:%lu", dwRecordId);

    //hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    //if (FAILED(hr))
    //{
    //    // Not failing because the registration failed.
    //    goto cleanup;
    //}

    //// Register the callback that handles recovery when the application
    //// encounters an unhandled exception or becomes unresponsive.
    //hr = RegisterApplicationRecoveryCallback(Recover, g_dwRecordId, RECOVERY_DEFAULT_PING_INTERVAL, 0);
    //if (FAILED(hr))
    //{
    //    // Not failing initialization because the registration failed.
    //    // Consider calling UnregisterApplicationRestart if you must
    //    // have the latest state information.
    //    goto cleanup;
    //}

//cleanup:

    return fSuccess;
}


BOOL CreateWindows(void)
{
    BOOL fSuccess = TRUE;
    WNDCLASSEX wc;
    ATOM atom;
    INITCOMMONCONTROLSEX initctrls;
    RECT rc;

    ZeroMemory(&wc, sizeof(wc));
    wc.cbSize = sizeof(wc);
    wc.lpfnWndProc = WndProc;
    wc.hInstance = g_hinst;
    wc.lpszClassName = L"MainWClass";
    wc.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);
    wc.hCursor = LoadCursor(NULL, IDC_ARROW);
    wc.lpszMenuName    = MAKEINTRESOURCE(IDC_RECOVER);

    atom = RegisterClassEx(&wc);
    g_hwnd = CreateWindowEx(0,
        L"MainWClass",
        L"Testing Application Restart and Recovery",
        WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN,
        CW_USEDEFAULT, CW_USEDEFAULT, 
        390, 165, 
        NULL,
        NULL,
        g_hinst,
        NULL);

    if (NULL == g_hwnd)
    {
        fSuccess = FALSE;
        goto cleanup;
    }

    initctrls.dwSize = sizeof(initctrls);
    initctrls.dwICC = ICC_BAR_CLASSES;
    InitCommonControlsEx(&initctrls);

    GetClientRect(g_hwnd, &rc);

    g_hwndStatus = CreateWindowEx(0, STATUSCLASSNAME, NULL,
        WS_CHILD | WS_BORDER | WS_VISIBLE,
        rc.left, rc.bottom - 20, rc.right, 20,
        g_hwnd, NULL, g_hinst, NULL);
        
    if (NULL == g_hwndStatus)
    {
        fSuccess = FALSE;
    }

cleanup:

    return fSuccess;
}


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HMENU hMenu;
    MENUITEMINFO miInfo;
    BOOL bChecked = FALSE;
    HRESULT hr = S_OK;
    int* p = NULL;
    ULONG error = ERROR_SUCCESS;
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];


    switch (message)
    {
        case WM_COMMAND:
            wmId = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                // Causes an access violation to test the restart feature,
                // if restart is checked. The application must be running
                // for at least 60 before it can be restarted if an access
                // violation occurs.
                case ID_FILE_CRASH:
                    *p = 5;
                    break;

                // Menu item used to register for restart (checked) and to
                // remove the registration (unchecked). The application must be running
                // for at least 60 seconds before it can be restarted if an access
                // violation occurs (select Crash from the File menu).
                case ID_FILE_RESTART:
                    hMenu = GetMenu(hWnd);
                    if (hMenu)
                    {
                        RtlZeroMemory(&miInfo, sizeof(MENUITEMINFO));
                        miInfo.cbSize = sizeof(MENUITEMINFO);
                        miInfo.fMask = MIIM_STATE;

                        if (GetMenuItemInfo(hMenu, ID_FILE_RESTART, FALSE, &miInfo))
                        {
                            // Toggling Restart to unchecked. Remove restart registration.
                            if ((miInfo.fState & MFS_CHECKED) == MFS_CHECKED)
                            {
                                miInfo.fState &= ~MFS_CHECKED;
                                miInfo.fState |= MFS_UNCHECKED;

                                hr = UnregisterApplicationRestart();
                                if (FAILED(hr))
                                {
                                    // Not failing because removing the registration failed.
                                }
                            }
                            else // Toggling Restart to checked. Register for restart.
                            {
                                miInfo.fState &= ~MFS_UNCHECKED;
                                miInfo.fState |= MFS_CHECKED;

                                // Register for restart. The command line is updated in the recovery callback,
                                // if recovery is selected.
                                RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
                                g_dwRecordId += 10; // Incrementing to show different value on restart.
                                StringCchPrintf(wsCommandLine, RESTART_MAX_CMD_LINE, L"/restart -r:%lu", g_dwRecordId);

                                hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
                                if (FAILED(hr))
                                {
                                    // Not failing because the registration failed.
                                }

                                MessageBox(hWnd, L"You must wait 60 seconds before selecting Crash from the\n"
                                    L"File menu to crash the application and test the restart feature.",
                                    L"Registered for restart", 
                                    MB_OK | MB_ICONINFORMATION);
                            }

                            if (!SetMenuItemInfo(hMenu, ID_FILE_RESTART, FALSE, &miInfo))
                            {
                                // Handle error; call GetLastError() to get the error.
                            }
                        }
                    }
                    else
                    {
                        // Handle error; call GetLastError() to get the error.
                    }

                    break;

                // Menu item use to register for recovery (checked) and to
                // remove the registration (unchecked).
                case ID_FILE_RECOVER:
                    hMenu = GetMenu(hWnd);
                    if (hMenu)
                    {
                        RtlZeroMemory(&miInfo, sizeof(MENUITEMINFO));
                        miInfo.cbSize = sizeof(MENUITEMINFO);
                        miInfo.fMask = MIIM_STATE;

                        if (GetMenuItemInfo(hMenu, ID_FILE_RECOVER, FALSE, &miInfo))
                        {
                            if ((miInfo.fState & MFS_CHECKED) == MFS_CHECKED)
                            {
                                miInfo.fState &= ~MFS_CHECKED;
                                miInfo.fState |= MFS_UNCHECKED;

                                hr = UnregisterApplicationRecoveryCallback();
                                if (FAILED(hr))
                                {
                                    // Not failing because removing the registration failed.
                                }
                            }
                            else
                            {
                                miInfo.fState &= ~MFS_UNCHECKED;
                                miInfo.fState |= MFS_CHECKED;

                                hr = RegisterApplicationRecoveryCallback(Recover, &g_dwRecordId, RECOVERY_DEFAULT_PING_INTERVAL, 0);
                                if (FAILED(hr))
                                {
                                    // Not failing because the registration failed.
                                }
                            }

                            if (!SetMenuItemInfo(hMenu, ID_FILE_RECOVER, FALSE, &miInfo))
                            {
                                // Handle the error; call GetLastError() to get the error.
                            }
                        }
                    }
                    else
                    {
                        // Handle error; call GetLastError() to get the error.
                    }

                    break;

                    case IDM_EXIT:
                        DestroyWindow(hWnd);
                    break;

                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }

            break;

        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // TODO: Add any drawing code here...
            EndPaint(hWnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        case WM_CLOSE:
            // You could use this message to handle additional recovery 
            // processing if you are unable to finish recovery in the 
            // WM_ENDSESSION message. This is for the application update
            // case only.

            DestroyWindow(hWnd);
            break;

        // The WM_QUERYENDSESSION and WM_ENDSESSION messages are used for 
        // recovery only in the case where the application is being updated.
        // The recovery callback is used instead for the case where the 
        // application becomes unresponsive or encounters an unhandled exception.
        case WM_QUERYENDSESSION:

            // Check the lParam parameter for why the system is asking the application to close.
            // The Restart Manager sets lParam to ENDSESSION_CLOSEAPP when installer needs to 
            // replace files that the application is using.
            if (lParam & ENDSESSION_CLOSEAPP)
            {
                // Consider using EnableWindow to disable the mouse & keyboard input until 
                // receiving the WM_ENDSESSION message.
                        
                // This message is the last opportunity to call the RegisterApplicationRestart
                // function to register to have your application restarted after the update
                // completes. If you have already registered for restart, you can use this 
                // opportunity to update the command line arguments. 
                hr = RegisterApplicationRestart(L"<commandlinearguments>", 0);
                if (FAILED(hr))
                {
                    // Log an event or do some error handling.
                }
                     
                // Typically, applications should respect the user's or system's request and return
                // TRUE to indicate that they are willing to close. If the application is performing
                // a critical operation which cannot be interrupted, such as burning media, then you
                // should return FALSE. If you return FALSE, you should also call the 
                // ShutdownBlockReasonCreate function to specify a reason for blocking the shutdown
                // operation. After the critical operation has completed, call the 
                // ShutdownBlockReasonDestroy function to indicate that the application is now 
                // ready to terminate.

                return TRUE;
            }

            return TRUE;

        case WM_ENDSESSION:

            // You receive this message after receiving the WM_QUERYENDSESSION message. The lParam
            // parameter indicates why the system asked the application to close. The Restart 
            // Manager sets lParam to ENDSESSION_CLOSEAPP when installer needs to replace files 
            // that the application is using. 
            if (lParam & ENDSESSION_CLOSEAPP)
            {
                // You also need to check the value of the wParam parameter. The wParam value 
                // indicates if the application should close or not based on the results of 
                // the query. If the value is TRUE, the application is closing. 
                if (wParam == TRUE)      
                {
                    // You should use this opportunity to save data and state information. 
                }
                else // FALSE, the application is not closing
                {
                    // If you disabled the mouse and keyboard input as suggested in 
                    // the WM_QUERYENDSESSION message, you should call the EnableWindow
                    // function to enable the input.
                 
                    // You could call the RegisterApplicationRestart function to update the
                    // command line as appropriate for your application.
                    hr = RegisterApplicationRestart(L"<commandlinearguments>", 0);
                    if (FAILED(hr))
                    {
                        // Log an event or do some error handling.
                    }
                }
            }
          
            return 0;

        // This example does not show other messages such as WM_PAINT 
        // or WM_DESTROY.

        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }

    return 0;
}


// Implement the recovery callback. This callback lets the application
// save state information or data in the event that the application
// encounters an unhandled exception or becomes unresponsive.
DWORD WINAPI Recover(PVOID pContext)
{
    HRESULT hr = S_OK;
    BOOL bCanceled = FALSE;
    DWORD dwRecordId = *(DWORD*)pContext;
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    // Do recovery work. Save state information.

    // Update the restart command line if restart is requested.
    if (IsRestartSelected())
    {
        RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
        StringCchPrintf(wsCommandLine, RESTART_MAX_CMD_LINE, L"/restart -r:%lu", dwRecordId);

        hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
        if (FAILED(hr))
        {
            // Not failing because the registration failed.
            wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
        }
    }

    // You must call the ApplicationRecoveryInProgress function within
    // the specified ping interval or the recovery callback exits.
    // Typically, you would do a block of work, call the function, and repeat.
    ApplicationRecoveryInProgress(&bCanceled);
    if (bCanceled)  
    {
        wprintf(L"Recovery was canceled by the user.\n");
        goto cleanup;
    }

cleanup:

    ApplicationRecoveryFinished((bCanceled) ? FALSE: TRUE);

    return 0;
}

BOOL IsRestartSelected()
{
    BOOL fSelected = FALSE;
    HMENU hMenu;
    MENUITEMINFO miInfo;

    hMenu = GetMenu(g_hwnd);
    if (hMenu)
    {
        RtlZeroMemory(&miInfo, sizeof(MENUITEMINFO));
        miInfo.cbSize = sizeof(MENUITEMINFO);
        miInfo.fMask = MIIM_STATE;

        if (GetMenuItemInfo(hMenu, ID_FILE_RESTART, FALSE, &miInfo))
        {
            if ((miInfo.fState & MFS_CHECKED) == MFS_CHECKED)
                fSelected = TRUE;
        }
    }

    return fSelected;
}
```



<span data-ttu-id="e7521-131">Di seguito è riportato il file di inclusione Recover. h per l'esempio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e7521-131">The following is the recover.h include file for the recovery example.</span></span>


```C++
#pragma once

#include "resource.h"
```



<span data-ttu-id="e7521-132">Di seguito è riportato il file di risorse Recover. RC per l'esempio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e7521-132">The following is the recover.rc resource file for the recovery example.</span></span>


```C++
// Microsoft Visual C++ generated resource script.
//
#include "resource.h"

#define APSTUDIO_READONLY_SYMBOLS
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 2 resource.
//
#define APSTUDIO_HIDDEN_SYMBOLS
#include "windows.h"
#undef APSTUDIO_HIDDEN_SYMBOLS

/////////////////////////////////////////////////////////////////////////////
#undef APSTUDIO_READONLY_SYMBOLS

/////////////////////////////////////////////////////////////////////////////
// English (U.S.) resources

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
#ifdef _WIN32
LANGUAGE LANG_ENGLISH, SUBLANG_ENGLISH_US
#pragma code_page(1252)
#endif //_WIN32


/////////////////////////////////////////////////////////////////////////////
//
// Menu
//

IDC_RECOVER MENU 
BEGIN
    POPUP "&File"
    BEGIN
        MENUITEM "C&rash",                      ID_FILE_CRASH
        MENUITEM "&Restart",                    ID_FILE_RESTART
        MENUITEM "Re&cover",                    ID_FILE_RECOVER
        MENUITEM "E&xit",                       IDM_EXIT
    END
END


#ifdef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// TEXTINCLUDE
//

1 TEXTINCLUDE 
BEGIN
    "resource.h\0"
END

2 TEXTINCLUDE 
BEGIN
    "#define APSTUDIO_HIDDEN_SYMBOLS\r\n"
    "#include ""windows.h""\r\n"
    "#undef APSTUDIO_HIDDEN_SYMBOLS\r\n"
    "\0"
END

3 TEXTINCLUDE 
BEGIN
    "\r\n"
    "\0"
END

#endif    // APSTUDIO_INVOKED

#endif    // English (U.S.) resources
/////////////////////////////////////////////////////////////////////////////

#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//


/////////////////////////////////////////////////////////////////////////////
#endif    // not APSTUDIO_INVOKED
```



<span data-ttu-id="e7521-133">Di seguito è riportato il file di inclusione Resource. h per l'esempio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e7521-133">The following is the resource.h include file for the recovery example.</span></span>


```C++
//{{NO_DEPENDENCIES}}
// Microsoft Visual C++ generated include file.
// Used by Recover.rc
//
#define IDS_APP_TITLE                   103
#define IDM_EXIT                        105
#define IDC_RECOVER                     109
#define IDR_MAINFRAME                   128
#define ID_FILE_CRASH                   32771
#define ID_FILE_RESTART                 32772
#define ID_FILE_RECOVER                 32773
#define IDC_STATIC                      -1

// Next default values for new objects
// 
#ifdef APSTUDIO_INVOKED
#ifndef APSTUDIO_READONLY_SYMBOLS
#define _APS_NO_MFC                     1
#define _APS_NEXT_RESOURCE_VALUE        129
#define _APS_NEXT_COMMAND_VALUE         32774
#define _APS_NEXT_CONTROL_VALUE         1000
#define _APS_NEXT_SYMED_VALUE           110
#endif
#endif
```



 

 
