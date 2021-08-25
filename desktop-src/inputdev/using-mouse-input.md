---
title: Uso dell'input del mouse
description: Questa sezione illustra le attività associate all'input del mouse.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- input utente, input del mouse
- acquisizione dell'input dell'utente, input del mouse
- input del mouse
- cursori, input del mouse
- cursore del mouse
- elaborazione di messaggi con doppio clic
- rotellina del mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38105da1fbbe3bee1be9ca280f1f5573dbb41ba4b7b6aa2013d9c600b8ad00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829971"
---
# <a name="using-mouse-input"></a>Uso dell'input del mouse

Questa sezione illustra le attività associate all'input del mouse.

-   [Rilevamento del cursore del mouse](#tracking-the-mouse-cursor)
-   [Disegno di linee con il mouse](#drawing-lines-with-the-mouse)
-   [Elaborazione di un messaggio con doppio clic](#processing-a-double-click-message)
-   [Selezione di una riga di testo](#selecting-a-line-of-text)
-   [Uso della rotellina del mouse in un documento con oggetti incorporati](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [Recupero del numero di linee di scorrimento della rotellina del mouse](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a>Rilevamento del cursore del mouse

Le applicazioni spesso eseguono attività che comportano il rilevamento della posizione del cursore del mouse. La maggior parte delle applicazioni di disegno, ad esempio, tiene traccia della posizione del cursore del mouse durante le operazioni di disegno, consentendo all'utente di disegnare nell'area client di una finestra trascinando il mouse. Le applicazioni di elaborazione di testo rilevano anche il cursore, consentendo all'utente di selezionare una parola o un blocco di testo facendo clic e trascinando il mouse.

Il rilevamento del cursore comporta in genere l'elaborazione dei messaggi [**\_ WM LBUTTONDOWN,**](wm-lbuttondown.md) [**WM \_ MOUSEMOVE**](wm-mousemove.md)e [**WM \_ LBUTTONUP.**](wm-lbuttonup.md) Una finestra determina quando iniziare a tenere traccia del cursore controllando la posizione del cursore specificata nel *parametro lParam* del **messaggio WM \_ LBUTTONDOWN.** Ad esempio, un'applicazione di elaborazione di testo inizierebbe a tenere traccia del cursore solo se si verificava il messaggio **WM \_ LBUTTONDOWN** mentre il cursore si trovava su una riga di testo, ma non se era oltre la fine del documento.

Una finestra tiene traccia della posizione del cursore elaborando il flusso di messaggi [**WM \_ MOUSEMOVE**](wm-mousemove.md) inviati alla finestra durante lo spostamento del mouse. L'elaborazione **del \_ messaggio WM MOUSEMOVE** comporta in genere un'operazione ripetitiva di disegno o disegno nell'area client. Ad esempio, un'applicazione di disegno potrebbe ridisegnare ripetutamente una linea durante lo spostamento del mouse. Una finestra usa il [**messaggio \_ WM LBUTTONUP**](wm-lbuttonup.md) come segnale per interrompere il rilevamento del cursore.

Inoltre, un'applicazione può chiamare la [**funzione TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) per fare in modo che il sistema invii altri messaggi utili per tenere traccia del cursore. Il sistema invia il [**messaggio \_ WM MOUSEHOVER**](wm-mousehover.md) quando il cursore passa sull'area client per un determinato periodo di tempo. Invia il messaggio [**\_ WM MOUSELEAVE**](wm-mouseleave.md) quando il cursore esce dall'area client. I [**messaggi \_ WM NCMOUSEHOVER**](wm-ncmousehover.md) e [**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md) sono i messaggi corrispondenti per le aree non client.

## <a name="drawing-lines-with-the-mouse"></a>Disegno di linee con il mouse

Nell'esempio di questa sezione viene illustrato come tenere traccia del cursore del mouse. Contiene parti di una routine della finestra che consente all'utente di disegnare linee nell'area client di una finestra trascinando il mouse.

Quando la routine della finestra riceve un messaggio [**\_ WM LBUTTONDOWN,**](wm-lbuttondown.md) acquisisce il mouse e salva le coordinate del cursore, usando le coordinate come punto iniziale della riga. Usa anche la funzione [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) per limitare il cursore all'area client durante l'operazione di disegno della linea.

Durante il primo [**messaggio WM \_ MOUSEMOVE,**](wm-mousemove.md) la routine della finestra disegna una linea dal punto iniziale alla posizione corrente del cursore. Durante i **messaggi WM \_ MOUSEMOVE** successivi, la routine della finestra cancella la riga precedente disegnando su di essa un colore della penna invertito. Disegna quindi una nuova riga dal punto iniziale alla nuova posizione del cursore.

Il [**messaggio \_ WM LBUTTONUP**](wm-lbuttonup.md) segnala la fine dell'operazione di disegno. La routine della finestra rilascia il mouse capture e rilascia il mouse dall'area client.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                       // handle to device context 
    RECT rcClient;                 // client area rectangle 
    POINT ptClientUL;              // client upper left corner 
    POINT ptClientLR;              // client lower right corner 
    static POINTS ptsBegin;        // beginning point 
    static POINTS ptsEnd;          // new endpoint 
    static POINTS ptsPrevEnd;      // previous endpoint 
    static BOOL fPrevLine = FALSE; // previous line flag 
 
    switch (uMsg) 
    { 
       case WM_LBUTTONDOWN: 
 
            // Capture mouse input. 
 
            SetCapture(hwndMain); 
 
            // Retrieve the screen coordinates of the client area, 
            // and convert them into client coordinates. 
 
            GetClientRect(hwndMain, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
 
            // Add one to the right and bottom sides, because the 
            // coordinates retrieved by GetClientRect do not 
            // include the far left and lowermost pixels. 
 
            ptClientLR.x = rcClient.right + 1; 
            ptClientLR.y = rcClient.bottom + 1; 
            ClientToScreen(hwndMain, &ptClientUL); 
            ClientToScreen(hwndMain, &ptClientLR); 
 
            // Copy the client coordinates of the client area 
            // to the rcClient structure. Confine the mouse cursor 
            // to the client area by passing the rcClient structure 
            // to the ClipCursor function. 
 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            ClipCursor(&rcClient); 
 
            // Convert the cursor coordinates into a POINTS 
            // structure, which defines the beginning point of the 
            // line drawn during a WM_MOUSEMOVE message. 
 
            ptsBegin = MAKEPOINTS(lParam); 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // When moving the mouse, the user must hold down 
            // the left mouse button to draw lines. 
 
            if (wParam & MK_LBUTTON) 
            { 
 
                // Retrieve a device context (DC) for the client area. 
 
                hdc = GetDC(hwndMain); 
 
                // The following function ensures that pixels of 
                // the previously drawn line are set to white and 
                // those of the new line are set to black. 
 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a line was drawn during an earlier WM_MOUSEMOVE 
                // message, draw over it. This erases the line by 
                // setting the color of its pixels to white. 
 
                if (fPrevLine) 
                { 
                    MoveToEx(hdc, ptsBegin.x, ptsBegin.y, 
                        (LPPOINT) NULL); 
                    LineTo(hdc, ptsPrevEnd.x, ptsPrevEnd.y); 
                } 
 
                // Convert the current cursor coordinates to a 
                // POINTS structure, and then draw a new line. 
 
                ptsEnd = MAKEPOINTS(lParam); 
                MoveToEx(hdc, ptsBegin.x, ptsBegin.y, (LPPOINT) NULL); 
                LineTo(hdc, ptsEnd.x, ptsEnd.y); 
 
                // Set the previous line flag, save the ending 
                // point of the new line, and then release the DC. 
 
                fPrevLine = TRUE; 
                ptsPrevEnd = ptsEnd; 
                ReleaseDC(hwndMain, hdc); 
            } 
            break; 
 
        case WM_LBUTTONUP: 
 
            // The user has finished drawing the line. Reset the 
            // previous line flag, release the mouse cursor, and 
            // release the mouse capture. 
 
            fPrevLine = FALSE; 
            ClipCursor(NULL); 
            ReleaseCapture(); 
            return 0; 
 
        case WM_DESTROY: 
            PostQuitMessage(0); 
            break; 
 
        // Process other messages. 
        
```



## <a name="processing-a-double-click-message"></a>Elaborazione di un messaggio con doppio clic

Per ricevere messaggi con doppio clic, una finestra deve appartenere a una classe finestra con lo stile della classe [**\_ CS DBLCLKS.**](/windows/desktop/winmsg/about-window-classes) Questo stile viene impostato durante la registrazione della classe della finestra, come illustrato nell'esempio seguente.


```
BOOL InitApplication(HINSTANCE hInstance) 
{ 
    WNDCLASS wc; 
 
    wc.style = CS_DBLCLKS | CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hInstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_IBEAM); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName = "MainMenu"; 
    wc.lpszClassName = "MainWClass"; 
 
    return RegisterClass(&wc); 
} 
```



Un messaggio con doppio clic è sempre preceduto da un messaggio di menu a discesa. Per questo motivo, le applicazioni usano in genere un messaggio con doppio clic per estendere un'attività avviata durante un messaggio di selezione del pulsante.

## <a name="selecting-a-line-of-text"></a>Selezione di una riga di testo

L'esempio riportato in questa sezione è tratto da una semplice applicazione di elaborazione di testo. Include codice che consente all'utente di impostare la posizione del cursore facendo clic in un punto qualsiasi di una riga di testo e di selezionare (evidenziare) una riga di testo facendo doppio clic in un punto qualsiasi della riga.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                     // handle to device context 
    TEXTMETRIC tm;               // font size data 
    int i, j;                    // loop counters 
    int cCR = 0;                 // count of carriage returns 
    char ch;                     // character from input buffer 
    static int nBegLine;         // beginning of selected line 
    static int nCurrentLine = 0; // currently selected line 
    static int nLastLine = 0;    // last text line 
    static int nCaretPosX = 0;   // x-coordinate of caret 
    static int cch = 0;          // number of characters entered 
    static int nCharWidth = 0;   // exact width of a character 
    static char szHilite[128];   // text string to highlight 
    static DWORD dwCharX;        // average width of characters 
    static DWORD dwLineHeight;   // line height 
    static POINTS ptsCursor;     // coordinates of mouse cursor 
    static COLORREF crPrevText;  // previous text color 
    static COLORREF crPrevBk;    // previous background color 
    static PTCHAR pchInputBuf;   // pointer to input buffer 
    static BOOL fTextSelected = FALSE; // text-selection flag 
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
            dwLineHeight = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep( (UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return, and position the 
                    // caret at the beginning of the new line. 
 
                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCurrentLine += 1; 
                    break; 
 
                default:    / displayable character 
 
                    ch = (char) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width, and display the 
                    // character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, 
                        nCurrentLine * dwLineHeight, &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer. 
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the new position exceeds the maximum, 
                    // insert a carriage return and reposition the 
                    // caret at the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwMaxCharX) 
                    { 
                        nCaretPosX = 0; 
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCurrentLine; 
                    } 
 
                    ShowCaret(hwndMain); 
 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            nLastLine = max(nLastLine, nCurrentLine); 
            break; 
 
        // Process other messages. 
 
        case WM_LBUTTONDOWN: 
 
            // If a line of text is currently highlighted, redraw 
            // the text to remove the highlighting. 
 
            if (fTextSelected) 
            { 
                hdc = GetDC(hwndMain); 
                SetTextColor(hdc, crPrevText); 
                SetBkColor(hdc, crPrevBk);
                hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
                if (FAILED(hResult))
                {
                // TODO: write error handler
                } 
                TextOut(hdc, 0, nCurrentLine * dwLineHeight, 
                    szHilite, *pcch); 
                ReleaseDC(hwndMain, hdc); 
                ShowCaret(hwndMain); 
                fTextSelected = FALSE; 
            } 
 
            // Save the current mouse-cursor coordinates. 
 
            ptsCursor = MAKEPOINTS(lParam); 
 
            // Determine which line the cursor is on, and save 
            // the line number. Do not allow line numbers greater 
            // than the number of the last line of text. The 
            // line number is later multiplied by the average height 
            // of the current font. The result is used to set the 
            // y-coordinate of the caret. 
 
            nCurrentLine = min((int)(ptsCursor.y / dwLineHeight), 
                nLastLine); 
 
            // Parse the text input buffer to find the first 
            // character in the selected line of text. Each 
            // line ends with a carriage return, so it is possible 
            // to count the carriage returns to find the selected 
            // line. 
 
            cCR = 0; 
            nBegLine = 0; 
            if (nCurrentLine != 0) 
            { 
                for (i = 0; (i < cch) && 
                        (cCR < nCurrentLine); i++) 
                { 
                    if (pchInputBuf[i] == 0x0D) 
                        ++cCR; 
                } 
                nBegLine = i; 
            } 
 
            // Starting at the beginning of the selected line, 
            // measure  the width of each character, summing the 
            // width with each character measured. Stop when the 
            // sum is greater than the x-coordinate of the cursor. 
            // The sum is used to set the x-coordinate of the caret. 
 
            hdc = GetDC(hwndMain); 
            nCaretPosX = 0; 
            for (i = nBegLine; 
                (pchInputBuf[i] != 0x0D) && (i < cch); i++) 
            { 
                ch = pchInputBuf[i]; 
                GetCharWidth32(hdc, (int) ch, (int) ch, &nCharWidth); 
                if ((nCaretPosX + nCharWidth) > ptsCursor.x) break; 
                else nCaretPosX += nCharWidth; 
            } 
            ReleaseDC(hwndMain, hdc); 
 
            // Set the caret to the user-selected position. 
 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            break; 
 
        case WM_LBUTTONDBLCLK: 
 
            // Copy the selected line of text to a buffer. 
 
            for (i = nBegLine, j = 0; (pchInputBuf[i] != 0x0D) && 
                    (i < cch); i++) 
            {
                szHilite[j++] = pchInputBuf[i]; 
            }
            szHilite[j] = '\0'; 
 
            // Hide the caret, invert the background and foreground 
            // colors, and then redraw the selected line. 
 
            HideCaret(hwndMain); 
            hdc = GetDC(hwndMain); 
            crPrevText = SetTextColor(hdc, RGB(255, 255, 255)); 
            crPrevBk = SetBkColor(hdc, RGB(0, 0, 0));
            hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 0, nCurrentLine * dwLineHeight, szHilite, *pcch); 
            SetTextColor(hdc, crPrevText); 
            SetBkColor(hdc, crPrevBk); 
            ReleaseDC(hwndMain, hdc); 
 
            fTextSelected = TRUE; 
            break; 

            // Process other messages. 

        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a>Uso della rotellina del mouse in un documento con oggetti incorporati

In questo esempio si presuppone Microsoft Word documento con vari oggetti incorporati:

-   Foglio di Microsoft Excel dati
-   Controllo casella di riepilogo incorporato che scorre in risposta alla rotellina
-   Controllo casella di testo incorporato che non risponde alla rotellina

Il [messaggio MSH \_ MOUSEWHEEL](about-mouse-input.md) viene sempre inviato alla finestra principale in Microsoft Word. Questo vale anche se il foglio di calcolo incorporato è attivo. La tabella seguente illustra come viene gestito il messaggio MSH \_ MOUSEWHEEL in base all'attenzione.



| Lo stato attivo è attivo                | La gestione è la seguente                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documento di Word              | Word scorre la finestra del documento.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Foglio di calcolo Excel incorporato | Word pubblica il messaggio in Excel. È necessario decidere se l'applicazione incorporata deve rispondere o meno al messaggio.                                                                                                                                                                                                                                                                                                                                                            |
| Controllo incorporato           | L'applicazione deve inviare il messaggio a un controllo incorporato con lo stato attivo e controllare il codice restituito per verificare se il controllo lo ha gestito. Se il controllo non lo ha gestito, l'applicazione deve scorrere la finestra del documento. Ad esempio, se l'utente fa clic su una casella di riepilogo e quindi ruota la rotellina, tale controllo scorre in risposta a una rotazione della rotellina. Se l'utente ha fatto clic su una casella di testo e quindi ha ruotato la rotellina, l'intero documento scorrerebbe. |



 

Nell'esempio seguente viene illustrato come un'applicazione può gestire i messaggi a due rotelle.


```
/************************************************
* this code deals with MSH_MOUSEWHEEL
*************************************************/
#include "zmouse.h"

//
// Mouse Wheel rotation stuff, only define if we are
// on a version of the OS that does not support
// WM_MOUSEWHEEL messages.
//
#ifndef WM_MOUSEWHEEL
#define WM_MOUSEWHEEL WM_MOUSELAST+1 
    // Message ID for IntelliMouse wheel
#endif

UINT uMSH_MOUSEWHEEL = 0;   // Value returned from
                            // RegisterWindowMessage()

/**************************************************

INT WINAPI WinMain(
         HINSTANCE hInst, 
         HINSTANCE hPrevInst, 
         LPSTR lpCmdLine, 
         INT nCmdShow)
{
    MSG msg;
    BOOL bRet;

    if (!InitInstance(hInst, nCmdShow))
        return FALSE;

    //
    // The new IntelliMouse uses a Registered message to transmit
    // wheel rotation info. So register for it!
 
    uMSH_MOUSEWHEEL =
     RegisterWindowMessage(MSH_MOUSEWHEEL); 
    if ( !uMSH_MOUSEWHEEL )
    {
        MessageBox(NULL,"
                   RegisterWindowMessag Failed!",
                   "Error",MB_OK);
        return msg.wParam;
    }
    
    while (( bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            if (!TranslateAccelerator(ghwndApp,
                                      ghaccelTable,
                                      &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }

    return msg.wParam;
}

/************************************************
* this code deals with WM_MOUSEWHEEL
*************************************************/
LONG APIENTRY MainWndProc(
    HWND hwnd,
    UINT msg,
    WPARAM wParam,
    LPARAM lParam)
{
    static int nZoom = 0;
    

    switch (msg)
    {
        //
        // Handle Mouse Wheel messages generated
        // by the operating systems that have built-in
        // support for the WM_MOUSEWHEEL message.
        //

        case WM_MOUSEWHEEL:
            ((short) HIWORD(wParam)< 0) ? nZoom-- : nZoom++;

            //
            // Do other wheel stuff...
            //

            break;

        default:
            //
            // uMSH_MOUSEWHEEL is a message registered by
            // the mswheel dll on versions of Windows that
            // do not support the new message in the OS.

            if( msg == uMSH_MOUSEWHEEL )
            {
               ((int)wParam < 0) ? nZoom-- : nZoom++;

                //
                // Do other wheel stuff...
                //
                break;
            }

            return DefWindowProc(hwnd,
                                 msg,
                                 wParam,
                                 lParam);
    }

    return 0L;
}
```



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a>Recupero del numero di linee di scorrimento della rotellina del mouse

Il codice seguente consente a un'applicazione di recuperare il numero di righe di scorrimento usando la [**funzione SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)


```
#ifndef SPI_GETWHEELSCROLLLINES
#define SPI_GETWHEELSCROLLLINES   104
#endif

#include "zmouse.h"

/*********************************************************
* FUNCTION: GetNumScrollLines
* Purpose : An OS independent method to retrieve the 
*           number of wheel scroll lines
* Params  : none
* Returns : UINT:  Number of scroll lines where WHEEL_PAGESCROLL 
*           indicates to scroll a page at a time.
*********************************************************/
UINT GetNumScrollLines(void)
{
   HWND hdlMsWheel;
   UINT ucNumLines=3;  // 3 is the default
   OSVERSIONINFO osversion;
   UINT uiMsh_MsgScrollLines;
   

   memset(&osversion, 0, sizeof(osversion));
   osversion.dwOSVersionInfoSize =sizeof(osversion);
   GetVersionEx(&osversion);

   if ((osversion.dwPlatformId == VER_PLATFORM_WIN32_WINDOWS) ||
       ( (osversion.dwPlatformId == VER_PLATFORM_WIN32_NT) && 
         (osversion.dwMajorVersion < 4) )   )
   {
        hdlMsWheel = FindWindow(MSH_WHEELMODULE_CLASS, 
                                MSH_WHEELMODULE_TITLE);
        if (hdlMsWheel)
        {
           uiMsh_MsgScrollLines = RegisterWindowMessage
                                     (MSH_SCROLL_LINES);
           if (uiMsh_MsgScrollLines)
                ucNumLines = (int)SendMessage(hdlMsWheel,
                                    uiMsh_MsgScrollLines, 
                                                       0, 
                                                       0);
        }
   }
   else if ( (osversion.dwPlatformId ==
                         VER_PLATFORM_WIN32_NT) &&
             (osversion.dwMajorVersion >= 4) )
   {
      SystemParametersInfo(SPI_GETWHEELSCROLLLINES,
                                          0,
                                    &ucNumLines, 0);
   }
   return(ucNumLines);
}
```



 

 