---
title: Supporto legacy per la panoramica con le barre di scorrimento
description: In questa sezione viene descritto il supporto per la panoramica con le barre di scorrimento nelle applicazioni basate su Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch, supporto legacy
- Panoramica con barre di scorrimento
- Windows Touch, panoramica con barre di scorrimento
- Windows Touch, barre di scorrimento
- barre di scorrimento, panoramica
- barre di scorrimento, supporto legacy
- Windows Touch, movimenti
- movimenti, panoramica con barre di scorrimento
- Windows Touch, gesti rapidi
- gesti rapidi, panoramica con barre di scorrimento
- gesti rapidi, disabilitazione
- Windows Touch, messaggi della rotellina del mouse
- messaggi rotellina del mouse
- Windows Touch, personalizzazione della panoramica
- Panoramica, barre di scorrimento
- Panoramica, supporto legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104562624"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a><span data-ttu-id="d6b98-119">Supporto legacy per la panoramica con le barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="d6b98-119">Legacy Support for Panning with Scroll Bars</span></span>

<span data-ttu-id="d6b98-120">In questa sezione viene descritto il supporto per la panoramica con le barre di scorrimento nelle applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="d6b98-120">This section describes support for panning using scroll bars in Windows-based applications.</span></span>

<span data-ttu-id="d6b98-121">In Windows 7 i movimenti di panning generano \_ \* messaggi di scorrimento WM per abilitare il supporto legacy per la panoramica.</span><span class="sxs-lookup"><span data-stu-id="d6b98-121">In Windows 7, panning gestures generate WM\_\*SCROLL messages to enable legacy support for panning.</span></span> <span data-ttu-id="d6b98-122">Poiché è possibile che le applicazioni non supportino tutti i \_ \* messaggi di scorrimento WM, il panning potrebbe non funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="d6b98-122">Because your applications may not support all of the WM\_\*SCROLL messages, panning may not work correctly.</span></span> <span data-ttu-id="d6b98-123">In questo argomento vengono descritti i passaggi da eseguire per assicurarsi che l'esperienza di panoramica legacy nelle applicazioni funzioni come previsto dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="d6b98-123">This topic describes the steps you must take to ensure that the legacy panning experience in applications functions as users expect.</span></span>

## <a name="overview"></a><span data-ttu-id="d6b98-124">Panoramica</span><span class="sxs-lookup"><span data-stu-id="d6b98-124">Overview</span></span>

<span data-ttu-id="d6b98-125">Le sezioni seguenti illustrano come abilitare l'esperienza di panoramica legacy:</span><span class="sxs-lookup"><span data-stu-id="d6b98-125">The following sections explain how to enable the legacy panning experience:</span></span>

-   <span data-ttu-id="d6b98-126">Creare un'applicazione con barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d6b98-126">Create an application with scroll bars.</span></span>
-   <span data-ttu-id="d6b98-127">Disabilitare i gesti rapidi.</span><span class="sxs-lookup"><span data-stu-id="d6b98-127">Disable flicks.</span></span>
-   <span data-ttu-id="d6b98-128">Personalizzare l'esperienza di panoramica.</span><span class="sxs-lookup"><span data-stu-id="d6b98-128">Customize the panning experience.</span></span>

## <a name="create-an-application-with-scroll-bars"></a><span data-ttu-id="d6b98-129">Creare un'applicazione con barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="d6b98-129">Create an Application with Scroll Bars</span></span>

<span data-ttu-id="d6b98-130">Avviare un nuovo progetto Win32 utilizzando la procedura guidata Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d6b98-130">Start a new Win32 project using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="d6b98-131">Verificare che il tipo di applicazione sia impostato sull'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="d6b98-131">Make sure the application type is set to the Windows application.</span></span> <span data-ttu-id="d6b98-132">Non è necessario abilitare il supporto per il Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="d6b98-132">You don't need to enable support for the Active Template Library (ATL).</span></span> <span data-ttu-id="d6b98-133">La figura seguente mostra l'aspetto del progetto dopo l'avvio.</span><span class="sxs-lookup"><span data-stu-id="d6b98-133">The following image shows what your project will look like after you have started it.</span></span>

![screenshot che mostra una finestra senza barre di scorrimento](images/gpd-1.png)

<span data-ttu-id="d6b98-135">Abilitare quindi le barre di scorrimento nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="d6b98-135">Next, enable scroll bars on the image.</span></span> <span data-ttu-id="d6b98-136">Modificare il codice di creazione della finestra in **InitInstance** in modo che la chiamata di funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) crei una finestra con barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d6b98-136">Change the window creation code in **InitInstance** so that the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function call creates a window with scroll bars.</span></span> <span data-ttu-id="d6b98-137">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d6b98-137">The following code shows how to do this.</span></span>


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



<span data-ttu-id="d6b98-138">Dopo aver modificato il codice di creazione della finestra, l'applicazione avrà una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d6b98-138">After you have changed the window creation code, your application will have a scroll bar.</span></span> <span data-ttu-id="d6b98-139">Nell'immagine seguente viene illustrato il modo in cui l'applicazione può essere esaminata in questo punto.</span><span class="sxs-lookup"><span data-stu-id="d6b98-139">The following image shows how the application might look at this point.</span></span>

![screenshot che mostra una finestra con una barra di scorrimento verticale ma senza testo](images/gpd-2.png)

<span data-ttu-id="d6b98-141">Dopo aver modificato il codice di creazione della finestra, aggiungere un oggetto barra di scorrimento all'applicazione e il testo da scorrere.</span><span class="sxs-lookup"><span data-stu-id="d6b98-141">After you have changed the window creation code, add a scroll bar object to your application and some text to scroll.</span></span> <span data-ttu-id="d6b98-142">Inserire il codice seguente nella parte superiore del metodo **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="d6b98-142">Place the following code into the top of the **WndProc** method.</span></span>


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



<span data-ttu-id="d6b98-143">Implementare quindi la logica dell'applicazione per la configurazione dei calcoli di testo per le metriche del testo.</span><span class="sxs-lookup"><span data-stu-id="d6b98-143">Next, implement the application logic for configuring the text calculations for text metrics.</span></span> <span data-ttu-id="d6b98-144">Il codice seguente deve sostituire il case **di \_ creazione di WM** esistente nella funzione **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="d6b98-144">The following code should replace the existing **WM\_CREATE** case in the **WndProc** function.</span></span>


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



<span data-ttu-id="d6b98-145">Implementare quindi la logica dell'applicazione per il ricalcolo del blocco di testo quando la finestra viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="d6b98-145">Next, implement the application logic for recalculation of the text block when the window is resized.</span></span> <span data-ttu-id="d6b98-146">Il codice seguente deve essere inserito nello switch del messaggio in **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="d6b98-146">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



<span data-ttu-id="d6b98-147">Implementare quindi la logica dell'applicazione per i messaggi di scorrimento verticali.</span><span class="sxs-lookup"><span data-stu-id="d6b98-147">Next, implement the application logic for vertical scroll messages.</span></span> <span data-ttu-id="d6b98-148">Il codice seguente deve essere inserito nello switch del messaggio in **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="d6b98-148">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



<span data-ttu-id="d6b98-149">Aggiornare quindi il codice per ricreare la finestra.</span><span class="sxs-lookup"><span data-stu-id="d6b98-149">Next, update the code to redraw the window.</span></span> <span data-ttu-id="d6b98-150">Il codice seguente deve sostituire il caso **di \_ disegno WM** predefinito in **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="d6b98-150">The following code should replace the default **WM\_PAINT** case in **WndProc**.</span></span>


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



<span data-ttu-id="d6b98-151">A questo punto, quando si compila e si esegue l'applicazione, dovrebbe essere presente il testo standard e una barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="d6b98-151">Now when you build and run your application, it should have the boilerplate text and a vertical scroll bar.</span></span> <span data-ttu-id="d6b98-152">Nell'immagine seguente viene illustrato il modo in cui l'applicazione potrebbe sembrare.</span><span class="sxs-lookup"><span data-stu-id="d6b98-152">The following image shows how your application might look.</span></span>

![screenshot che mostra una finestra con una barra di scorrimento verticale e un testo](images/gpd-3.png)

## <a name="disable-flicks"></a><span data-ttu-id="d6b98-154">Disabilitare i gesti rapidi</span><span class="sxs-lookup"><span data-stu-id="d6b98-154">Disable Flicks</span></span>

<span data-ttu-id="d6b98-155">Per migliorare l'esperienza di panoramica nell'applicazione, è necessario disattivare i gesti rapidi.</span><span class="sxs-lookup"><span data-stu-id="d6b98-155">To improve the panning experience in your application, you should turn off flicks.</span></span> <span data-ttu-id="d6b98-156">A tale scopo, impostare le proprietà della finestra sul valore *HWND* quando viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="d6b98-156">To do this, set window properties on the *hWnd* value when it is initialized.</span></span> <span data-ttu-id="d6b98-157">I valori usati per i gesti rapidi vengono archiviati nell'intestazione tpcshrd. h, che deve anche essere inclusa.</span><span class="sxs-lookup"><span data-stu-id="d6b98-157">The values used for flicks are stored in the tpcshrd.h header, which also must be included.</span></span> <span data-ttu-id="d6b98-158">Il codice seguente deve essere inserito nelle direttive include e nella funzione **InitInstance** dopo che è stato creato *HWND*.</span><span class="sxs-lookup"><span data-stu-id="d6b98-158">The following code should be placed in your include directives and in the **InitInstance** function after you have created your *hWnd*.</span></span>

> [!Note]  
> <span data-ttu-id="d6b98-159">Questa operazione è utile per le applicazioni che richiedono un feedback immediato su un evento Touch o Pen Down anziché eseguire il test di una soglia di tempo o di distanza.</span><span class="sxs-lookup"><span data-stu-id="d6b98-159">This is useful for applications that require immediate feedback on a touch or pen down event instead of testing for a time or distance threshold.</span></span>

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a><span data-ttu-id="d6b98-160">Personalizzare l'esperienza di panoramica</span><span class="sxs-lookup"><span data-stu-id="d6b98-160">Customize the Panning Experience</span></span>

<span data-ttu-id="d6b98-161">Per impostazione predefinita, è possibile che si desideri un'esperienza di panoramica diversa da quella offerta da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6b98-161">You might want a different panning experience than Windows 7 offers by default.</span></span> <span data-ttu-id="d6b98-162">Per migliorare l'esperienza di panoramica, è necessario aggiungere il gestore per il messaggio di [**\_ movimento WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="d6b98-162">To improve the panning experience, you must add the handler for the [**WM\_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="d6b98-163">Per ulteriori informazioni, vedere [migliorare l'esperienza di panoramica del Single-Finger](improving-the-single-finger-panning-experience.md).</span><span class="sxs-lookup"><span data-stu-id="d6b98-163">For more information, see [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6b98-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6b98-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6b98-165">Movimenti tocco di Windows</span><span class="sxs-lookup"><span data-stu-id="d6b98-165">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 