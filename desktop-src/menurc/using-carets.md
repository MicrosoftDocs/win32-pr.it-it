---
title: Uso del punto di inserimento
description: In questa sezione vengono forniti esempi di codice che illustrano come eseguire attività correlate ai carrier.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- risorse, punto di inserimento
- carenze, creazione
- carenze, visualizzazione
- carriere, distruzione
- carenze, nascondere
- intermittenza, tempi di inattenzione
- righe lampeggianti
- blocchi lampeggianti
- bitmap intermittenti
- creazione di carriere
- visualizzazione di carriere
- nascondere i punto di inserimento
- eliminazione di carriere
- lampeggi volte
- input dell'utente, input da tastiera
- acquisizione dell'input dell'utente, input da tastiera
- input da tastiera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6450a3169588b3072d1fee271f4890a7cdeafd2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046636"
---
# <a name="using-carets"></a><span data-ttu-id="5e6ea-120">Uso del punto di inserimento</span><span class="sxs-lookup"><span data-stu-id="5e6ea-120">Using Carets</span></span>

<span data-ttu-id="5e6ea-121">Questa sezione contiene esempi di codice per le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="5e6ea-121">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="5e6ea-122">Creazione e visualizzazione di un accento circonflesso</span><span class="sxs-lookup"><span data-stu-id="5e6ea-122">Creating and Displaying a Caret</span></span>](#creating-and-displaying-a-caret)
-   [<span data-ttu-id="5e6ea-123">Nascondere un accento circonflesso</span><span class="sxs-lookup"><span data-stu-id="5e6ea-123">Hiding a Caret</span></span>](#hiding-a-caret)
-   [<span data-ttu-id="5e6ea-124">Eliminazione di un accento circonflesso</span><span class="sxs-lookup"><span data-stu-id="5e6ea-124">Destroying a Caret</span></span>](#destroying-a-caret)
-   [<span data-ttu-id="5e6ea-125">Regolazione del tempo di lampeggio</span><span class="sxs-lookup"><span data-stu-id="5e6ea-125">Adjusting the Blink Time</span></span>](#adjusting-the-blink-time)
-   [<span data-ttu-id="5e6ea-126">Elaborazione dell'input da tastiera</span><span class="sxs-lookup"><span data-stu-id="5e6ea-126">Processing Keyboard Input</span></span>](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a><span data-ttu-id="5e6ea-127">Creazione e visualizzazione di un accento circonflesso</span><span class="sxs-lookup"><span data-stu-id="5e6ea-127">Creating and Displaying a Caret</span></span>

<span data-ttu-id="5e6ea-128">Quando riceve lo stato attivo della tastiera, la finestra deve creare e visualizzare il cursore.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-128">Upon receiving the keyboard focus, the window should create and display the caret.</span></span> <span data-ttu-id="5e6ea-129">Utilizzare la funzione [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) per creare un punto di inserimento nella finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-129">Use the [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) function to create a caret in the given window.</span></span> <span data-ttu-id="5e6ea-130">È quindi possibile chiamare [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) per impostare la posizione corrente del cursore e [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) per rendere visibile il cursore.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-130">You can then call [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) to set the current position of the caret and [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) to make the caret visible.</span></span>

<span data-ttu-id="5e6ea-131">Il sistema invia il messaggio di [**\_ SetFocus di WM**](/windows/desktop/inputdev/wm-setfocus) alla finestra che riceve lo stato attivo; pertanto, un'applicazione deve creare e visualizzare il cursore durante l'elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-131">The system sends the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message to the window receiving keyboard focus; therefore, an application should create and display the caret while processing this message.</span></span>


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



<span data-ttu-id="5e6ea-132">Per creare un punto di inserimento basato su una bitmap, è necessario specificare un handle bitmap quando si usa [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span><span class="sxs-lookup"><span data-stu-id="5e6ea-132">To create a caret based on a bitmap, you must specify a bitmap handle when using [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span></span> <span data-ttu-id="5e6ea-133">È possibile usare un'applicazione grafica per creare la bitmap e un compilatore di risorse per aggiungere la bitmap alle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-133">You can use a graphics application to create the bitmap and a resource compiler to add the bitmap to your application's resources.</span></span> <span data-ttu-id="5e6ea-134">L'applicazione può quindi usare la funzione [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) per caricare l'handle bitmap.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-134">Your application can then use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap handle.</span></span> <span data-ttu-id="5e6ea-135">Ad esempio, è possibile sostituire la riga **CreateCaret** nell'esempio precedente con le righe seguenti per creare un punto di inserimento bitmap.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-135">For example, you could replace the **CreateCaret** line in the preceding example with the following lines to create a bitmap caret.</span></span>


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



<span data-ttu-id="5e6ea-136">In alternativa, è possibile usare la funzione [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) o [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) per recuperare l'handle della bitmap del cursore.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-136">Alternatively, you can use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) or [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) function to retrieve the handle of the caret bitmap.</span></span> <span data-ttu-id="5e6ea-137">Per ulteriori informazioni sulle bitmap, vedere [bitmap](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="5e6ea-137">For more information about bitmaps, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="5e6ea-138">Se l'applicazione specifica un handle bitmap, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignora i parametri width e Height.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-138">If your application specifies a bitmap handle, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignores the width and height parameters.</span></span> <span data-ttu-id="5e6ea-139">La bitmap definisce la dimensione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-139">The bitmap defines the size of the caret.</span></span>

## <a name="hiding-a-caret"></a><span data-ttu-id="5e6ea-140">Nascondere un accento circonflesso</span><span class="sxs-lookup"><span data-stu-id="5e6ea-140">Hiding a Caret</span></span>

<span data-ttu-id="5e6ea-141">Ogni volta che l'applicazione ridisegna una schermata durante l'elaborazione di un messaggio diverso da [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), deve rendere invisibile il cursore usando la funzione [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) .</span><span class="sxs-lookup"><span data-stu-id="5e6ea-141">Whenever your application redraws a screen while processing a message other than [**WM\_PAINT**](/windows/desktop/gdi/wm-paint), it must make the caret invisible by using the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function.</span></span> <span data-ttu-id="5e6ea-142">Al termine del disegno dell'applicazione, visualizzare nuovamente il punto di inserimento tramite la funzione [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) .</span><span class="sxs-lookup"><span data-stu-id="5e6ea-142">When your application is finished drawing, redisplay the caret by using the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function.</span></span> <span data-ttu-id="5e6ea-143">Se l'applicazione elabora il messaggio di **\_ disegno WM** , non è necessario nascondere e visualizzare nuovamente il cursore, perché questa funzione esegue questa operazione automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-143">If your application processes the **WM\_PAINT** message, it is not necessary to hide and redisplay the caret, because this function does this automatically.</span></span>

<span data-ttu-id="5e6ea-144">Nell'esempio di codice seguente viene illustrato come fare in modo che l'applicazione nasconda il cursore durante il disegno di un carattere sullo schermo e durante l'elaborazione del messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="5e6ea-144">The following code sample shows how to have your application hide the caret while drawing a character on the screen and while processing the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


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



<span data-ttu-id="5e6ea-145">Se l'applicazione chiama la funzione [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) più volte senza chiamare [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), il cursore non verrà visualizzato fino a quando l'applicazione non chiamerà anche **ShowCaret** lo stesso numero di volte.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-145">If your application calls the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function several times without calling [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), the caret will not be displayed until the application also calls **ShowCaret** the same number of times.</span></span>

## <a name="destroying-a-caret"></a><span data-ttu-id="5e6ea-146">Eliminazione di un accento circonflesso</span><span class="sxs-lookup"><span data-stu-id="5e6ea-146">Destroying a Caret</span></span>

<span data-ttu-id="5e6ea-147">Quando una finestra perde lo stato attivo della tastiera, il sistema invia il messaggio [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-147">When a window loses the keyboard focus, the system sends the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message to the window.</span></span> <span data-ttu-id="5e6ea-148">L'applicazione deve eliminare il cursore durante l'elaborazione del messaggio usando la funzione [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) .</span><span class="sxs-lookup"><span data-stu-id="5e6ea-148">Your application should destroy the caret while processing this message by using the [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) function.</span></span> <span data-ttu-id="5e6ea-149">Il codice seguente illustra come eliminare un accento circonflesso in una finestra che non ha più lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-149">The following code shows how to destroy a caret in a window that no longer has the keyboard focus.</span></span>


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a><span data-ttu-id="5e6ea-150">Regolazione del tempo di lampeggio</span><span class="sxs-lookup"><span data-stu-id="5e6ea-150">Adjusting the Blink Time</span></span>

<span data-ttu-id="5e6ea-151">Nelle finestre a 16 bit, un'applicazione basata su Windows può chiamare la funzione [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) per salvare l'ora di indicizzazione corrente, quindi chiamare la funzione [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) per modificare il tempo di lampeggio durante la relativa elaborazione del messaggio [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="5e6ea-151">In 16-bit Windows, a Windows-based application could call the [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) function to save the current blink time, then call the [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function to adjust the blink time during its processing of the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="5e6ea-152">L'applicazione ripristinerà il tempo di lampeggio salvato per l'uso di altre applicazioni chiamando **SetCaretBlinkTime** durante la relativa elaborazione del messaggio [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="5e6ea-152">The application would restore the saved blink time for the use of other applications by calling **SetCaretBlinkTime** during its processing of the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="5e6ea-153">Tuttavia, questa tecnica non funziona in ambienti multithread.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-153">However, this technique does not work in multithreaded environments.</span></span> <span data-ttu-id="5e6ea-154">In particolare, la disattivazione di un'applicazione non viene sincronizzata con l'attivazione di un'altra applicazione, in modo che se un'applicazione si blocca, è ancora possibile attivare un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-154">Specifically, the deactivation of one application is not synchronized with the activation of another application, so that if one application hangs, another application can still be activated.</span></span>

<span data-ttu-id="5e6ea-155">Le applicazioni devono rispettare il tempo di lampeggio scelto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-155">Applications should respect the blink time chosen by the user.</span></span> <span data-ttu-id="5e6ea-156">La funzione [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) deve essere chiamata solo da un'applicazione che consente all'utente di impostare il tempo di lampeggio.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-156">The [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function should only be called by an application that allows the user to set the blink time.</span></span>

## <a name="processing-keyboard-input"></a><span data-ttu-id="5e6ea-157">Elaborazione dell'input da tastiera</span><span class="sxs-lookup"><span data-stu-id="5e6ea-157">Processing Keyboard Input</span></span>

<span data-ttu-id="5e6ea-158">Nell'esempio seguente viene illustrato come utilizzare un cursore in un semplice editor di testo.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-158">The following example demonstrates how to use a caret in a simple text editor.</span></span> <span data-ttu-id="5e6ea-159">L'esempio aggiorna la posizione del punto di inserimento quando l'utente digita caratteri stampabili e usa varie chiavi per spostarsi nell'area client.</span><span class="sxs-lookup"><span data-stu-id="5e6ea-159">The example updates the caret position as the user types printable characters and uses various keys to move through the client area.</span></span>


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



 

 