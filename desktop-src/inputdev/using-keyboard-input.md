---
title: Uso dell'input da tastiera
description: Questa sezione illustra le attività associate all'input da tastiera.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- input utente, input da tastiera
- acquisizione di input utente, input da tastiera
- input da tastiera
- messaggi di sequenza di tasti
- messaggi di tipo carattere
- caret, input da tastiera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1be8753ec6a5f920f09f6e5376b7988a88de0f9a49551492408e84908bb0c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248273"
---
# <a name="using-keyboard-input"></a>Uso dell'input da tastiera

Una finestra riceve l'input da tastiera sotto forma di messaggi di sequenza di tasti e di caratteri. Il ciclo di messaggi associato alla finestra deve includere il codice per convertire i messaggi di sequenza di tasti nei messaggi di caratteri corrispondenti. Se la finestra visualizza l'input da tastiera nell'area client, deve creare e visualizzare un punto di inserimento per indicare la posizione in cui verrà immesso il carattere successivo. Le sezioni seguenti descrivono il codice necessario per la ricezione, l'elaborazione e la visualizzazione dell'input da tastiera:

-   [Elaborazione di messaggi di sequenza di tasti](#processing-keystroke-messages)
-   [Traduzione di messaggi di tipo carattere](#translating-character-messages)
-   [Elaborazione di messaggi di tipo carattere](#processing-character-messages)
-   [Uso del caret](#using-the-caret)
-   [Visualizzazione dell'input da tastiera](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>Elaborazione di messaggi di sequenza di tasti

La routine della finestra con lo stato attivo della tastiera riceve messaggi di pressione dei tasti quando l'utente digita sulla tastiera. I messaggi di pressione dei tasti [**sono WM \_ KEYDOWN,**](wm-keydown.md) [**WM \_ KEYUP,**](wm-keyup.md) [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)e [**WM \_ SYSKEYUP.**](wm-syskeyup.md) Una tipica routine della finestra ignora tutti i messaggi di pressione dei tasti, ad eccezione **di WM \_ KEYDOWN.** Il sistema invia il **messaggio WM \_ KEYDOWN** quando l'utente preme un tasto.

Quando la routine della finestra riceve il [**messaggio WM \_ KEYDOWN,**](wm-keydown.md) deve esaminare il codice del tasto virtuale che accompagna il messaggio per determinare come elaborare la sequenza di tasti. Il codice della chiave virtuale si trova nel parametro *wParam del* messaggio. In genere, un'applicazione elabora solo le sequenze di tasti generate da tasti non carattere, inclusi i tasti funzione, i tasti di spostamento del cursore e i tasti di scopo speciale, ad esempio INS, DEL, HOME ed END.

L'esempio seguente illustra il framework di routine della finestra utilizzato da un'applicazione tipica per ricevere ed elaborare i messaggi di pressione dei tasti.


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a>Traduzione di messaggi di tipo carattere

Qualsiasi thread che riceve input di caratteri dall'utente deve includere la [**funzione TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) nel ciclo di messaggi. Questa funzione esamina il codice del tasto virtuale di un messaggio di sequenza di tasti e, se il codice corrisponde a un carattere, inserisce un messaggio di tipo carattere nella coda di messaggi. Il messaggio carattere viene rimosso e inviato all'iterazione successiva del ciclo di messaggi. il *parametro wParam* del messaggio contiene il codice carattere.

In generale, il ciclo di messaggi di un thread deve usare la funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) per convertire ogni messaggio, non solo i messaggi con chiave virtuale. Sebbene **TranslateMessage non** abbia alcun effetto su altri tipi di messaggi, garantisce che l'input da tastiera venga tradotto correttamente. L'esempio seguente illustra come includere la funzione **TranslateMessage** in un tipico ciclo di messaggi di thread.


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a>Elaborazione di messaggi di tipo carattere

Una routine della finestra riceve un messaggio di tipo carattere quando la [**funzione TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) converte un codice di chiave virtuale corrispondente a un tasto di scelta. I messaggi di tipo carattere [**sono WM \_ CHAR,**](wm-char.md) [**WM \_ DEADCHAR,**](wm-deadchar.md) [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)e [**WM \_ SYSDEADCHAR.**](wm-sysdeadchar.md) Una tipica routine della finestra ignora tutti i messaggi di tipo carattere ad eccezione **di WM \_ CHAR.** La **funzione TranslateMessage** genera un **messaggio WM \_ CHAR** quando l'utente preme uno dei tasti seguenti:

-   Qualsiasi tasto di scelta
-   BACKSPACE
-   ENTER (ritorno a capo)
-   ESC
-   MAIUSC+INVIO (avanzamento riga)
-   TAB

Quando una routine della finestra riceve il [**messaggio WM \_ CHAR,**](wm-char.md) deve esaminare il codice carattere che accompagna il messaggio per determinare come elaborare il carattere. Il codice carattere si trova nel parametro *wParam del* messaggio.

Nell'esempio seguente viene illustrato il framework di routine della finestra utilizzato da un'applicazione tipica per ricevere ed elaborare messaggi di tipo carattere.


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a>Uso del caret

Una finestra che riceve l'input da tastiera visualizza in genere i caratteri tipi dall'utente nell'area client della finestra. Una finestra deve usare un cursore per indicare la posizione nell'area client in cui verrà visualizzato il carattere successivo. La finestra deve anche creare e visualizzare il punto di interesse quando riceve lo stato attivo della tastiera e nascondere ed eliminare il punto di interesse quando perde lo stato attivo. Una finestra può eseguire queste operazioni nell'elaborazione dei [**messaggi WM \_ SETFOCUS**](wm-setfocus.md) e [**WM \_ KILLFOCUS.**](wm-killfocus.md) Per altre informazioni sui caret, vedere [Carets](/windows/desktop/menurc/carets).

## <a name="displaying-keyboard-input"></a>Visualizzazione dell'input da tastiera

L'esempio in questa sezione illustra come un'applicazione può ricevere caratteri dalla tastiera, visualizzarli nell'area client di una finestra e aggiornare la posizione del cursore con ogni carattere digitato. Viene inoltre illustrato come spostare il cursore in risposta alle sequenze di tasti FRECCIA SINISTRA, FRECCIA DESTRA, HOME ed FINE e viene illustrato come evidenziare il testo selezionato in risposta alla combinazione di tasti MAIUSC+FRECCIA DESTRA.

Durante l'elaborazione [**del messaggio WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) la procedura della finestra illustrata nell'esempio alloca un buffer di 64.000 per l'archiviazione dell'input da tastiera. Recupera anche le metriche del tipo di carattere attualmente caricato, salvando l'altezza e la larghezza media dei caratteri nel tipo di carattere. L'altezza e la larghezza vengono usate nell'elaborazione del messaggio [**WM \_ SIZE**](/windows/desktop/winmsg/wm-size) per calcolare la lunghezza della riga e il numero massimo di righe, in base alle dimensioni dell'area client.

La routine della finestra crea e visualizza il caret durante l'elaborazione [**del messaggio WM \_ SETFOCUS.**](wm-setfocus.md) Nasconde ed elimina il caret durante l'elaborazione del [**messaggio \_ KILLFOCUS WM.**](wm-killfocus.md)

Quando si elabora [**il messaggio WM \_ CHAR,**](wm-char.md) la routine della finestra visualizza i caratteri, li archivia nel buffer di input e aggiorna la posizione del cursore. La routine della finestra converte anche i caratteri di tabulazione in quattro spazi consecutivi. I caratteri backspace, linefeed e escape generano un segnale acustico, ma non vengono elaborati in altro modo.

La routine della finestra esegue i movimenti del punto di controllo sinistro, destro, finale e iniziale durante l'elaborazione del [**messaggio WM \_ KEYDOWN.**](wm-keydown.md) Durante l'elaborazione dell'azione del tasto FRECCIA DESTRA, la routine della finestra controlla lo stato del tasto MAIUSC e, se è in giù, seleziona il carattere a destra del cursore mentre il cursore viene spostato.

Si noti che il codice seguente viene scritto in modo che possa essere compilato come Unicode o COME ANSI. Se il codice sorgente definisce UNICODE, le stringhe vengono gestite come caratteri Unicode. In caso contrario, vengono gestiti come caratteri ANSI.


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 