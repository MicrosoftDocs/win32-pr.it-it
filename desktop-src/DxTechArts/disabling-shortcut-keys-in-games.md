---
title: Disabilitazione dei tasti di scelta rapida nei giochi
description: Questo articolo descrive come disabilitare temporaneamente i tasti di scelta rapida in Microsoft Windows per evitare interruzioni del gioco per i giochi a schermo intero.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eae2ee1b30e78b17440f2c6144c529de4e6d7b6272a5d497de5c5e631ac1c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070521"
---
# <a name="disabling-shortcut-keys-in-games"></a>Disabilitazione dei tasti di scelta rapida nei giochi

Questo articolo descrive come disabilitare temporaneamente i tasti di scelta rapida in Microsoft Windows per evitare interruzioni del gioco per i giochi a schermo intero. I tasti MAIUSC e CTRL vengono spesso usati come pulsanti di fuoco o di esecuzione nei giochi. Se gli utenti premono accidentalmente il tasto Windows (che si trova vicino a questi tasti), possono far saltare improvvisamente fuori dall'applicazione, causando un'esperienza di gioco insoddrizante. Il semplice uso del tasto MAIUSC come pulsante di gioco può inavvertitamente eseguire il collegamento Tasti permanenti che può visualizzare una finestra di dialogo di avviso. Per evitare questi problemi, è necessario disabilitare queste chiavi durante l'esecuzione in modalità schermo intero e abilitare le chiavi ai gestori predefiniti quando vengono eseguite in modalità a finestre o uscire dall'applicazione.

Questo articolo descrive come eseguire le operazioni seguenti:

-   [Disabilitare il tasto Windows tastiera con un hook da tastiera](#disable-the-windows-key-with-a-keyboard-hook)
-   [Disabilitare i tasti di scelta rapida per l'accessibilità](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>Disabilitare il tasto Windows tastiera con un hook da tastiera

Usare un gancio da tastiera di basso livello per filtrare Windows tasto da elaborare. L'hook della tastiera di basso livello illustrato nell'esempio 1 rimane attivo anche se un utente riduce a icona la finestra o passa a un'altra applicazione. Ciò significa che è necessario assicurarsi che la chiave Windows non sia disabilitata quando l'applicazione viene disattivata. Il codice nell'esempio 1 esegue questa operazione gestendo il messaggio WM \_ ACTIVATEAPP.

> [!Note]  
> Questo metodo funziona in Windows 2000 e versioni successive di Windows. Questo metodo funziona anche con gli account utente con privilegi minimi (noti anche come account utente con privilegi limitati).

 

Questo metodo viene usato da DXUT ed è illustrato nell'esempio di codice seguente.

**Esempio 1. Uso di un hook della tastiera di basso livello per disabilitare il tasto Windows tastiera**


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



## <a name="disable-the-accessibility-shortcut-keys"></a>Disabilitare i tasti di scelta rapida per l'accessibilità

Windows include funzionalità di accessibilità come StickyKeys, FilterKeys e ToggleKeys (vedere Windows [Accessibilità](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))). Ognuna di queste funzioni ha uno scopo diverso. StickyKeys, ad esempio, è progettato per le persone che hanno difficoltà a tenere premuto due o più chiavi contemporaneamente. Ognuna di queste funzionalità di accessibilità ha anche un tasto di scelta rapida che consente di attivarlo o disattivarlo. Ad esempio, il tasto di scelta rapida Tasti permanenti viene attivato premendo il tasto MAIUSC cinque volte. Se il tasto MAIUSC viene usato anche nel gioco, l'utente potrebbe attivare accidentalmente questo collegamento durante il gioco. Quando il collegamento viene attivato, Windows (per impostazione predefinita) visualizza un avviso in una finestra di dialogo, che causa Windows ridurre al minimo un gioco in esecuzione in modalità schermo intero. Questo, naturalmente, può avere un effetto drastico sul gioco.

Le funzionalità di accessibilità sono necessarie per alcuni clienti e non interferiscono con i giochi a schermo intero; Pertanto, non è consigliabile modificare le impostazioni di accessibilità. Tuttavia, poiché i tasti di scelta rapida per le funzionalità di accessibilità possono interrompere il gioco se attivato accidentalmente, è consigliabile disattivare un collegamento di accessibilità solo quando tale funzionalità non è abilitata chiamando [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).

Un collegamento di accessibilità disattivato da [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) rimane disattivato anche dopo la chiusura dell'applicazione. Ciò significa che è necessario ripristinare le impostazioni prima di uscire dall'applicazione. Poiché è possibile che l'applicazione non venga chiusa correttamente, è necessario scrivere queste impostazioni nell'archiviazione permanente in modo che possano essere ripristinate quando l'applicazione viene eseguita di nuovo. È anche possibile usare un gestore eccezioni per ripristinare queste impostazioni in caso di arresto anomalo del sistema.

**Per disattivare questi tasti di scelta rapida**

1.  Acquisire le impostazioni di accessibilità correnti prima di disabilitarle.
2.  Disabilitare il collegamento di accessibilità quando l'applicazione passa alla modalità schermo intero se la funzionalità di accessibilità è disattivata.
3.  Ripristinare le impostazioni di accessibilità quando l'applicazione passa in modalità finestra o si chiude.

Questo metodo viene usato in DXUT ed è illustrato nell'esempio di codice seguente.

> [!Note]  
> Questo metodo funziona quando viene eseguito in un account utente limitato.

 

**Esempio 2. Disabilitazione dei tasti di scelta rapida per l'accessibilità**


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



 

 