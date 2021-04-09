---
title: Cornice della finestra personalizzata mediante DWM
description: In questo argomento viene illustrato come utilizzare le API di Gestione finestre desktop (DWM) per creare frame di finestra personalizzati per l'applicazione.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Gestione finestre desktop (DWM), frame di finestra personalizzati
- DWM (Gestione finestre desktop), frame di finestra personalizzati
- frame di finestra personalizzati
- rimozione di frame standard
- estensione di frame client
- Gestione finestre desktop (DWM), estensione di frame client
- DWM (Gestione finestre desktop), estensione di frame client
- Gestione finestre desktop (DWM), rimozione di frame standard
- DWM (Gestione finestre desktop), rimozione di frame standard
- Gestione finestre desktop (DWM), disegno in frame estesi
- DWM (Gestione finestre desktop), disegno in frame estesi
- disegno in frame estesi
- test delle occorrenze
- Gestione finestre desktop (DWM), hit testing
- DWM (Gestione finestre desktop), hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047329"
---
# <a name="custom-window-frame-using-dwm"></a>Cornice della finestra personalizzata mediante DWM

In questo argomento viene illustrato come utilizzare le API di Gestione finestre desktop (DWM) per creare frame di finestra personalizzati per l'applicazione.

-   [Introduzione](#introduction)
-   [Estensione del frame client](#extending-the-client-frame)
-   [Rimozione del frame standard](#removing-the-standard-frame)
-   [Disegno nella finestra cornice estesa](#drawing-in-the-extended-frame-window)
-   [Abilitazione dell'hit testing per il frame personalizzato](#enabling-hit-testing-for-the-custom-frame)
-   [Appendice A: procedura della finestra di esempio](#appendix-a-sample-window-procedure)
-   [Appendice B: disegno del titolo della didascalia](#appendix-b-painting-the-caption-title)
-   [Appendice C: funzione HitTestNCA](#appendix-c-hittestnca-function)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

In Windows Vista e versioni successive, l'aspetto delle aree non client delle finestre dell'applicazione (la barra del titolo, l'icona, il bordo della finestra e i pulsanti della didascalia) sono controllati da DWM. Utilizzando le API di DWM, è possibile modificare il modo in cui DWM esegue il rendering del frame di una finestra.

Una funzionalità delle API di DWM è la possibilità di estendere il frame dell'applicazione nell'area client. In questo modo è possibile integrare un elemento dell'interfaccia utente client, ad esempio una barra degli strumenti, nel frame, fornendo ai controlli dell'interfaccia utente una posizione più evidente nell'interfaccia utente dell'applicazione. Windows Internet Explorer 7 in Windows Vista, ad esempio, integra la barra di spostamento nella cornice della finestra estendendo la parte superiore del frame, come illustrato nello screenshot seguente.

![barra di spostamento integrata nella cornice della finestra.](images/ie7-extendedborder-boxed.png)

La possibilità di estendere la cornice della finestra consente anche di creare frame personalizzati mantenendo l'aspetto della finestra. Ad esempio, Microsoft Office Word 2007 disegna il pulsante di Office e la barra di accesso rapido all'interno del frame personalizzato, fornendo i pulsanti di riduzione a icona standard, Ingrandisci e Chiudi, come illustrato nello screenshot seguente.

![pulsante di Office e barra di accesso rapido in Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Estensione del frame client

La funzionalità per estendere il frame nell'area client viene esposta dalla funzione [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Per estendere il frame, passare l'handle della finestra di destinazione insieme ai valori di inserimento dei margini a **DwmExtendFrameIntoClientArea**. I valori di inserimento dei margini determinano la distanza per estendere il frame nei quattro lati della finestra.

Il codice seguente illustra l'uso di [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) per estendere il frame.


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



Si noti che l'estensione del frame viene eseguita all'interno del messaggio di [**\_ attivazione WM**](/windows/desktop/inputdev/wm-activate) invece che del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) . Ciò garantisce che l'estensione del frame venga gestita correttamente quando la finestra è con le dimensioni predefinite e quando viene ingrandita.

Nell'immagine seguente viene mostrata una cornice di finestra standard (a sinistra) e la stessa cornice della finestra estesa (a destra). Il frame viene esteso usando l'esempio di codice precedente e lo sfondo predefinito Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) ( \_ finestra dei colori + 1).

![Screenshot di uno standard (a sinistra) e di un frame esteso (a destra) con sfondo bianco](images/white-sidebyside.png)

La differenza visiva tra queste due finestre è molto sottile. L'unica differenza tra i due è che il bordo della linea nera sottile dell'area client nella finestra a sinistra non è presente nella finestra a destra. Il motivo di questo bordo mancante è che è incorporato nel frame esteso, ma il resto dell'area client non lo è. Affinché i frame estesi siano visibili, le aree sottostanti ogni lato dei frame estesi devono contenere dati pixel con un valore alfa pari a 0. Il bordo nero intorno all'area client presenta dati pixel in cui tutti i valori di colore (rosso, verde, blu e alfa) vengono impostati su 0. Il resto dello sfondo non ha il valore alfa impostato su 0, quindi il resto del frame esteso non è visibile.

Il modo più semplice per garantire la visibilità dei frame estesi consiste nel disegnare l'intero nero dell'area client. A tale scopo, inizializzare il membro *hbrBackground* della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sull'handle del pennello nero azionario \_ . La figura seguente mostra lo stesso frame standard (a sinistra) e il frame esteso (a destra) mostrati in precedenza. Questa volta, tuttavia, *hbrBackground* è impostato sull'handle di \_ pennello nero ottenuto dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .

![Screenshot di uno standard (a sinistra) e di un frame esteso (a destra) con sfondo nero](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Rimozione del frame standard

Dopo aver esteso il frame dell'applicazione e averlo reso visibile, è possibile rimuovere il frame standard. La rimozione del frame standard consente di controllare la larghezza di ogni lato del frame anziché semplicemente di estendere il frame standard.

Per rimuovere la cornice della finestra standard, è necessario gestire il messaggio [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) , in particolare quando il valore *wParam* è **true** e il valore restituito è 0. In questo modo, l'applicazione usa l'intera area della finestra come area client, rimuovendo il frame standard.

I risultati della gestione del messaggio [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) non sono visibili fino a quando non è necessario ridimensionare l'area client. Fino a quel momento, la visualizzazione iniziale della finestra viene visualizzata con il frame standard e i bordi estesi. Per ovviare a questo problema, è necessario ridimensionare la finestra o eseguire un'azione che avvii un messaggio **WM \_ NCCALCSIZE** al momento della creazione della finestra. Questa operazione può essere eseguita tramite la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per spostare la finestra e ridimensionarla. Il codice seguente illustra una chiamata a **SetWindowPos** che impone l'invio di un messaggio **WM \_ NCCALCSIZE** usando gli attributi Rectangle della finestra corrente e il \_ flag FRAMECHANGED di SWP.


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



La figura seguente mostra il frame standard (a sinistra) e il frame appena esteso senza il frame standard (Right).

![Screenshot di un frame standard (a sinistra) e di un frame personalizzato (a destra)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Disegno nella finestra cornice estesa

Rimuovendo il frame standard, si perde il disegno automatico dell'icona e del titolo dell'applicazione. Per aggiungerli nuovamente all'applicazione, è necessario crearli manualmente. A tale scopo, esaminare prima di tutto la modifica apportata all'area client.

Con la rimozione del frame standard, l'area client è ora costituita dall'intera finestra, incluso il frame esteso. Che include l'area in cui vengono disegnati i pulsanti della didascalia. Nel confronto affiancato riportato di seguito, l'area client sia per il frame standard che per il frame esteso personalizzato viene evidenziata in rosso. L'area client per la finestra cornice standard (a sinistra) è l'area nera. Nella finestra cornice estesa (a destra) l'area client è l'intera finestra.

![Screenshot di un'area client evidenziata in rosso nel frame standard e personalizzato](images/clientarea-sidebyside.png)

Poiché l'intera finestra è l'area client, è possibile creare semplicemente gli elementi desiderati nel frame esteso. Per aggiungere un titolo all'applicazione, è sufficiente creare un testo nell'area appropriata. La figura seguente mostra il testo con tema disegnato nel frame della didascalia personalizzata. Il titolo viene disegnato usando la funzione [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) . Per visualizzare il codice che dipinge il titolo, vedere [Appendice B: disegno del titolo della didascalia](#appendix-b-painting-the-caption-title).

![Screenshot di un frame personalizzato con titolo](images/custom-caption-title.png)

> [!Note]  
> Quando si disegna nel frame personalizzato, prestare attenzione quando si posizionano i controlli dell'interfaccia utente. Poiché l'intera finestra è l'area client, è necessario regolare la posizione del controllo dell'interfaccia utente per ogni larghezza del frame se non si desidera che vengano visualizzate in o nel frame esteso.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Abilitazione dell'hit testing per il frame personalizzato

Un effetto collaterale della rimozione del frame standard è la perdita del comportamento predefinito di ridimensionamento e di trasferimento. Affinché l'applicazione possa emulare correttamente il comportamento della finestra standard, è necessario implementare la logica per gestire l'hit test del pulsante della didascalia e il ridimensionamento del frame o lo stato di trasferimento.

Per l'hit test del pulsante della didascalia, DWM fornisce la funzione [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) . Per eseguire correttamente il test dei pulsanti della didascalia negli scenari di frame personalizzati, i messaggi devono essere prima passati a **DwmDefWindowProc** per la gestione. **DwmDefWindowProc** restituisce **true** se un messaggio viene gestito e **false** in caso contrario. Se il messaggio non viene gestito da **DwmDefWindowProc**, l'applicazione deve gestire il messaggio stesso o passare il messaggio su [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Per il ridimensionamento e lo stato del frame, l'applicazione deve fornire la logica di hit testing e gestire i messaggi di hit test del frame. I messaggi di hit test del frame vengono inviati all'utente tramite il messaggio [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) , anche se l'applicazione crea un frame personalizzato senza il frame standard. Il codice seguente illustra la gestione del messaggio **WM \_ NCHITTEST** quando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) non la gestisce. Per visualizzare il codice della funzione chiamata `HitTestNCA` , vedere [Appendice C: HitTestNCA Function](#appendix-c-hittestnca-function).


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a>Appendice A: procedura della finestra di esempio

Nell'esempio di codice riportato di seguito viene illustrata una routine della finestra e le funzioni di lavoro di supporto utilizzate per creare un'applicazione cornice personalizzata.


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a>Appendice B: disegno del titolo della didascalia

Il codice seguente illustra come disegnare un titolo di didascalia nel frame esteso. Questa funzione deve essere chiamata dall'interno delle chiamate a [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a>Appendice C: funzione HitTestNCA

Il codice seguente illustra la `HitTestNCA` funzione usata nell' [Abilitazione dell'hit testing per il frame personalizzato](#enabling-hit-testing-for-the-custom-frame). Questa funzione gestisce la logica di hit testing per [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) quando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) non gestisce il messaggio.


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari di Gestione finestre desktop](dwm-overview.md)
</dt> </dl>

 

 