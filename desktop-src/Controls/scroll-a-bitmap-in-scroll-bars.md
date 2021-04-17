---
title: Come scorrere una bitmap
description: In questa sezione vengono descritte le modifiche che è possibile apportare alla routine della finestra principale di un'applicazione per consentire all'utente di scorrere una bitmap.
ms.assetid: FA6FEA49-25EB-4C18-AD07-74BD77501906
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01a93fbb005b75d7cd860bc8545c4e77a80767
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474390"
---
# <a name="how-to-scroll-a-bitmap"></a>Come scorrere una bitmap

In questa sezione vengono descritte le modifiche che è possibile apportare alla routine della finestra principale di un'applicazione per consentire all'utente di scorrere una bitmap.

Nell'esempio è inclusa una voce di menu che copia il contenuto della schermata in una bitmap e visualizza la bitmap nell'area client. Nell'esempio vengono inoltre elaborati i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) generati dalle barre di scorrimento in modo che l'utente possa scorrere la bitmap orizzontalmente e verticalmente. A differenza dell'esempio relativo al testo a scorrimento, l'esempio bitmap usa la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) per creare la parte non valida dell'area client.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="processing-the-wm_create-message"></a>Elaborazione del \_ messaggio di creazione WM

Quando viene elaborato il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) , vengono inizializzate le variabili necessarie per lo scorrimento. Usare la funzione [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) per creare un contesto di dispositivo compatibile (DC), la funzione [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) per creare una bitmap e la funzione [**SelezionaOggetto**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) per selezionare la bitmap per il controller di dominio. Si noti che un controller di dominio compatibile è noto anche come controller di dominio di memoria.

Vengono recuperate le informazioni specifiche del dispositivo sul dispositivo di visualizzazione. Se per la schermata viene creato un controller di dominio compatibile, come nell'esempio, usare la funzione [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) per ottenere queste informazioni. Le informazioni includono il numero di bit di colore adiacenti per pixel, il numero di piani di colore e l'altezza e la larghezza del controller di dominio.

### <a name="processing-the-wm_size-message"></a>Elaborazione del \_ messaggio dimensioni WM

L'elaborazione del messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) richiede la regolazione dell'intervallo di scorrimento e della posizione, in modo che rifletta le dimensioni dell'area client e la bitmap che verrà visualizzata.

La funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) imposta i valori di posizione minimo e massimo, le dimensioni della pagina e la posizione di scorrimento per una barra di scorrimento.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Elaborazione dei \_ messaggi WM HSCROLL e WM \_ VSCROLL

Quando vengono elaborati i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) , viene esaminato il codice di richiesta della barra di scorrimento e la posizione di scorrimento è impostata su un nuovo valore che riflette l'azione di scorrimento dell'utente. Se la posizione di scorrimento si trova all'interno dell'intervallo di scorrimento, la finestra viene spostata nella nuova posizione utilizzando la funzione [**ScrollWindow**](/windows/desktop/api/Winuser/nf-winuser-scrollwindow) . La posizione della casella di scorrimento viene quindi modificata tramite la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .

Dopo lo scorrimento di una finestra, parte dell'area client viene resa non valida. Per assicurarsi che l'area non valida venga aggiornata, usare la funzione [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) per generare un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . Quando si elabora il messaggio di **\_ disegno WM** , un'applicazione deve ridisegnare l'area non valida nella parte inferiore dell'area client. Durante lo scorrimento o il ridimensionamento dell'area client, nell'esempio viene utilizzata la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) per copiare la parte appropriata della bitmap nella parte non valida dell'area client.

## <a name="example-of-scrolling-a-bitmap"></a>Esempio di scorrimento di una bitmap

L'esempio seguente consente all'utente di acquisire il contenuto della schermata in una bitmap e di scorrere la bitmap nell'area client. Il contenuto della schermata viene acquisito quando l'utente fa clic con il pulsante destro del mouse sull'area client.


```C++
LRESULT CALLBACK MyBitmapWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    HDC hdc; 
    PAINTSTRUCT ps; 
    SCROLLINFO si; 
 
    // These variables are required by BitBlt. 
    static HDC hdcWin;           // window DC 
    static HDC hdcScreen;        // DC for entire screen 
    static HDC hdcScreenCompat;  // memory DC for screen 
    static HBITMAP hbmpCompat;   // bitmap handle to old DC 
    static BITMAP bmp;           // bitmap data structure 
    static BOOL fBlt;            // TRUE if BitBlt occurred 
    static BOOL fScroll;         // TRUE if scrolling occurred 
    static BOOL fSize;           // TRUE if fBlt & WM_SIZE 
 
    // These variables are required for horizontal scrolling. 
    static int xMinScroll;       // minimum horizontal scroll value 
    static int xCurrentScroll;   // current horizontal scroll value 
    static int xMaxScroll;       // maximum horizontal scroll value 
 
    // These variables are required for vertical scrolling. 
    static int yMinScroll;       // minimum vertical scroll value 
    static int yCurrentScroll;   // current vertical scroll value 
    static int yMaxScroll;       // maximum vertical scroll value 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create a normal DC and a memory DC for the entire 
            // screen. The normal DC provides a snapshot of the 
            // screen contents. The memory DC keeps a copy of this 
            // snapshot in the associated bitmap. 
            hdcScreen = CreateDC(L"DISPLAY", (PCTSTR) NULL, 
                (PCTSTR) NULL, (CONST DEVMODE *) NULL); 
            hdcScreenCompat = CreateCompatibleDC(hdcScreen); 
 
            // Retrieve the metrics for the bitmap associated with the 
            // regular device context. 
            bmp.bmBitsPixel = 
                (BYTE) GetDeviceCaps(hdcScreen, BITSPIXEL); 
            bmp.bmPlanes = (BYTE) GetDeviceCaps(hdcScreen, PLANES); 
            bmp.bmWidth = GetDeviceCaps(hdcScreen, HORZRES); 
            bmp.bmHeight = GetDeviceCaps(hdcScreen, VERTRES); 
 
            // The width must be byte-aligned. 
            bmp.bmWidthBytes = ((bmp.bmWidth + 15) &~15)/8; 
 
            // Create a bitmap for the compatible DC. 
            hbmpCompat = CreateBitmap(bmp.bmWidth, bmp.bmHeight, 
                bmp.bmPlanes, bmp.bmBitsPixel, (CONST VOID *) NULL); 
 
            // Select the bitmap for the compatible DC. 
            SelectObject(hdcScreenCompat, hbmpCompat); 
 
            // Initialize the flags. 
            fBlt = FALSE; 
            fScroll = FALSE; 
            fSize = FALSE; 
 
            // Initialize the horizontal scrolling variables. 
            xMinScroll = 0; 
            xCurrentScroll = 0; 
            xMaxScroll = 0; 
 
            // Initialize the vertical scrolling variables. 
            yMinScroll = 0; 
            yCurrentScroll = 0; 
            yMaxScroll = 0; 
 
            break; 
 
        case WM_SIZE: 
        { 
            int xNewSize; 
            int yNewSize; 
 
            xNewSize = LOWORD(lParam); 
            yNewSize = HIWORD(lParam); 
 
            if (fBlt) 
                fSize = TRUE; 
     
            // The horizontal scrolling range is defined by 
            // (bitmap_width) - (client_width). The current horizontal 
            // scroll value remains within the horizontal scrolling range. 
            xMaxScroll = max(bmp.bmWidth-xNewSize, 0); 
            xCurrentScroll = min(xCurrentScroll, xMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = xMinScroll; 
            si.nMax   = bmp.bmWidth; 
            si.nPage  = xNewSize; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            // The vertical scrolling range is defined by 
            // (bitmap_height) - (client_height). The current vertical 
            // scroll value remains within the vertical scrolling range. 
            yMaxScroll = max(bmp.bmHeight - yNewSize, 0); 
            yCurrentScroll = min(yCurrentScroll, yMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = yMinScroll; 
            si.nMax   = bmp.bmHeight; 
            si.nPage  = yNewSize; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 
 
        case WM_PAINT: 
        { 
            PRECT prect; 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            // If the window has been resized and the user has 
            // captured the screen, use the following call to 
            // BitBlt to paint the window's client area. 
            if (fSize) 
            { 
                BitBlt(ps.hdc, 
                    0, 0, 
                    bmp.bmWidth, bmp.bmHeight, 
                    hdcScreenCompat, 
                    xCurrentScroll, yCurrentScroll, 
                    SRCCOPY); 
 
                fSize = FALSE; 
            } 
 
            // If scrolling has occurred, use the following call to 
            // BitBlt to paint the invalid rectangle. 
            // 
            // The coordinates of this rectangle are specified in the 
            // RECT structure to which prect points. 
            // 
            // Note that it is necessary to increment the seventh 
            // argument (prect->left) by xCurrentScroll and the 
            // eighth argument (prect->top) by yCurrentScroll in 
            // order to map the correct pixels from the source bitmap. 
             if (fScroll) 
            { 
                prect = &ps.rcPaint; 
 
                BitBlt(ps.hdc, 
                    prect->left, prect->top, 
                    (prect->right - prect->left), 
                    (prect->bottom - prect->top), 
                    hdcScreenCompat, 
                    prect->left + xCurrentScroll, 
                    prect->top + yCurrentScroll, 
                    SRCCOPY); 
 
                fScroll = FALSE; 
            } 
 
            EndPaint(hwnd, &ps); 

            break; 
        } 

        case WM_HSCROLL: 
        { 
            int xDelta;     // xDelta = new_pos - current_pos  
            int xNewPos;    // new position 
            int yDelta = 0; 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft left of the scroll box. 
                case SB_PAGEUP: 
                    xNewPos = xCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft right of the scroll box. 
                case SB_PAGEDOWN: 
                    xNewPos = xCurrentScroll + 50; 
                    break; 
 
                // User clicked the left arrow. 
                case SB_LINEUP: 
                    xNewPos = xCurrentScroll - 5; 
                    break; 
 
                // User clicked the right arrow. 
                case SB_LINEDOWN: 
                    xNewPos = xCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    xNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    xNewPos = xCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen width. 
            xNewPos = max(0, xNewPos); 
            xNewPos = min(xMaxScroll, xNewPos); 
 
            // If the current position does not change, do not scroll.
            if (xNewPos == xCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            xDelta = xNewPos - xCurrentScroll; 
 
            // Reset the current scroll position. 
            xCurrentScroll = xNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            break; 
        } 
        
        case WM_VSCROLL: 
        { 
            int xDelta = 0; 
            int yDelta;     // yDelta = new_pos - current_pos 
            int yNewPos;    // new position 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft above the scroll box. 
                case SB_PAGEUP: 
                    yNewPos = yCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft below the scroll box. 
                case SB_PAGEDOWN: 
                    yNewPos = yCurrentScroll + 50; 
                    break; 
 
                // User clicked the top arrow. 
                case SB_LINEUP: 
                    yNewPos = yCurrentScroll - 5; 
                    break; 
 
                // User clicked the bottom arrow. 
                case SB_LINEDOWN: 
                    yNewPos = yCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    yNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    yNewPos = yCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen height. 
            yNewPos = max(0, yNewPos); 
            yNewPos = min(yMaxScroll, yNewPos); 
 
            // If the current position does not change, do not scroll.
            if (yNewPos == yCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            yDelta = yNewPos - yCurrentScroll; 
 
            // Reset the current scroll position. 
            yCurrentScroll = yNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 

        case WM_RBUTTONDOWN:
        {
            // Get the compatible DC of the client area. 
            hdcWin = GetDC(hwnd); 

            // Fill the client area to remove any existing contents. 
            RECT rect;
            GetClientRect(hwnd, &rect);
            FillRect(hdcWin, &rect, (HBRUSH)(COLOR_WINDOW+1));
 
            // Copy the contents of the current screen 
            // into the compatible DC. 
            BitBlt(hdcScreenCompat, 0, 0, bmp.bmWidth, 
                bmp.bmHeight, hdcScreen, 0, 0, SRCCOPY); 
 
            // Copy the compatible DC to the client area.
            BitBlt(hdcWin, 0, 0, bmp.bmWidth, bmp.bmHeight, 
                hdcScreenCompat, 0, 0, SRCCOPY); 
 
            ReleaseDC(hwnd, hdcWin); 
            fBlt = TRUE; 
            break; 
        }

        case WM_DESTROY :
            PostQuitMessage (0);
            return 0;
    }
    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle barre di scorrimento](using-scroll-bars.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 