---
title: Supporto legacy per la panoramica con barre di scorrimento
description: Questa sezione descrive il supporto per la panoramica tramite barre di scorrimento nelle Windows basate su applicazioni basate su .
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Tocco, supporto legacy
- panoramica con barre di scorrimento
- Windows Tocco, panoramica con barre di scorrimento
- Windows Tocco, barre di scorrimento
- barre di scorrimento, panoramica
- barre di scorrimento, supporto legacy
- Windows Tocco, movimenti
- movimenti, panoramica con barre di scorrimento
- Windows Tocco, gesti rapidi
- gesti rapidi, panoramica con barre di scorrimento
- gesti rapidi, disabilitazione
- Windows Tocco, messaggi con rotellina del mouse
- messaggi relativi alla rotellina del mouse
- Windows Tocco, personalizzazione della panoramica
- panoramica, barre di scorrimento
- panoramica, supporto legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97190d637cae5cc6936ecd78dca31e1e6c0f9ef1037b292b6080f973fc4e8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086321"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a>Supporto legacy per la panoramica con barre di scorrimento

Questa sezione descrive il supporto per la panoramica tramite barre di scorrimento nelle Windows basate su applicazioni basate su .

In Windows 7 i movimenti di panoramica generano messaggi WM SCROLL per abilitare il supporto legacy per \_ \* la panoramica. Poiché le applicazioni potrebbero non supportare tutti i messaggi WM \_ \* SCROLL, la panoramica potrebbe non funzionare correttamente. Questo argomento descrive i passaggi da eseguire per garantire che l'esperienza di panoramica legacy nelle applicazioni funzioni come previsto dagli utenti.

## <a name="overview"></a>Panoramica

Le sezioni seguenti illustrano come abilitare l'esperienza di panoramica legacy:

-   Creare un'applicazione con barre di scorrimento.
-   Disabilitare i gesti rapidi.
-   Personalizzare l'esperienza di panoramica.

## <a name="create-an-application-with-scroll-bars"></a>Creare un'applicazione con barre di scorrimento

Avviare un nuovo progetto Win32 usando la Microsoft Visual Studio guidata. Assicurarsi che il tipo di applicazione sia impostato sull'Windows applicazione. Non è necessario abilitare il supporto per Active Template Library (ATL). L'immagine seguente mostra l'aspetto del progetto dopo l'avvio.

![Screenshot che mostra una finestra senza barre di scorrimento](images/gpd-1.png)

Abilitare quindi le barre di scorrimento nell'immagine. Modificare il codice di creazione della finestra in **InitInstance** in modo che la chiamata alla funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) crei una finestra con barre di scorrimento. A tal fine, osservare il codice indicato di seguito.


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



Dopo aver modificato il codice di creazione della finestra, l'applicazione avrà una barra di scorrimento. L'immagine seguente illustra l'aspetto dell'applicazione a questo punto.

![Screenshot che mostra una finestra con una barra di scorrimento verticale ma senza testo](images/gpd-2.png)

Dopo aver modificato il codice di creazione della finestra, aggiungere un oggetto barra di scorrimento all'applicazione e del testo da scorrere. Inserire il codice seguente all'inizio del **metodo WndProc.**


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



Implementare quindi la logica dell'applicazione per configurare i calcoli del testo per le metriche del testo. Il codice seguente deve sostituire il case **WM \_ CREATE** esistente nella **funzione WndProc.**


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



Implementare quindi la logica dell'applicazione per il ricalcolo del blocco di testo quando la finestra viene ridimensionata. Il codice seguente deve essere inserito nell'opzione message in **WndProc**.


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



Implementare quindi la logica dell'applicazione per i messaggi di scorrimento verticale. Il codice seguente deve essere inserito nell'opzione message in **WndProc**.


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



Aggiornare quindi il codice per ridisegnare la finestra. Il codice seguente deve sostituire il case **WM \_ PAINT** predefinito in **WndProc.**


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



A questo punto, quando si compila ed esegue l'applicazione, l'applicazione deve contenere il testo boilerplate e una barra di scorrimento verticale. L'immagine seguente mostra l'aspetto dell'applicazione.

![Screenshot che mostra una finestra con una barra di scorrimento verticale e testo](images/gpd-3.png)

## <a name="disable-flicks"></a>Disabilita gesti rapidi

Per migliorare l'esperienza di panoramica nell'applicazione, è consigliabile disattivare i gesti rapidi. A tale scopo, impostare le proprietà della finestra sul valore *hWnd* quando viene inizializzato. I valori usati per i gesti rapidi vengono archiviati nell'intestazione tpcshrd.h, che deve anche essere inclusa. Il codice seguente deve essere inserito nelle direttive include e nella **funzione InitInstance** dopo aver creato *hWnd*.

> [!Note]  
> Ciò è utile per le applicazioni che richiedono un feedback immediato su un evento tocco o penna giù invece di eseguire il test per una soglia di tempo o distanza.

 


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

Potrebbe essere necessario un'esperienza di panoramica diversa rispetto Windows 7 offerte per impostazione predefinita. Per migliorare l'esperienza di panoramica, è necessario aggiungere il gestore per il [**messaggio WM \_ GESTURE.**](wm-gesture.md) Per altre informazioni, vedere [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Movimenti tocco](guide-multi-touch-gestures.md)
</dt> </dl>

 

 