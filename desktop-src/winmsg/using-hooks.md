---
description: 'Altre informazioni su: uso di hook'
ms.assetid: f0ca9e41-a9f7-435f-a601-f0959adcb514
title: Uso di hook
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d65d457b4549601aa89c3dae5b6e05c1fe0afed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884638"
---
# <a name="using-hooks"></a><span data-ttu-id="00946-103">Uso di hook</span><span class="sxs-lookup"><span data-stu-id="00946-103">Using Hooks</span></span>

<span data-ttu-id="00946-104">Gli esempi di codice seguenti illustrano come eseguire le attività seguenti associate agli hook:</span><span class="sxs-lookup"><span data-stu-id="00946-104">The following code examples demonstrate how to perform the following tasks associated with hooks:</span></span>

-   [<span data-ttu-id="00946-105">Installazione e rilascio di procedure Hook</span><span class="sxs-lookup"><span data-stu-id="00946-105">Installing and Releasing Hook Procedures</span></span>](#installing-and-releasing-hook-procedures)
-   [<span data-ttu-id="00946-106">Monitoraggio degli eventi di sistema</span><span class="sxs-lookup"><span data-stu-id="00946-106">Monitoring System Events</span></span>](#monitoring-system-events)

## <a name="installing-and-releasing-hook-procedures"></a><span data-ttu-id="00946-107">Installazione e rilascio di procedure Hook</span><span class="sxs-lookup"><span data-stu-id="00946-107">Installing and Releasing Hook Procedures</span></span>

<span data-ttu-id="00946-108">È possibile installare una routine hook chiamando la funzione [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) e specificando il tipo di hook che chiama la procedura, se la routine deve essere associata a tutti i thread nello stesso desktop del thread chiamante o con un thread particolare e un puntatore al punto di ingresso della routine.</span><span class="sxs-lookup"><span data-stu-id="00946-108">You can install a hook procedure by calling the [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) function and specifying the type of hook calling the procedure, whether the procedure should be associated with all threads in the same desktop as the calling thread or with a particular thread, and a pointer to the procedure entry point.</span></span>

<span data-ttu-id="00946-109">È necessario inserire una routine hook globale in una DLL separata dall'applicazione che installa la routine hook.</span><span class="sxs-lookup"><span data-stu-id="00946-109">You must place a global hook procedure in a DLL separate from the application installing the hook procedure.</span></span> <span data-ttu-id="00946-110">Per poter installare la routine hook, l'applicazione di installazione deve disporre dell'handle per il modulo DLL.</span><span class="sxs-lookup"><span data-stu-id="00946-110">The installing application must have the handle to the DLL module before it can install the hook procedure.</span></span> <span data-ttu-id="00946-111">Per recuperare un handle per il modulo DLL, chiamare la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della dll.</span><span class="sxs-lookup"><span data-stu-id="00946-111">To retrieve a handle to the DLL module, call the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function with the name of the DLL.</span></span> <span data-ttu-id="00946-112">Una volta ottenuto l'handle, è possibile chiamare la funzione [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare un puntatore alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="00946-112">After you have obtained the handle, you can call the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve a pointer to the hook procedure.</span></span> <span data-ttu-id="00946-113">Infine, usare [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) per installare l'indirizzo della procedura di hook nella catena di hook appropriata.</span><span class="sxs-lookup"><span data-stu-id="00946-113">Finally, use [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) to install the hook procedure address in the appropriate hook chain.</span></span> <span data-ttu-id="00946-114">**SetWindowsHookEx** passa l'handle del modulo, un puntatore al punto di ingresso della routine di hook e 0 per l'identificatore del thread, a indicare che la routine hook deve essere associata a tutti i thread nello stesso desktop del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="00946-114">**SetWindowsHookEx** passes the module handle, a pointer to the hook-procedure entry point, and 0 for the thread identifier, indicating that the hook procedure should be associated with all threads in the same desktop as the calling thread.</span></span> <span data-ttu-id="00946-115">Questa sequenza è illustrata nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="00946-115">This sequence is shown in the following example.</span></span>

``` syntax
HOOKPROC hkprcSysMsg;
static HINSTANCE hinstDLL; 
static HHOOK hhookSysMsg; 
 
hinstDLL = LoadLibrary(TEXT("c:\\myapp\\sysmsg.dll")); 
hkprcSysMsg = (HOOKPROC)GetProcAddress(hinstDLL, "SysMessageProc"); 

hhookSysMsg = SetWindowsHookEx( 
                    WH_SYSMSGFILTER,
                    hkprcSysMsg,
                    hinstDLL,
                    0); 
```

<span data-ttu-id="00946-116">È possibile rilasciare una routine hook specifica del thread, ovvero rimuovere il relativo indirizzo dalla catena di hook, chiamando la funzione [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex) , specificando l'handle per la procedura di hook da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="00946-116">You can release a thread-specific hook procedure (remove its address from the hook chain) by calling the [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex) function, specifying the handle to the hook procedure to release.</span></span> <span data-ttu-id="00946-117">Rilasciare una procedura hook non appena l'applicazione non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="00946-117">Release a hook procedure as soon as your application no longer needs it.</span></span>

<span data-ttu-id="00946-118">È possibile rilasciare una routine hook globale usando [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex), ma questa funzione non libera la DLL contenente la procedura di hook.</span><span class="sxs-lookup"><span data-stu-id="00946-118">You can release a global hook procedure by using [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex), but this function does not free the DLL containing the hook procedure.</span></span> <span data-ttu-id="00946-119">Ciò è dovuto al fatto che le routine hook globali vengono chiamate nel contesto del processo di ogni applicazione sul desktop, causando una chiamata implicita alla funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per tutti questi processi.</span><span class="sxs-lookup"><span data-stu-id="00946-119">This is because global hook procedures are called in the process context of every application in the desktop, causing an implicit call to the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function for all of those processes.</span></span> <span data-ttu-id="00946-120">Poiché non è possibile effettuare una chiamata alla funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per un altro processo, non esiste alcun modo per liberare la dll.</span><span class="sxs-lookup"><span data-stu-id="00946-120">Because a call to the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function cannot be made for another process, there is then no way to free the DLL.</span></span> <span data-ttu-id="00946-121">Il sistema infine libera la DLL dopo che tutti i processi collegati in modo esplicito alla DLL sono stati terminati o sono denominati **FreeLibrary** e tutti i processi che hanno chiamato la routine hook hanno ripreso l'elaborazione all'esterno della dll.</span><span class="sxs-lookup"><span data-stu-id="00946-121">The system eventually frees the DLL after all processes explicitly linked to the DLL have either terminated or called **FreeLibrary** and all processes that called the hook procedure have resumed processing outside the DLL.</span></span>

<span data-ttu-id="00946-122">Un metodo alternativo per l'installazione di una procedura di hook globale è fornire una funzione di installazione nella DLL, insieme alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="00946-122">An alternative method for installing a global hook procedure is to provide an installation function in the DLL, along with the hook procedure.</span></span> <span data-ttu-id="00946-123">Con questo metodo, l'applicazione di installazione non necessita dell'handle per il modulo DLL.</span><span class="sxs-lookup"><span data-stu-id="00946-123">With this method, the installing application does not need the handle to the DLL module.</span></span> <span data-ttu-id="00946-124">Tramite il collegamento con la DLL, l'applicazione ottiene l'accesso alla funzione di installazione.</span><span class="sxs-lookup"><span data-stu-id="00946-124">By linking with the DLL, the application gains access to the installation function.</span></span> <span data-ttu-id="00946-125">La funzione di installazione può fornire l'handle del modulo DLL e altri dettagli nella chiamata a [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).</span><span class="sxs-lookup"><span data-stu-id="00946-125">The installation function can supply the DLL module handle and other details in the call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).</span></span> <span data-ttu-id="00946-126">La DLL può inoltre contenere una funzione che rilascia la routine hook globale; l'applicazione può chiamare questa funzione di rilascio hook quando viene terminata.</span><span class="sxs-lookup"><span data-stu-id="00946-126">The DLL can also contain a function that releases the global hook procedure; the application can call this hook-releasing function when terminating.</span></span>

## <a name="monitoring-system-events"></a><span data-ttu-id="00946-127">Monitoraggio degli eventi di sistema</span><span class="sxs-lookup"><span data-stu-id="00946-127">Monitoring System Events</span></span>

<span data-ttu-id="00946-128">Nell'esempio seguente vengono utilizzate diverse procedure Hook specifiche dei thread per monitorare il sistema per gli eventi che interessano un thread.</span><span class="sxs-lookup"><span data-stu-id="00946-128">The following example uses a variety of thread-specific hook procedures to monitor the system for events affecting a thread.</span></span> <span data-ttu-id="00946-129">Viene illustrato come elaborare gli eventi per i tipi di routine hook seguenti:</span><span class="sxs-lookup"><span data-stu-id="00946-129">It demonstrates how to process events for the following types of hook procedures:</span></span>

-   <span data-ttu-id="00946-130">**CALLWNDPROC di WH \_**</span><span class="sxs-lookup"><span data-stu-id="00946-130">**WH\_CALLWNDPROC**</span></span>
-   <span data-ttu-id="00946-131">**\_CBT WH**</span><span class="sxs-lookup"><span data-stu-id="00946-131">**WH\_CBT**</span></span>
-   <span data-ttu-id="00946-132">**DEBUG di WH \_**</span><span class="sxs-lookup"><span data-stu-id="00946-132">**WH\_DEBUG**</span></span>
-   <span data-ttu-id="00946-133">**WH \_ GETmessage**</span><span class="sxs-lookup"><span data-stu-id="00946-133">**WH\_GETMESSAGE**</span></span>
-   <span data-ttu-id="00946-134">**\_tastiera WH**</span><span class="sxs-lookup"><span data-stu-id="00946-134">**WH\_KEYBOARD**</span></span>
-   <span data-ttu-id="00946-135">**\_mouse WH**</span><span class="sxs-lookup"><span data-stu-id="00946-135">**WH\_MOUSE**</span></span>
-   <span data-ttu-id="00946-136">**MSGFILTER di WH \_**</span><span class="sxs-lookup"><span data-stu-id="00946-136">**WH\_MSGFILTER**</span></span>

<span data-ttu-id="00946-137">L'utente può installare e rimuovere una procedura di hook usando il menu.</span><span class="sxs-lookup"><span data-stu-id="00946-137">The user can install and remove a hook procedure by using the menu.</span></span> <span data-ttu-id="00946-138">Quando viene installata una procedura hook e viene eseguito un evento monitorato dalla procedura, la procedura scrive le informazioni sull'evento nell'area client della finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="00946-138">When a hook procedure is installed and an event that is monitored by the procedure occurs, the procedure writes information about the event to the client area of the application's main window.</span></span>


```
#include <windows.h>
#include <strsafe.h>
#include "app.h"

#pragma comment( lib, "user32.lib") 
#pragma comment( lib, "gdi32.lib")

#define NUMHOOKS 7 
 
// Global variables 
 
typedef struct _MYHOOKDATA 
{ 
    int nType; 
    HOOKPROC hkprc; 
    HHOOK hhook; 
} MYHOOKDATA; 
 
MYHOOKDATA myhookdata[NUMHOOKS]; 

HWND gh_hwndMain;

// Hook procedures

LRESULT WINAPI CallWndProc(int, WPARAM, LPARAM);
LRESULT WINAPI CBTProc(int, WPARAM, LPARAM);
LRESULT WINAPI DebugProc(int, WPARAM, LPARAM);
LRESULT WINAPI GetMsgProc(int, WPARAM, LPARAM);
LRESULT WINAPI KeyboardProc(int, WPARAM, LPARAM);
LRESULT WINAPI MouseProc(int, WPARAM, LPARAM);
LRESULT WINAPI MessageProc(int, WPARAM, LPARAM);

void LookUpTheMessage(PMSG, LPTSTR);
 
LRESULT WINAPI MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    static BOOL afHooks[NUMHOOKS]; 
    int index; 
    static HMENU hmenu; 
 
    gh_hwndMain = hwndMain;
    
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Save the menu handle
 
            hmenu = GetMenu(hwndMain); 
 
            // Initialize structures with hook data. The menu-item identifiers are 
            // defined as 0 through 6 in the header file app.h. They can be used to 
            // identify array elements both here and during the WM_COMMAND message. 
 
            myhookdata[IDM_CALLWNDPROC].nType = WH_CALLWNDPROC; 
            myhookdata[IDM_CALLWNDPROC].hkprc = CallWndProc; 
            myhookdata[IDM_CBT].nType = WH_CBT; 
            myhookdata[IDM_CBT].hkprc = CBTProc; 
            myhookdata[IDM_DEBUG].nType = WH_DEBUG; 
            myhookdata[IDM_DEBUG].hkprc = DebugProc; 
            myhookdata[IDM_GETMESSAGE].nType = WH_GETMESSAGE; 
            myhookdata[IDM_GETMESSAGE].hkprc = GetMsgProc; 
            myhookdata[IDM_KEYBOARD].nType = WH_KEYBOARD; 
            myhookdata[IDM_KEYBOARD].hkprc = KeyboardProc; 
            myhookdata[IDM_MOUSE].nType = WH_MOUSE; 
            myhookdata[IDM_MOUSE].hkprc = MouseProc; 
            myhookdata[IDM_MSGFILTER].nType = WH_MSGFILTER; 
            myhookdata[IDM_MSGFILTER].hkprc = MessageProc; 
 
            // Initialize all flags in the array to FALSE. 
 
            memset(afHooks, FALSE, sizeof(afHooks)); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                 // The user selected a hook command from the menu. 
 
                case IDM_CALLWNDPROC: 
                case IDM_CBT: 
                case IDM_DEBUG: 
                case IDM_GETMESSAGE: 
                case IDM_KEYBOARD: 
                case IDM_MOUSE: 
                case IDM_MSGFILTER: 
 
                    // Use the menu-item identifier as an index 
                    // into the array of structures with hook data. 
 
                    index = LOWORD(wParam); 
 
                    // If the selected type of hook procedure isn't 
                    // installed yet, install it and check the 
                    // associated menu item. 
 
                    if (!afHooks[index]) 
                    { 
                        myhookdata[index].hhook = SetWindowsHookEx( 
                            myhookdata[index].nType, 
                            myhookdata[index].hkprc, 
                            (HINSTANCE) NULL, GetCurrentThreadId()); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_CHECKED); 
                        afHooks[index] = TRUE; 
                    } 
 
                    // If the selected type of hook procedure is 
                    // already installed, remove it and remove the 
                    // check mark from the associated menu item. 
 
                    else 
                    { 
                        UnhookWindowsHookEx(myhookdata[index].hhook); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_UNCHECKED); 
                        afHooks[index] = FALSE; 
                    } 
 
                default: 
                    return (DefWindowProc(hwndMain, uMsg, wParam, 
                        lParam)); 
            } 
            break; 
 
            //
            // Process other messages. 
            //
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
/**************************************************************** 
  WH_CALLWNDPROC hook procedure 
 ****************************************************************/ 
 
LRESULT WINAPI CallWndProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szCWPBuf[256]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch;
    HRESULT hResult; 
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szCWPBuf, 256/sizeof(TCHAR),  
               "CALLWNDPROC - tsk: %ld, msg: %s, %d times   ", 
                wParam, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: writer error handler
            }
            hResult = StringCchLength(szCWPBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 15, szCWPBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_GETMESSAGE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK GetMsgProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szMSGBuf[256]; 
    CHAR szRem[16]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0) // do not process message 
        return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case HC_ACTION: 
            switch (wParam) 
            { 
                case PM_REMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_REMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                case PM_NOREMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_NOREMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                default:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
            } 
 
            // Call an application-defined function that converts a 
            // message constant to a string and copies it to a 
            // buffer. 
 
            LookUpTheMessage((PMSG) lParam, szMsg); 
 
            hdc = GetDC(gh_hwndMain);
            hResult = StringCchPrintf(szMSGBuf, 256/sizeof(TCHAR), 
                "GETMESSAGE - wParam: %s, msg: %s, %d times   ", 
                szRem, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szMSGBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 35, szMSGBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_DEBUG hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK DebugProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),   
                "DEBUG - nCode: %d, tsk: %ld, %d times   ", 
                nCode,wParam, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 55, szBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_CBT hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK CBTProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szCode[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, 
            lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HCBT_ACTIVATE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_ACTIVATE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CLICKSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CLICKSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CREATEWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CREATEWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_DESTROYWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_DESTROYWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_KEYSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_KEYSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MINMAX:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MINMAX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MOVESIZE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MOVESIZE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_QS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_QS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SETFOCUS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SETFOCUS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SYSCOMMAND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SYSCOMMAND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
    } 
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "CBT -  nCode: %s, tsk: %ld, %d times   ",
        szCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 75, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MOUSE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MouseProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process the message 
        return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, 
            wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), 
        "MOUSE - nCode: %d, msg: %s, x: %d, y: %d, %d times   ", 
        nCode, szMsg, LOWORD(lParam), HIWORD(lParam), c++); 
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    TextOut(hdc, 2, 95, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_KEYBOARD hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK KeyboardProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "KEYBOARD - nCode: %d, vk: %d, %d times ", nCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 115, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MSGFILTER hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MessageProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    CHAR szCode[32]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case MSGF_DIALOGBOX:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_DIALOGBOX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_MENU:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_MENU");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_SCROLLBAR:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_SCROLLBAR");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchPrintf(szCode, 128/sizeof(TCHAR), "Unknown: %d", nCode);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
            break; 
    } 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),  
        "MSGFILTER  nCode: %s, msg: %s, %d times    ", 
        szCode, szMsg, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 135, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, wParam, lParam); 
}
```



 

 
