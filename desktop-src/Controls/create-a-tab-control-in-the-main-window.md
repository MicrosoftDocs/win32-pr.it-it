---
title: Come creare un controllo Struttura a schede nella finestra principale
description: L'esempio in questa sezione illustra come creare un controllo Struttura a schede e visualizzarlo nell'area client della finestra principale dell'applicazione.
ms.assetid: 24157B8B-177B-471C-9DA0-548D09EA5F89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b7d945b01c1e6409cf795d7f42f29999830ed1272bb661a9bb13e52cd1e293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320011"
---
# <a name="how-to-create-a-tab-control-in-the-main-window"></a>Come creare un controllo Struttura a schede nella finestra principale

L'esempio in questa sezione illustra come creare un controllo Struttura a schede e visualizzarlo nell'area client della finestra principale dell'applicazione. L'applicazione visualizza una terza finestra (un controllo statico) nell'area di visualizzazione del controllo Struttura a schede. La finestra padre posiziona e ridimensiona il controllo Struttura a schede e il controllo statico quando elabora il [**messaggio WM \_ SIZE.**](/windows/desktop/winmsg/wm-size)

In questo esempio sono presenti sette schede, una per ogni giorno della settimana. Quando l'utente seleziona una scheda, l'applicazione visualizza il nome del giorno corrispondente nel controllo statico.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-tab-control-in-the-main-window"></a>Creare un controllo Struttura a schede nella finestra principale

La funzione seguente crea il controllo Struttura a schede e aggiunge una scheda per ogni giorno della settimana. I nomi dei giorni sono definiti come risorse stringa, numerate consecutivamente a partire da IDS SUNDAY (definite nel file di intestazione delle \_ risorse dell'applicazione). Sia la finestra padre che il controllo Struttura a schede devono avere lo stile della finestra [**WS \_ CLIPSIBLINGS.**](/windows/desktop/winmsg/window-styles) La funzione di inizializzazione dell'applicazione chiama questa funzione dopo aver creato la finestra principale.


```C++
#define DAYS_IN_WEEK 7

// Creates a tab control, sized to fit the specified parent window's client
//   area, and adds some tabs. 
// Returns the handle to the tab control. 
// hwndParent - parent window (the application's main window). 
// 
HWND DoCreateTabControl(HWND hwndParent) 
{ 
    RECT rcClient; 
    INITCOMMONCONTROLSEX icex;
    HWND hwndTab; 
    TCITEM tie; 
    int i; 
    TCHAR achTemp[256];  // Temporary buffer for strings.
 
    // Initialize common controls.
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&icex);
    
    // Get the dimensions of the parent window's client area, and 
    // create a tab control child window of that size. Note that g_hInst
    // is the global instance handle.
    GetClientRect(hwndParent, &rcClient); 
    hwndTab = CreateWindow(WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, rcClient.right, rcClient.bottom, 
        hwndParent, NULL, g_hInst, NULL); 
    if (hwndTab == NULL)
    { 
        return NULL; 
    }
 
    // Add tabs for each day of the week. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = achTemp; 
 
    for (i = 0; i < DAYS_IN_WEEK; i++) 
    { 
        // Load the day string from the string resources. Note that
        // g_hInst is the global instance handle.
        LoadString(g_hInst, IDS_SUNDAY + i, 
                achTemp, sizeof(achTemp) / sizeof(achTemp[0])); 
        if (TabCtrl_InsertItem(hwndTab, i, &tie) == -1) 
        { 
            DestroyWindow(hwndTab); 
            return NULL; 
        } 
    } 
    return hwndTab; 
} 
```



La funzione seguente crea il controllo statico che si trova nell'area di visualizzazione del controllo Struttura a schede. La funzione di inizializzazione dell'applicazione chiama questa funzione dopo aver creato la finestra principale e il controllo Struttura a schede.


```C++
// Creates a child window (a static control) to occupy the tab control's 
//   display area. 
// Returns the handle to the static control. 
// hwndTab - handle of the tab control. 
// 
HWND DoCreateDisplayWindow(HWND hwndTab) 
{ 
    HWND hwndStatic = CreateWindow(WC_STATIC, L"", 
        WS_CHILD | WS_VISIBLE | WS_BORDER, 
        100, 100, 100, 100,        // Position and dimensions; example only.
        hwndTab, NULL, g_hInst,    // g_hInst is the global instance handle
        NULL); 
    return hwndStatic; 
}
```



Le funzioni di esempio seguenti vengono chiamate dalla routine della finestra dell'applicazione. L'applicazione chiama la funzione durante l'elaborazione del messaggio WM SIZE per posizionare e ridimensionare il controllo Struttura a schede per adattarlo `OnSize` all'area client della [**\_**](/windows/desktop/winmsg/wm-size) finestra principale.

Quando si seleziona una scheda, il controllo struttura a schede invia un messaggio [**WM \_ NOTIFY,**](wm-notify.md) specificando il codice di notifica [ \_ TCN SELCHANGE.](tcn-selchange.md) La funzione `OnNotify` dell'applicazione elabora questo codice di notifica impostando il testo del controllo statico.


```C++
// Handles the WM_SIZE message for the main window by resizing the 
//   tab control. 
// hwndTab - handle of the tab control.
// lParam - the lParam parameter of the WM_SIZE message.
//
HRESULT OnSize(HWND hwndTab, LPARAM lParam)
{
    RECT rc; 

    if (hwndTab == NULL)
        return E_INVALIDARG;

    // Resize the tab control to fit the client are of main window.
     if (!SetWindowPos(hwndTab, HWND_TOP, 0, 0, GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), SWP_SHOWWINDOW))
        return E_FAIL;

    return S_OK;
}

// Handles notifications from the tab control, as follows: 
//   TCN_SELCHANGING - always returns FALSE to allow the user to select a 
//     different tab.  
//   TCN_SELCHANGE - loads a string resource and displays it in a static 
//     control on the selected tab.
// hwndTab - handle of the tab control.
// hwndDisplay - handle of the static control. 
// lParam - the lParam parameter of the WM_NOTIFY message.
//
BOOL OnNotify(HWND hwndTab, HWND hwndDisplay, LPARAM lParam)
{
    TCHAR achTemp[256]; // temporary buffer for strings

    switch (((LPNMHDR)lParam)->code)
        {
            case TCN_SELCHANGING:
                {
                    // Return FALSE to allow the selection to change.
                    return FALSE;
                }

            case TCN_SELCHANGE:
                { 
                    int iPage = TabCtrl_GetCurSel(hwndTab); 

                    // Note that g_hInst is the global instance handle.
                    LoadString(g_hInst, IDS_SUNDAY + iPage, achTemp,
                        sizeof(achTemp) / sizeof(achTemp[0])); 
                    LRESULT result = SendMessage(hwndDisplay, WM_SETTEXT, 0,
                        (LPARAM) achTemp); 
                    break;
                } 
        }
        return TRUE;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Struttura a schede](using-tab-controls.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 