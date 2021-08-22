---
title: Uso dei caret
description: In questa sezione vengono forniti esempi di codice che illustrano come eseguire attività correlate ai caret.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- risorse, caret
- caret, creazione
- caret, visualizzazione
- caret, eliminazione
- caret, nascondere
- cursori, tempi di lampeggiamento
- righe lampeggianti
- blocchi lampeggianti
- bitmap lampeggianti
- creazione di caret
- visualizzazione di caret
- nascondere i caret
- eliminazione di caret
- blink times
- input utente, input da tastiera
- acquisizione dell'input dell'utente, input da tastiera
- input da tastiera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c930931df8ce401fbed8cc9af16db3cb52de08ebe9cf539109b426497318d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472647"
---
# <a name="using-carets"></a>Uso dei caret

In questa sezione sono disponibili esempi di codice per le attività seguenti:

-   [Creazione e visualizzazione di un punto di controllo](#creating-and-displaying-a-caret)
-   [Nascondere un punto di controllo](#hiding-a-caret)
-   [Eliminazione di un punto di controllo](#destroying-a-caret)
-   [Regolazione dell'ora di lampeggiamento](#adjusting-the-blink-time)
-   [Elaborazione dell'input da tastiera](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Creazione e visualizzazione di un punto di controllo

Quando si riceve lo stato attivo della tastiera, la finestra deve creare e visualizzare il punto di interesse. Usare la [**funzione CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) per creare un punto di accesso nella finestra specificata. È quindi possibile chiamare [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) per impostare la posizione corrente del cursore e [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) per rendere visibile il cursore.

Il sistema invia il messaggio [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) alla finestra che riceve lo stato attivo della tastiera. Pertanto, un'applicazione deve creare e visualizzare il punto di interesse durante l'elaborazione del messaggio.


```
HWND hwnd,       // window handle 
int x;           // horizontal coordinate of cursor 
int y;           // vertical coordinate of cursor 
int nWidth;      // width of cursor 
int nHeight;     // height of cursor 
char *lpszChar;  // pointer to character 
 
    case WM_SETFOCUS: 
 
    // Create a solid black caret. 
        CreateCaret(hwnd, (HBITMAP) NULL, nWidth, nHeight); 
 
    // Adjust the caret position, in client coordinates. 
        SetCaretPos(x, y); 
 
    // Display the caret. 
        ShowCaret(hwnd); 
 
        break; 
```



Per creare un punto di selezione basato su una bitmap, è necessario specificare un handle di bitmap quando si usa [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret). È possibile usare un'applicazione grafica per creare la bitmap e un compilatore di risorse per aggiungere la bitmap alle risorse dell'applicazione. L'applicazione può quindi usare la [**funzione LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) per caricare l'handle della bitmap. Ad esempio, è possibile sostituire la **riga CreateCaret** nell'esempio precedente con le righe seguenti per creare un punto di interruzione bitmap.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



In alternativa, è possibile usare la [**funzione CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) o [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) per recuperare l'handle della bitmap del punto di accesso. Per altre informazioni sulle bitmap, vedere [Bitmap.](/windows/desktop/gdi/bitmaps)

Se l'applicazione specifica un handle di bitmap, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignora i parametri di larghezza e altezza. La bitmap definisce le dimensioni del caret.

## <a name="hiding-a-caret"></a>Nascondere un punto di controllo

Ogni volta che l'applicazione ridisegna una schermata durante l'elaborazione di un messaggio diverso da [**WM \_ PAINT,**](/windows/desktop/gdi/wm-paint)deve rendere invisibile il punto di accesso usando la [**funzione HideCaret.**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) Al termine del disegno dell'applicazione, visualizzare nuovamente il caret usando la [**funzione ShowCaret.**](/windows/desktop/api/Winuser/nf-winuser-showcaret) Se l'applicazione elabora il **messaggio WM \_ PAINT,** non è necessario nascondere e visualizzare nuovamente il caret, perché questa funzione esegue automaticamente questa operazione.

L'esempio di codice seguente mostra come fare in modo che l'applicazione nascondi il punto di controllo durante il disegno di un carattere sullo schermo e durante l'elaborazione [**del messaggio WM \_ CHAR.**](/windows/desktop/inputdev/wm-char)


```
HWND hwnd,   // window handle 
HDC hdc;     // device context 
 
    case WM_CHAR: 
        switch (wParam) 
        { 
            case 0x08: 
             
             // Process a backspace. 
             
                break; 
 
            case 0x09: 
             
             // Process a tab.  
             
                break; 
 
            case 0x0D: 
             
             // Process a carriage return. 
             
                break; 
 
            case 0x1B: 
             
             // Process an escape. 
             
                break; 
 
            case 0x0A: 
             
             // Process a linefeed. 
             
                break; 
 
            default: 
                // Hide the caret. 
                HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                hdc = GetDC(hwnd); 
                SelectObject(hdc, 
                    GetStockObject(SYSTEM_FIXED_FONT)); 
 
                TextOut(hdc, x, y, lpszChar, 1); 
 
                ReleaseDC(hwnd, hdc); 
 
                // Display the caret. 
 
                ShowCaret(hwnd); 
 
        } 
```



Se l'applicazione chiama la funzione [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) più volte senza chiamare [**ShowCaret,**](/windows/desktop/api/Winuser/nf-winuser-showcaret)il caret non verrà visualizzato finché l'applicazione non chiama **anche ShowCaret** lo stesso numero di volte.

## <a name="destroying-a-caret"></a>Eliminazione di un punto di controllo

Quando una finestra perde lo stato attivo della tastiera, il sistema invia il messaggio [**\_ KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus) alla finestra. L'applicazione deve eliminare il caret durante l'elaborazione del messaggio usando la [**funzione DestroyCaret.**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) Nel codice seguente viene illustrato come eliminare un punto di interesse in una finestra che non ha più lo stato attivo della tastiera.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Regolazione dell'ora di lampeggiamento

Nel Windows a 16 bit un'applicazione basata su Windows può chiamare la funzione [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) per salvare l'ora di lampeggiamento corrente, quindi chiamare la funzione [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) per regolare l'ora di lampeggiamento durante l'elaborazione del messaggio [**WM \_ SETFOCUS.**](/windows/desktop/inputdev/wm-setfocus) L'applicazione ripristina l'ora di lampeggiamento salvata per l'uso di altre applicazioni chiamando **SetCaretBlinkTime durante** l'elaborazione del [**messaggio \_ KILLFOCUS WM.**](/windows/desktop/inputdev/wm-killfocus) Tuttavia, questa tecnica non funziona in ambienti multithreading. In particolare, la disattivazione di un'applicazione non è sincronizzata con l'attivazione di un'altra applicazione, in modo che se un'applicazione si blocca, un'altra applicazione può comunque essere attivata.

Le applicazioni devono rispettare l'ora di lampeggiamento scelta dall'utente. La [**funzione SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) deve essere chiamata solo da un'applicazione che consente all'utente di impostare l'ora di lampeggiamento.

## <a name="processing-keyboard-input"></a>Elaborazione dell'input da tastiera

L'esempio seguente illustra come usare un punto di controllo in un editor di testo semplice. Nell'esempio viene aggiornata la posizione del cursore mentre l'utente tipizza caratteri stampabili e vengono utilizzate varie chiavi per spostarsi nell'area client.


```
#define TEXTMATRIX(x, y) *(pTextMatrix + (y * nWindowCharsX) + x) 
// Global variables.
HINSTANCE hinst;                  // current instance 
HBITMAP hCaret;                   // caret bitmap 
HDC hdc;                          // device context  
PAINTSTRUCT ps;                   // client area paint info 
static char *pTextMatrix = NULL;  // points to text matrix 
static int  nCharX,               // width of char. in logical units 
            nCharY,               // height of char. in logical units 
            nWindowX,             // width of client area 
            nWindowY,             // height of client area 
            nWindowCharsX,        // width of client area 
            nWindowCharsY,        // height of client area 
            nCaretPosX,           // x-position of caret 
            nCaretPosY;           // y-position of caret 
static UINT uOldBlink;            // previous blink rate 
int x, y;                         // coordinates for text matrix 
TEXTMETRIC tm;                    // font information 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,            // window handle 
    UINT message,         // type of message 
    UINT wParam,          // additional information 
    LONG lParam)          // additional information 
{ 
 
    switch (message) 
    { 
        case WM_CREATE: 
        // Select a fixed-width system font, and get its text metrics.
 
            hdc = GetDC(hwnd); 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwnd, hdc); 
 
        // Save the avg. width and height of characters. 
 
            nCharX = tm.tmAveCharWidth; 
            nCharY = tm.tmHeight; 
 
            return 0; 
 
        case WM_SIZE: 
        // Determine the width of the client area, in pixels 
        // and in number of characters. 
 
            nWindowX = LOWORD(lParam); 
            nWindowCharsX = max(1, nWindowX/nCharX); 
 
            // Determine the height of the client area, in 
            // pixels and in number of characters. 
 
            nWindowY = HIWORD(lParam); 
            nWindowCharsY = max(1, nWindowY/nCharY); 
 
            // Clear the buffer that holds the text input. 
 
            if (pTextMatrix != NULL) 
                free(pTextMatrix); 
 
            // If there is enough memory, allocate space for the 
            // text input buffer. 
 
            pTextMatrix = malloc(nWindowCharsX * nWindowCharsY); 
 
            if (pTextMatrix == NULL) 
                ErrorHandler("Not enough memory."); 
            else 
                for (y = 0; y < nWindowCharsY; y++) 
                    for (x = 0; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, y) = ' '; 
 
            // Move the caret to the origin. 
 
            SetCaretPos(0, 0); 
 
            return 0; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_HOME:       // Home 
                    nCaretPosX = 0; 
                    break; 
 
                case VK_END:        // End 
                    nCaretPosX = nWindowCharsX - 1; 
                    break; 
 
                case VK_PRIOR:      // Page Up 
                    nCaretPosY = 0; 
                    break; 
 
                case VK_NEXT:       // Page Down 
                    nCaretPosY = nWindowCharsY -1; 
                    break; 
 
                case VK_LEFT:       // Left arrow 
                    nCaretPosX = max(nCaretPosX - 1, 0); 
                    break; 
 
                case VK_RIGHT:      // Right arrow 
                    nCaretPosX = min(nCaretPosX + 1, 
                        nWindowCharsX - 1); 
                    break; 
 
                case VK_UP:         // Up arrow 
                    nCaretPosY = max(nCaretPosY - 1, 0); 
                    break; 
 
                case VK_DOWN:       // Down arrow 
                    nCaretPosY = min(nCaretPosY + 1, 
                        nWindowCharsY - 1); 
                    break; 
 
                case VK_DELETE:     // Delete 
 
                // Move all the characters that followed the 
                // deleted character (on the same line) one 
                // space back (to the left) in the matrix. 
 
                    for (x = nCaretPosX; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, nCaretPosY) = 
                            TEXTMATRIX(x + 1, nCaretPosY); 
 
                    // Replace the last character on the 
                    // line with a space. 
 
                    TEXTMATRIX(nWindowCharsX - 1, 
                        nCaretPosY) = ' '; 
 
                    // The application will draw outside the 
                    // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                    // Redraw the line, adjusted for the 
                    // deleted character. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 
                        nWindowCharsX - nCaretPosX); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // virtual-key processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:          // Backspace 
                // Move the caret back one space, and then 
                // process this like the DEL key. 
 
                    if (nCaretPosX > 0) 
                    { 
                        nCaretPosX--; 
                        SendMessage(hwnd, WM_KEYDOWN, 
                            VK_DELETE, 1L); 
                    } 
                    break; 
 
                case 0x09:          // Tab 
                // Tab stops exist every four spaces, so add 
                // spaces until the user hits the next tab. 
 
                    do 
                    { 
                        SendMessage(hwnd, WM_CHAR, ' ', 1L); 
                    } while (nCaretPosX % 4 != 0); 
                    break; 
 
                case 0x0D:          // Carriage return 
                // Go to the beginning of the next line. 
                // The bottom line wraps around to the top. 
 
                    nCaretPosX = 0; 
 
                    if (++nCaretPosY == nWindowCharsY) 
                        nCaretPosY = 0; 
                    break; 
 
                case 0x1B:        // Escape 
                case 0x0A:        // Linefeed 
                    MessageBeep((UINT) -1); 
                    break; 
 
                default: 
                // Add the character to the text buffer. 
 
                    TEXTMATRIX(nCaretPosX, nCaretPosY) = 
                        (char) wParam; 
 
                // The application will draw outside the 
                // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 1); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    // Prepare to wrap around if you reached the 
                    // end of the line. 
 
                    if (++nCaretPosX == nWindowCharsX) 
                    { 
                        nCaretPosX = 0; 
                        if (++nCaretPosY == nWindowCharsY) 
                            nCaretPosY = 0; 
                    } 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // character processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_PAINT: 
        // Draw all the characters in the buffer, line by line. 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
 
            for (y = 0; y < nWindowCharsY; y++) 
                TextOut(hdc, 0, y * nCharY, &TEXTMATRIX(0, y), 
                    nWindowCharsX); 
 
            EndPaint(hwnd, &ps); 
 
        case WM_SETFOCUS: 
        // The window has the input focus. Load the 
        // application-defined caret resource. 
 
            hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
            // Create the caret. 
 
            CreateCaret(hwnd, hCaret, 0, 0); 
 
            // Adjust the caret position. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            // Display the caret. 
 
            ShowCaret(hwnd); 
 
            break; 
 
        case WM_KILLFOCUS: 
        // The window is losing the input focus, 
        // so destroy the caret. 
 
            DestroyCaret(); 
 
            break; 
 
        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
    } 
 
    return NULL; 
} 
```



 

 