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
# <a name="legacy-support-for-panning-with-scroll-bars"></a>Supporto legacy per la panoramica con le barre di scorrimento

In questa sezione viene descritto il supporto per la panoramica con le barre di scorrimento nelle applicazioni basate su Windows.

In Windows 7 i movimenti di panning generano \_ \* messaggi di scorrimento WM per abilitare il supporto legacy per la panoramica. Poiché è possibile che le applicazioni non supportino tutti i \_ \* messaggi di scorrimento WM, il panning potrebbe non funzionare correttamente. In questo argomento vengono descritti i passaggi da eseguire per assicurarsi che l'esperienza di panoramica legacy nelle applicazioni funzioni come previsto dagli utenti.

## <a name="overview"></a>Panoramica

Le sezioni seguenti illustrano come abilitare l'esperienza di panoramica legacy:

-   Creare un'applicazione con barre di scorrimento.
-   Disabilitare i gesti rapidi.
-   Personalizzare l'esperienza di panoramica.

## <a name="create-an-application-with-scroll-bars"></a>Creare un'applicazione con barre di scorrimento

Avviare un nuovo progetto Win32 utilizzando la procedura guidata Microsoft Visual Studio. Verificare che il tipo di applicazione sia impostato sull'applicazione Windows. Non è necessario abilitare il supporto per il Active Template Library (ATL). La figura seguente mostra l'aspetto del progetto dopo l'avvio.

![screenshot che mostra una finestra senza barre di scorrimento](images/gpd-1.png)

Abilitare quindi le barre di scorrimento nell'immagine. Modificare il codice di creazione della finestra in **InitInstance** in modo che la chiamata di funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) crei una finestra con barre di scorrimento. A tal fine, osservare il codice indicato di seguito.


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



Dopo aver modificato il codice di creazione della finestra, l'applicazione avrà una barra di scorrimento. Nell'immagine seguente viene illustrato il modo in cui l'applicazione può essere esaminata in questo punto.

![screenshot che mostra una finestra con una barra di scorrimento verticale ma senza testo](images/gpd-2.png)

Dopo aver modificato il codice di creazione della finestra, aggiungere un oggetto barra di scorrimento all'applicazione e il testo da scorrere. Inserire il codice seguente nella parte superiore del metodo **WndProc** .


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



Implementare quindi la logica dell'applicazione per la configurazione dei calcoli di testo per le metriche del testo. Il codice seguente deve sostituire il case **di \_ creazione di WM** esistente nella funzione **WndProc** .


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



Implementare quindi la logica dell'applicazione per il ricalcolo del blocco di testo quando la finestra viene ridimensionata. Il codice seguente deve essere inserito nello switch del messaggio in **WndProc**.


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



Implementare quindi la logica dell'applicazione per i messaggi di scorrimento verticali. Il codice seguente deve essere inserito nello switch del messaggio in **WndProc**.


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



Aggiornare quindi il codice per ricreare la finestra. Il codice seguente deve sostituire il caso **di \_ disegno WM** predefinito in **WndProc**.


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



A questo punto, quando si compila e si esegue l'applicazione, dovrebbe essere presente il testo standard e una barra di scorrimento verticale. Nell'immagine seguente viene illustrato il modo in cui l'applicazione potrebbe sembrare.

![screenshot che mostra una finestra con una barra di scorrimento verticale e un testo](images/gpd-3.png)

## <a name="disable-flicks"></a>Disabilitare i gesti rapidi

Per migliorare l'esperienza di panoramica nell'applicazione, è necessario disattivare i gesti rapidi. A tale scopo, impostare le proprietà della finestra sul valore *HWND* quando viene inizializzato. I valori usati per i gesti rapidi vengono archiviati nell'intestazione tpcshrd. h, che deve anche essere inclusa. Il codice seguente deve essere inserito nelle direttive include e nella funzione **InitInstance** dopo che è stato creato *HWND*.

> [!Note]  
> Questa operazione è utile per le applicazioni che richiedono un feedback immediato su un evento Touch o Pen Down anziché eseguire il test di una soglia di tempo o di distanza.

 


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



## <a name="customize-the-panning-experience"></a>Personalizzare l'esperienza di panoramica

Per impostazione predefinita, è possibile che si desideri un'esperienza di panoramica diversa da quella offerta da Windows 7. Per migliorare l'esperienza di panoramica, è necessario aggiungere il gestore per il messaggio di [**\_ movimento WM**](wm-gesture.md) . Per ulteriori informazioni, vedere [migliorare l'esperienza di panoramica del Single-Finger](improving-the-single-finger-panning-experience.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Movimenti tocco di Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 