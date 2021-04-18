---
title: Uso dell'input da tastiera
description: In questa sezione vengono illustrate le attività associate all'input da tastiera.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- input dell'utente, input da tastiera
- acquisizione dell'input dell'utente, input da tastiera
- input da tastiera
- messaggi di tasti
- messaggi di tipo carattere
- carenze, input da tastiera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76b3f90a626506430b91e7539069c6ecdf634c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299726"
---
# <a name="using-keyboard-input"></a><span data-ttu-id="e10d9-109">Uso dell'input da tastiera</span><span class="sxs-lookup"><span data-stu-id="e10d9-109">Using Keyboard Input</span></span>

<span data-ttu-id="e10d9-110">Una finestra riceve l'input da tastiera sotto forma di messaggi di sequenza di tasti e messaggi di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="e10d9-110">A window receives keyboard input in the form of keystroke messages and character messages.</span></span> <span data-ttu-id="e10d9-111">Il ciclo di messaggi collegato alla finestra deve includere il codice per convertire i messaggi di sequenza di tasti nei messaggi di caratteri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="e10d9-111">The message loop attached to the window must include code to translate keystroke messages into the corresponding character messages.</span></span> <span data-ttu-id="e10d9-112">Se nella finestra viene visualizzato l'input da tastiera nell'area client, è necessario creare e visualizzare un accento circonflesso per indicare la posizione in cui verrà immesso il carattere successivo.</span><span class="sxs-lookup"><span data-stu-id="e10d9-112">If the window displays keyboard input in its client area, it should create and display a caret to indicate the position where the next character will be entered.</span></span> <span data-ttu-id="e10d9-113">Le sezioni seguenti descrivono il codice richiesto per la ricezione, l'elaborazione e la visualizzazione dell'input da tastiera:</span><span class="sxs-lookup"><span data-stu-id="e10d9-113">The following sections describe the code involved in receiving, processing, and displaying keyboard input:</span></span>

-   [<span data-ttu-id="e10d9-114">Elaborazione dei messaggi di sequenza di tasti</span><span class="sxs-lookup"><span data-stu-id="e10d9-114">Processing Keystroke Messages</span></span>](#processing-keystroke-messages)
-   [<span data-ttu-id="e10d9-115">Conversione di messaggi di tipo carattere</span><span class="sxs-lookup"><span data-stu-id="e10d9-115">Translating Character Messages</span></span>](#translating-character-messages)
-   [<span data-ttu-id="e10d9-116">Elaborazione di messaggi di tipo carattere</span><span class="sxs-lookup"><span data-stu-id="e10d9-116">Processing Character Messages</span></span>](#processing-character-messages)
-   [<span data-ttu-id="e10d9-117">Uso del punto di inserimento</span><span class="sxs-lookup"><span data-stu-id="e10d9-117">Using the Caret</span></span>](#using-the-caret)
-   [<span data-ttu-id="e10d9-118">Visualizzazione dell'input da tastiera</span><span class="sxs-lookup"><span data-stu-id="e10d9-118">Displaying Keyboard Input</span></span>](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a><span data-ttu-id="e10d9-119">Elaborazione dei messaggi di sequenza di tasti</span><span class="sxs-lookup"><span data-stu-id="e10d9-119">Processing Keystroke Messages</span></span>

<span data-ttu-id="e10d9-120">La routine della finestra della finestra con lo stato attivo riceve i messaggi di sequenza di tasti quando l'utente digita sulla tastiera.</span><span class="sxs-lookup"><span data-stu-id="e10d9-120">The window procedure of the window that has the keyboard focus receives keystroke messages when the user types at the keyboard.</span></span> <span data-ttu-id="e10d9-121">I messaggi di tasti sono [**WM \_ KeyDown**](wm-keydown.md), [**WM \_ KEYUP**](wm-keyup.md), [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)e [**WM \_ SYSKEYUP**](wm-syskeyup.md).</span><span class="sxs-lookup"><span data-stu-id="e10d9-121">The keystroke messages are [**WM\_KEYDOWN**](wm-keydown.md), [**WM\_KEYUP**](wm-keyup.md), [**WM\_SYSKEYDOWN**](wm-syskeydown.md), and [**WM\_SYSKEYUP**](wm-syskeyup.md).</span></span> <span data-ttu-id="e10d9-122">Una routine di finestra tipica ignora tutti i messaggi di sequenza di tasti eccetto **WM \_ KeyDown**.</span><span class="sxs-lookup"><span data-stu-id="e10d9-122">A typical window procedure ignores all keystroke messages except **WM\_KEYDOWN**.</span></span> <span data-ttu-id="e10d9-123">Il sistema invia il messaggio di **WM \_ KeyDown** quando l'utente preme un tasto.</span><span class="sxs-lookup"><span data-stu-id="e10d9-123">The system posts the **WM\_KEYDOWN** message when the user presses a key.</span></span>

<span data-ttu-id="e10d9-124">Quando la routine della finestra riceve il messaggio di [**WM \_ KeyDown**](wm-keydown.md) , deve esaminare il codice della chiave virtuale che accompagna il messaggio per determinare come elaborare la sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="e10d9-124">When the window procedure receives the [**WM\_KEYDOWN**](wm-keydown.md) message, it should examine the virtual-key code that accompanies the message to determine how to process the keystroke.</span></span> <span data-ttu-id="e10d9-125">Il codice della chiave virtuale si trova nel parametro *wParam* del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e10d9-125">The virtual-key code is in the message's *wParam* parameter.</span></span> <span data-ttu-id="e10d9-126">In genere, un'applicazione elabora solo le sequenze di tasti generate da chiavi non di tipo carattere, inclusi i tasti funzione, i tasti di spostamento del cursore e i tasti per scopi specifici, ad esempio INS, CANC, HOME e END.</span><span class="sxs-lookup"><span data-stu-id="e10d9-126">Typically, an application processes only keystrokes generated by noncharacter keys, including the function keys, the cursor movement keys, and the special purpose keys such as INS, DEL, HOME, and END.</span></span>

<span data-ttu-id="e10d9-127">Nell'esempio seguente viene illustrato il Framework di routine della finestra utilizzato da una tipica applicazione per ricevere ed elaborare i messaggi di sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="e10d9-127">The following example shows the window procedure framework that a typical application uses to receive and process keystroke messages.</span></span>


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



## <a name="translating-character-messages"></a><span data-ttu-id="e10d9-128">Conversione di messaggi di tipo carattere</span><span class="sxs-lookup"><span data-stu-id="e10d9-128">Translating Character Messages</span></span>

<span data-ttu-id="e10d9-129">Qualsiasi thread che riceve input di caratteri dall'utente deve includere la funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) nel ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="e10d9-129">Any thread that receives character input from the user must include the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function in its message loop.</span></span> <span data-ttu-id="e10d9-130">Questa funzione esamina il codice della chiave virtuale di un messaggio di sequenza di tasti e, se il codice corrisponde a un carattere, inserisce un messaggio di tipo carattere nella coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="e10d9-130">This function examines the virtual-key code of a keystroke message and, if the code corresponds to a character, places a character message into the message queue.</span></span> <span data-ttu-id="e10d9-131">Il messaggio del carattere viene rimosso e inviato alla successiva iterazione del ciclo di messaggi; il parametro *wParam* del messaggio contiene il codice carattere.</span><span class="sxs-lookup"><span data-stu-id="e10d9-131">The character message is removed and dispatched on the next iteration of the message loop; the *wParam* parameter of the message contains the character code.</span></span>

<span data-ttu-id="e10d9-132">In generale, il ciclo di messaggi di un thread deve utilizzare la funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) per tradurre ogni messaggio, non solo i messaggi della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="e10d9-132">In general, a thread's message loop should use the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function to translate every message, not just virtual-key messages.</span></span> <span data-ttu-id="e10d9-133">Sebbene **TranslateMessage** non abbia alcun effetto su altri tipi di messaggi, garantisce che l'input da tastiera venga convertito correttamente.</span><span class="sxs-lookup"><span data-stu-id="e10d9-133">Although **TranslateMessage** has no effect on other types of messages, it guarantees that keyboard input is translated correctly.</span></span> <span data-ttu-id="e10d9-134">Nell'esempio seguente viene illustrato come includere la funzione **TranslateMessage** in un normale ciclo di messaggi del thread.</span><span class="sxs-lookup"><span data-stu-id="e10d9-134">The following example shows how to include the **TranslateMessage** function in a typical thread message loop.</span></span>


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



## <a name="processing-character-messages"></a><span data-ttu-id="e10d9-135">Elaborazione di messaggi di tipo carattere</span><span class="sxs-lookup"><span data-stu-id="e10d9-135">Processing Character Messages</span></span>

<span data-ttu-id="e10d9-136">Una routine della finestra riceve un messaggio di carattere quando la funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) converte un codice di chiave virtuale corrispondente a un tasto carattere.</span><span class="sxs-lookup"><span data-stu-id="e10d9-136">A window procedure receives a character message when the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function translates a virtual-key code corresponding to a character key.</span></span> <span data-ttu-id="e10d9-137">I messaggi di tipo carattere sono [**WM \_ char**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)e [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md).</span><span class="sxs-lookup"><span data-stu-id="e10d9-137">The character messages are [**WM\_CHAR**](wm-char.md), [**WM\_DEADCHAR**](wm-deadchar.md), [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar), and [**WM\_SYSDEADCHAR**](wm-sysdeadchar.md).</span></span> <span data-ttu-id="e10d9-138">Una routine di finestra tipica ignora tutti i messaggi di tipo carattere eccetto **WM \_ char**.</span><span class="sxs-lookup"><span data-stu-id="e10d9-138">A typical window procedure ignores all character messages except **WM\_CHAR**.</span></span> <span data-ttu-id="e10d9-139">La funzione **TranslateMessage** genera un messaggio **WM \_ char** quando l'utente preme una delle chiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e10d9-139">The **TranslateMessage** function generates a **WM\_CHAR** message when the user presses any of the following keys:</span></span>

-   <span data-ttu-id="e10d9-140">Qualsiasi tasto carattere</span><span class="sxs-lookup"><span data-stu-id="e10d9-140">Any character key</span></span>
-   <span data-ttu-id="e10d9-141">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="e10d9-141">BACKSPACE</span></span>
-   <span data-ttu-id="e10d9-142">ENTER (ritorno a capo)</span><span class="sxs-lookup"><span data-stu-id="e10d9-142">ENTER (carriage return)</span></span>
-   <span data-ttu-id="e10d9-143">ESC</span><span class="sxs-lookup"><span data-stu-id="e10d9-143">ESC</span></span>
-   <span data-ttu-id="e10d9-144">MAIUSC + INVIO (avanzamento riga)</span><span class="sxs-lookup"><span data-stu-id="e10d9-144">SHIFT+ENTER (linefeed)</span></span>
-   <span data-ttu-id="e10d9-145">TAB</span><span class="sxs-lookup"><span data-stu-id="e10d9-145">TAB</span></span>

<span data-ttu-id="e10d9-146">Quando una routine della finestra riceve il messaggio [**WM \_ char**](wm-char.md) , deve esaminare il codice carattere che accompagna il messaggio per determinare come elaborare il carattere.</span><span class="sxs-lookup"><span data-stu-id="e10d9-146">When a window procedure receives the [**WM\_CHAR**](wm-char.md) message, it should examine the character code that accompanies the message to determine how to process the character.</span></span> <span data-ttu-id="e10d9-147">Il codice carattere si trova nel parametro *wParam* del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e10d9-147">The character code is in the message's *wParam* parameter.</span></span>

<span data-ttu-id="e10d9-148">Nell'esempio seguente viene illustrato il Framework di routine della finestra utilizzato da una tipica applicazione per ricevere ed elaborare i messaggi di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="e10d9-148">The following example shows the window procedure framework that a typical application uses to receive and process character messages.</span></span>


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



## <a name="using-the-caret"></a><span data-ttu-id="e10d9-149">Uso del punto di inserimento</span><span class="sxs-lookup"><span data-stu-id="e10d9-149">Using the Caret</span></span>

<span data-ttu-id="e10d9-150">Una finestra che riceve l'input da tastiera Visualizza in genere i caratteri che l'utente digita nell'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="e10d9-150">A window that receives keyboard input typically displays the characters the user types in the window's client area.</span></span> <span data-ttu-id="e10d9-151">Una finestra deve usare un accento circonflesso per indicare la posizione nell'area client in cui verrà visualizzato il carattere successivo.</span><span class="sxs-lookup"><span data-stu-id="e10d9-151">A window should use a caret to indicate the position in the client area where the next character will appear.</span></span> <span data-ttu-id="e10d9-152">La finestra deve anche creare e visualizzare il cursore quando riceve lo stato attivo della tastiera e nascondere ed eliminare il cursore quando perde lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="e10d9-152">The window should also create and display the caret when it receives the keyboard focus, and hide and destroy the caret when it loses the focus.</span></span> <span data-ttu-id="e10d9-153">Una finestra può eseguire queste operazioni nell'elaborazione dei messaggi WM [**\_ SetFocus**](wm-setfocus.md) e [**WM \_ KILLFOCUS**](wm-killfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="e10d9-153">A window can perform these operations in the processing of the [**WM\_SETFOCUS**](wm-setfocus.md) and [**WM\_KILLFOCUS**](wm-killfocus.md) messages.</span></span> <span data-ttu-id="e10d9-154">Per ulteriori informazioni sui Carrier, vedere la pagina relativa ai [Carrier](/windows/desktop/menurc/carets).</span><span class="sxs-lookup"><span data-stu-id="e10d9-154">For more information about carets, see [Carets](/windows/desktop/menurc/carets).</span></span>

## <a name="displaying-keyboard-input"></a><span data-ttu-id="e10d9-155">Visualizzazione dell'input da tastiera</span><span class="sxs-lookup"><span data-stu-id="e10d9-155">Displaying Keyboard Input</span></span>

<span data-ttu-id="e10d9-156">Nell'esempio riportato in questa sezione viene illustrato il modo in cui un'applicazione può ricevere i caratteri dalla tastiera, visualizzarli nell'area client di una finestra e aggiornare la posizione del punto di inserimento con ogni carattere digitato.</span><span class="sxs-lookup"><span data-stu-id="e10d9-156">The example in this section shows how an application can receive characters from the keyboard, display them in the client area of a window, and update the position of the caret with each character typed.</span></span> <span data-ttu-id="e10d9-157">Viene inoltre illustrato come spostare il punto di inserimento in risposta alle sequenze di tasti freccia sinistra, freccia destra, HOME e fine e viene illustrato come evidenziare il testo selezionato in risposta alla combinazione di tasti MAIUSC + freccia destra.</span><span class="sxs-lookup"><span data-stu-id="e10d9-157">It also demonstrates how to move the caret in response to the LEFT ARROW, RIGHT ARROW, HOME, and END keystrokes, and shows how to highlight selected text in response to the SHIFT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="e10d9-158">Durante l'elaborazione del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) , la procedura della finestra illustrata nell'esempio alloca un buffer 64K per l'archiviazione dell'input da tastiera.</span><span class="sxs-lookup"><span data-stu-id="e10d9-158">During processing of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure shown in the example allocates a 64K buffer for storing keyboard input.</span></span> <span data-ttu-id="e10d9-159">Recupera anche le metriche del tipo di carattere attualmente caricato, salvando l'altezza e la larghezza media dei caratteri nel tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e10d9-159">It also retrieves the metrics of the currently loaded font, saving the height and average width of characters in the font.</span></span> <span data-ttu-id="e10d9-160">L'altezza e la larghezza vengono utilizzate nell'elaborazione del messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) per calcolare la lunghezza della riga e il numero massimo di righe, in base alle dimensioni dell'area client.</span><span class="sxs-lookup"><span data-stu-id="e10d9-160">The height and width are used in processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to calculate the line length and maximum number of lines, based on the size of the client area.</span></span>

<span data-ttu-id="e10d9-161">La procedura finestra Crea e visualizza il punto di inserimento quando si elabora il messaggio di [**\_ SetFocus di WM**](wm-setfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="e10d9-161">The window procedure creates and displays the caret when processing the [**WM\_SETFOCUS**](wm-setfocus.md) message.</span></span> <span data-ttu-id="e10d9-162">Nasconde ed Elimina il punto di inserimento durante l'elaborazione del messaggio [**WM \_ KILLFOCUS**](wm-killfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="e10d9-162">It hides and deletes the caret when processing the [**WM\_KILLFOCUS**](wm-killfocus.md) message.</span></span>

<span data-ttu-id="e10d9-163">Quando si elabora il messaggio [**WM \_ char**](wm-char.md) , la routine della finestra Visualizza i caratteri, li archivia nel buffer di input e aggiorna la posizione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="e10d9-163">When processing the [**WM\_CHAR**](wm-char.md) message, the window procedure displays characters, stores them in the input buffer, and updates the caret position.</span></span> <span data-ttu-id="e10d9-164">La procedura della finestra converte anche i caratteri di tabulazione in quattro spazi consecutivi.</span><span class="sxs-lookup"><span data-stu-id="e10d9-164">The window procedure also converts tab characters to four consecutive space characters.</span></span> <span data-ttu-id="e10d9-165">I caratteri backspace, avanzamento riga e Escape generano un segnale acustico, ma non vengono elaborati in altro modo.</span><span class="sxs-lookup"><span data-stu-id="e10d9-165">Backspace, linefeed, and escape characters generate a beep, but are not otherwise processed.</span></span>

<span data-ttu-id="e10d9-166">La routine della finestra esegue i movimenti di cursore a sinistra, a destra, fine e Home durante l'elaborazione del messaggio del [**\_ KeyDown di WM**](wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="e10d9-166">The window procedure performs the left, right, end, and home caret movements when processing the [**WM\_KEYDOWN**](wm-keydown.md) message.</span></span> <span data-ttu-id="e10d9-167">Durante l'elaborazione dell'azione del tasto freccia destra, la routine della finestra Controlla lo stato del tasto MAIUSC e, se è inattivo, seleziona il carattere a destra del punto di inserimento quando il punto di inserimento viene spostato.</span><span class="sxs-lookup"><span data-stu-id="e10d9-167">While processing the action of the RIGHT ARROW key, the window procedure checks the state of the SHIFT key and, if it is down, selects the character to the right of the caret as the caret is moved.</span></span>

<span data-ttu-id="e10d9-168">Si noti che il codice seguente viene scritto in modo che sia possibile compilarlo come Unicode o come ANSI.</span><span class="sxs-lookup"><span data-stu-id="e10d9-168">Note that the following code is written so that it can be compiled either as Unicode or as ANSI.</span></span> <span data-ttu-id="e10d9-169">Se il codice sorgente definisce UNICODE, le stringhe vengono gestite come caratteri Unicode; in caso contrario, vengono gestiti come caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="e10d9-169">If the source code defines UNICODE, strings are handled as Unicode characters; otherwise, they are handled as ANSI characters.</span></span>


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



 

 