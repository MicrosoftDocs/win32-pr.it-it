---
title: Disabilitazione di tasti di scelta rapida nei giochi
description: In questo articolo viene descritto come disabilitare temporaneamente i tasti di scelta rapida in Microsoft Windows per impedire l'esecuzione di giochi da gioco a schermo intero.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff426e0d728150cf5f6ac3cd8d46a711c9b4f8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473526"
---
# <a name="disabling-shortcut-keys-in-games"></a><span data-ttu-id="4fabb-103">Disabilitazione di tasti di scelta rapida nei giochi</span><span class="sxs-lookup"><span data-stu-id="4fabb-103">Disabling Shortcut Keys in Games</span></span>

<span data-ttu-id="4fabb-104">In questo articolo viene descritto come disabilitare temporaneamente i tasti di scelta rapida in Microsoft Windows per impedire l'esecuzione di giochi da gioco a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="4fabb-104">This articles describes how to temporarily disable keyboard shortcuts in Microsoft Windows to prevent disruption of game play for full screen games.</span></span> <span data-ttu-id="4fabb-105">Il tasto MAIUSC e il tasto CTRL vengono spesso usati come pulsanti Fire o Run nei giochi.</span><span class="sxs-lookup"><span data-stu-id="4fabb-105">The SHIFT key and the CTRL key are often used as fire or run buttons in games.</span></span> <span data-ttu-id="4fabb-106">Se gli utenti preme accidentalmente il tasto Windows (che si trova vicino a queste chiavi), possono causare un improvviso salto all'esterno dell'applicazione, che rovina l'esperienza del gioco.</span><span class="sxs-lookup"><span data-stu-id="4fabb-106">If users accidentally press the Windows key (located near these keys), they can cause themselves to suddenly jump out of the application, which ruins the game experience.</span></span> <span data-ttu-id="4fabb-107">Semplicemente l'utilizzo del tasto MAIUSC come pulsante di gioco può eseguire inavvertitamente il collegamento StickyKeys che può visualizzare una finestra di dialogo di avviso.</span><span class="sxs-lookup"><span data-stu-id="4fabb-107">Simply using the SHIFT key as a game button can inadvertently execute the StickyKeys shortcut which may display a warning dialog.</span></span> <span data-ttu-id="4fabb-108">Per evitare questi problemi, è necessario disabilitare queste chiavi durante l'esecuzione in modalità a schermo intero e riabilitare le chiavi ai gestori predefiniti durante l'esecuzione in modalità finestra o uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4fabb-108">To avoid these issues, you should disable these keys when running in full-screen mode, and either enable the keys back to their default handlers when running in windowed mode or exit the application.</span></span>

<span data-ttu-id="4fabb-109">Questo articolo descrive come eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4fabb-109">This article describes how to do the following:</span></span>

-   [<span data-ttu-id="4fabb-110">Disabilitare il tasto Windows con un gancio da tastiera</span><span class="sxs-lookup"><span data-stu-id="4fabb-110">Disable the Windows Key with a Keyboard Hook</span></span>](#disable-the-windows-key-with-a-keyboard-hook)
-   [<span data-ttu-id="4fabb-111">Disabilitare i tasti di scelta rapida per l'accessibilità</span><span class="sxs-lookup"><span data-stu-id="4fabb-111">Disable the Accessibility Shortcut Keys</span></span>](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a><span data-ttu-id="4fabb-112">Disabilitare il tasto Windows con un gancio da tastiera</span><span class="sxs-lookup"><span data-stu-id="4fabb-112">Disable the Windows Key with a Keyboard Hook</span></span>

<span data-ttu-id="4fabb-113">Usare un hook di tastiera di basso livello per filtrare la chiave di Windows da elaborare.</span><span class="sxs-lookup"><span data-stu-id="4fabb-113">Use a low-level keyboard hook to filter out the Windows key from being processed.</span></span> <span data-ttu-id="4fabb-114">L'hook della tastiera di basso livello illustrato nell'esempio 1 rimane attivo anche se un utente riduce la finestra o passa a un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="4fabb-114">The low-level keyboard hook shown in Example 1 remains in effect even if a user minimizes the window or switches to another application.</span></span> <span data-ttu-id="4fabb-115">Ciò significa che è necessario assicurarsi che la chiave Windows non sia disabilitata quando l'applicazione viene disattivata.</span><span class="sxs-lookup"><span data-stu-id="4fabb-115">This means that you must be careful to ensure that the Windows key is not disabled when the application is deactivated.</span></span> <span data-ttu-id="4fabb-116">Il codice nell'esempio 1 esegue questa operazione gestendo il \_ messaggio WM ACTIVATEAPP.</span><span class="sxs-lookup"><span data-stu-id="4fabb-116">The code in Example 1 does this by handling the WM\_ACTIVATEAPP message.</span></span>

> [!Note]  
> <span data-ttu-id="4fabb-117">Questo metodo funziona in Windows 2000 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="4fabb-117">This method works on Windows 2000 and later versions of Windows.</span></span> <span data-ttu-id="4fabb-118">Questo metodo funziona anche con gli account utente con privilegi minimi (noti anche come account utente limitati).</span><span class="sxs-lookup"><span data-stu-id="4fabb-118">This method also works with least-privileged user accounts (also known as limited-user accounts).</span></span>

 

<span data-ttu-id="4fabb-119">Questo metodo viene usato da DXUT ed è illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="4fabb-119">This method is used by DXUT and is illustrated in the following code example.</span></span>

<span data-ttu-id="4fabb-120">**Esempio 1. Uso di un hook di tastiera di basso livello per disabilitare il tasto Windows**</span><span class="sxs-lookup"><span data-stu-id="4fabb-120">**Example 1. Using a low-level keyboard hook to disable the Windows key**</span></span>


```C++
HHOOK g_hKeyboardHook;
BOOL g_bFullscreen;
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Initialization
    g_hKeyboardHook = SetWindowsHookEx( WH_KEYBOARD_LL,  LowLevelKeyboardProc, GetModuleHandle(NULL), 0 );
 
    // 
    // main application code here
    // 
 
    // Cleanup before shutdown
    UnhookWindowsHookEx( g_hKeyboardHook );
}
 
 
LRESULT CALLBACK LowLevelKeyboardProc( int nCode, WPARAM wParam, LPARAM lParam )
{
    if (nCode < 0 || nCode != HC_ACTION )  // do not process message 
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam); 
 
    bool bEatKeystroke = false;
    KBDLLHOOKSTRUCT* p = (KBDLLHOOKSTRUCT*)lParam;
    switch (wParam) 
    {
        case WM_KEYDOWN:  
        case WM_KEYUP:    
        {
            bEatKeystroke = (g_bFullscreen && g_bWindowActive && ((p->vkCode == VK_LWIN) || (p->vkCode == VK_RWIN)));
            break;
        }
    }
 
    if( bEatKeystroke )
        return 1;
    else
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam );
}
 
 
LRESULT CALLBACK WndProc( HWND hWnd, UINT uMsg, WPARAM wParam, LPARAM lParam )
{
    switch( uMsg )
    {
       case WM_ACTIVATEAPP:
            // g_bWindowActive is used to control if the Windows key is filtered by the keyboard hook or not.
            if( wParam == TRUE )
                g_bWindowActive  = true;           
            else 
                g_bWindowActive  = false;           
            break;
    }
}
```



## <a name="disable-the-accessibility-shortcut-keys"></a><span data-ttu-id="4fabb-121">Disabilitare i tasti di scelta rapida per l'accessibilità</span><span class="sxs-lookup"><span data-stu-id="4fabb-121">Disable the Accessibility Shortcut Keys</span></span>

<span data-ttu-id="4fabb-122">Windows include funzionalità di accessibilità, ad esempio StickyKeys, filtro tasti e ToggleKeys (vedere [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span><span class="sxs-lookup"><span data-stu-id="4fabb-122">Windows includes accessibility features such as StickyKeys, FilterKeys, and ToggleKeys (see [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span></span> <span data-ttu-id="4fabb-123">Ognuno di questi scopi è diverso. StickyKeys, ad esempio, è progettato per gli utenti che hanno difficoltà a tenere contemporaneamente due o più chiavi.</span><span class="sxs-lookup"><span data-stu-id="4fabb-123">Each of these serves a different purpose; StickyKeys for example, is designed for people who have difficulty holding down two or more keys simultaneously.</span></span> <span data-ttu-id="4fabb-124">Ognuna di queste funzionalità di accessibilità dispone anche di un tasto di scelta rapida che consente di attivare o disattivare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4fabb-124">Each of these accessibility features also has a keyboard shortcut that allows the feature to be turned on or off.</span></span> <span data-ttu-id="4fabb-125">Ad esempio, il collegamento StickyKeys viene attivato premendo cinque volte il tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="4fabb-125">For example, the StickyKeys shortcut is triggered by pressing the SHIFT key five times.</span></span> <span data-ttu-id="4fabb-126">Se anche il tasto MAIUSC viene usato nel gioco, l'utente potrebbe attivare accidentalmente il collegamento durante il gioco.</span><span class="sxs-lookup"><span data-stu-id="4fabb-126">If the SHIFT key is also used in the game, the user could accidentally trigger this shortcut during game play.</span></span> <span data-ttu-id="4fabb-127">Quando viene attivato il collegamento, Windows (per impostazione predefinita) presenta un avviso in una finestra di dialogo, in modo da consentire a Windows di ridurre al minimo un gioco in esecuzione in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="4fabb-127">When the shortcut is triggered, Windows (by default) presents a warning in a dialog box, which would cause Windows to minimize a game running in full-screen mode.</span></span> <span data-ttu-id="4fabb-128">Questo, ovviamente, può avere un effetto drastico sulla riproduzione del gioco.</span><span class="sxs-lookup"><span data-stu-id="4fabb-128">This, of course, can have a drastic effect on game play.</span></span>

<span data-ttu-id="4fabb-129">Le funzionalità di accessibilità sono necessarie per alcuni clienti e non interferiscono con i giochi a schermo intero; Pertanto, non è necessario modificare le impostazioni di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="4fabb-129">The accessibility features are required for some customers and do not themselves interfere with full-screen games; therefore, you should not change the accessibility settings.</span></span> <span data-ttu-id="4fabb-130">Tuttavia, poiché i tasti di scelta rapida per le funzionalità di accessibilità possono compromettere il gioco se attivato accidentalmente, è consigliabile disattivare un collegamento di accessibilità solo quando tale funzionalità non è abilitata chiamando [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="4fabb-130">However, because the shortcuts for accessibility features can disrupt game play if triggered accidentally, you should turn off an accessibility shortcut only when that feature is not enabled by calling [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span></span>

<span data-ttu-id="4fabb-131">Un collegamento di accessibilità disabilitato da [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) rimane disattivato anche dopo la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4fabb-131">An accessibility shortcut that is turned off by [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) remains turned off even after the application has exited.</span></span> <span data-ttu-id="4fabb-132">Ciò significa che è necessario ripristinare le impostazioni prima di uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4fabb-132">This means that you must restore the settings before exiting the application.</span></span> <span data-ttu-id="4fabb-133">Poiché è possibile che l'applicazione non venga chiusa correttamente, è necessario scrivere queste impostazioni nell'archivio permanente in modo che possano essere ripristinate quando l'applicazione viene eseguita di nuovo.</span><span class="sxs-lookup"><span data-stu-id="4fabb-133">Because it is possible for the application to fail to exit correctly, you should write these settings to persistent storage so that they can be restored when the application is run again.</span></span> <span data-ttu-id="4fabb-134">È anche possibile usare un gestore di eccezioni per ripristinare queste impostazioni se si verifica un arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="4fabb-134">You could also use an exception handler to restore these settings if a crash occurs.</span></span>

<span data-ttu-id="4fabb-135">**Per disattivare questi tasti di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="4fabb-135">**To turn off these shortcuts**</span></span>

1.  <span data-ttu-id="4fabb-136">Acquisisci le impostazioni di accessibilità correnti prima di disattivarle.</span><span class="sxs-lookup"><span data-stu-id="4fabb-136">Capture the current accessibility settings before disabling them.</span></span>
2.  <span data-ttu-id="4fabb-137">Disabilitare il collegamento di accessibilità quando l'applicazione passa alla modalità schermo intero se la funzionalità di accessibilità è disattivata.</span><span class="sxs-lookup"><span data-stu-id="4fabb-137">Disable the accessibility shortcut when the application goes into full-screen mode if the accessibility feature is off.</span></span>
3.  <span data-ttu-id="4fabb-138">Ripristinare le impostazioni di accessibilità quando l'applicazione passa alla modalità finestra o viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="4fabb-138">Restore the accessibility settings when the application goes into windowed mode or exits.</span></span>

<span data-ttu-id="4fabb-139">Questo metodo viene usato in DXUT ed è illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="4fabb-139">This method is used in DXUT, and is illustrated in the following code example.</span></span>

> [!Note]  
> <span data-ttu-id="4fabb-140">Questo metodo funziona quando viene eseguito con un account utente limitato.</span><span class="sxs-lookup"><span data-stu-id="4fabb-140">This method works when running on a limited user account.</span></span>

 

<span data-ttu-id="4fabb-141">**Esempio 2. Disabilitazione di tasti di scelta rapida accessibilità**</span><span class="sxs-lookup"><span data-stu-id="4fabb-141">**Example 2. Disabling accessibility shortcut keys**</span></span>


```C++
STICKYKEYS g_StartupStickyKeys = {sizeof(STICKYKEYS), 0};
TOGGLEKEYS g_StartupToggleKeys = {sizeof(TOGGLEKEYS), 0};
FILTERKEYS g_StartupFilterKeys = {sizeof(FILTERKEYS), 0};    
 
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Save the current sticky/toggle/filter key settings so they can be restored them later
    SystemParametersInfo(SPI_GETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
    SystemParametersInfo(SPI_GETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
    SystemParametersInfo(SPI_GETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
 
    // Disable when full screen
    AllowAccessibilityShortcutKeys( true );
 
    // Restore back when going to windowed or shutting down
    AllowAccessibilityShortcutKeys( false );
}
 
 
void AllowAccessibilityShortcutKeys( bool bAllowKeys )
{
    if( bAllowKeys )
    {
        // Restore StickyKeys/etc to original state and enable Windows key      
        STICKYKEYS sk = g_StartupStickyKeys;
        TOGGLEKEYS tk = g_StartupToggleKeys;
        FILTERKEYS fk = g_StartupFilterKeys;
        
        SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
        SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
        SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
    }
    else
    {
        // Disable StickyKeys/etc shortcuts but if the accessibility feature is on, 
        // then leave the settings alone as its probably being usefully used
 
        STICKYKEYS skOff = g_StartupStickyKeys;
        if( (skOff.dwFlags & SKF_STICKYKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            skOff.dwFlags &= ~SKF_HOTKEYACTIVE;
            skOff.dwFlags &= ~SKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &skOff, 0);
        }
 
        TOGGLEKEYS tkOff = g_StartupToggleKeys;
        if( (tkOff.dwFlags & TKF_TOGGLEKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            tkOff.dwFlags &= ~TKF_HOTKEYACTIVE;
            tkOff.dwFlags &= ~TKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &tkOff, 0);
        }
 
        FILTERKEYS fkOff = g_StartupFilterKeys;
        if( (fkOff.dwFlags & FKF_FILTERKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            fkOff.dwFlags &= ~FKF_HOTKEYACTIVE;
            fkOff.dwFlags &= ~FKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &fkOff, 0);
        }
    }
}
```



 

 