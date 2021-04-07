---
title: Come scorrere il testo
description: In questa sezione vengono descritte le modifiche che è possibile apportare alla routine della finestra principale di un'applicazione per consentire a un utente di scorrere il testo.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ef9a2eea9490beac7b6ff5048b70de61eb635f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872974"
---
# <a name="how-to-scroll-text"></a><span data-ttu-id="4fcdd-103">Come scorrere il testo</span><span class="sxs-lookup"><span data-stu-id="4fcdd-103">How to Scroll Text</span></span>

<span data-ttu-id="4fcdd-104">In questa sezione vengono descritte le modifiche che è possibile apportare alla routine della finestra principale di un'applicazione per consentire a un utente di scorrere il testo.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-104">This section describes the changes you can make to an application's main window procedure to enable a user to scroll text.</span></span> <span data-ttu-id="4fcdd-105">L'esempio in questa sezione Crea e visualizza una matrice di stringhe di testo ed elabora i messaggi della barra di scorrimento [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) in modo che l'utente possa scorrere il testo in senso verticale e orizzontale.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-105">The example in this section creates and displays an array of text strings, and processes [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) scroll bar messages so that the user can scroll text both vertically and horizontally.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4fcdd-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="4fcdd-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4fcdd-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="4fcdd-107">Technologies</span></span>

-   [<span data-ttu-id="4fcdd-108">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="4fcdd-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4fcdd-109">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4fcdd-109">Prerequisites</span></span>

-   <span data-ttu-id="4fcdd-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="4fcdd-110">C/C++</span></span>
-   <span data-ttu-id="4fcdd-111">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="4fcdd-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4fcdd-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4fcdd-112">Instructions</span></span>

### <a name="processing-the-wm_create-message"></a><span data-ttu-id="4fcdd-113">Elaborazione del \_ messaggio di creazione WM</span><span class="sxs-lookup"><span data-stu-id="4fcdd-113">Processing the WM\_CREATE Message</span></span>

<span data-ttu-id="4fcdd-114">Le unità di scorrimento vengono in genere impostate durante l'elaborazione del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="4fcdd-114">Scrolling units are typically set while processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="4fcdd-115">È consigliabile basare le unità di scorrimento sulle dimensioni del tipo di carattere associato al contesto di dispositivo (DC) della finestra.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-115">It is convenient to base the scrolling units on the dimensions of the font associated with the window's device context (DC).</span></span> <span data-ttu-id="4fcdd-116">Per recuperare le dimensioni del carattere per un controller di dominio specifico, usare la funzione [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) .</span><span class="sxs-lookup"><span data-stu-id="4fcdd-116">To retrieve the font dimensions for a specific DC, use the [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) function.</span></span>

<span data-ttu-id="4fcdd-117">Nell'esempio riportato in questa sezione, un'unità di scorrimento verticale equivale all'altezza di una cella di tipo carattere, più all'esterno.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-117">In the example in this section, one vertical scrolling unit is equivalent to the height of a character cell, plus external leading.</span></span> <span data-ttu-id="4fcdd-118">Un'unità di scorrimento orizzontale equivale alla larghezza media di una cella di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-118">One horizontal scrolling unit is equivalent to the average width of a character cell.</span></span> <span data-ttu-id="4fcdd-119">Le posizioni di scorrimento orizzontale, quindi, non corrispondono ai caratteri effettivi, a meno che il tipo di carattere dello schermo non sia a larghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-119">The horizontal scrolling positions, therefore, do not correspond to actual characters, unless the screen font is fixed-width.</span></span>

### <a name="processing-the-wm_size-message"></a><span data-ttu-id="4fcdd-120">Elaborazione del \_ messaggio dimensioni WM</span><span class="sxs-lookup"><span data-stu-id="4fcdd-120">Processing the WM\_SIZE Message</span></span>

<span data-ttu-id="4fcdd-121">Quando si elabora il messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) , è opportuno regolare l'intervallo di scorrimento e la posizione di scorrimento in modo da riflettere le dimensioni dell'area client, nonché il numero di righe di testo che verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-121">When processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, it is convenient to adjust the scrolling range and scrolling position to reflect the dimensions of the client area as well as the number of lines of text that will be displayed.</span></span>

<span data-ttu-id="4fcdd-122">La funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) imposta i valori di posizione minimo e massimo, le dimensioni della pagina e la posizione di scorrimento per una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-122">The [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function sets the minimum and maximum position values, the page size, and the scrolling position for a scroll bar.</span></span>

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a><span data-ttu-id="4fcdd-123">Elaborazione dei \_ messaggi WM HSCROLL e WM \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="4fcdd-123">Processing the WM\_HSCROLL and WM\_VSCROLL Messages</span></span>

<span data-ttu-id="4fcdd-124">La barra di scorrimento invia messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) alla routine della finestra ogni volta che l'utente fa clic sulla barra di scorrimento o trascina la casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-124">The scroll bar sends [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to the window procedure whenever the user clicks the scroll bar or drags the scroll box.</span></span> <span data-ttu-id="4fcdd-125">Le parole meno significative di **WM \_ VSCROLL** e **WM \_ HSCROLL** contengono ciascuno un codice di richiesta che indica la direzione e la grandezza dell'azione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-125">The low-order words of **WM\_VSCROLL** and **WM\_HSCROLL** each contain a request code that indicates the direction and magnitude of the scrolling action.</span></span>

<span data-ttu-id="4fcdd-126">Quando vengono elaborati i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) , viene esaminato il codice della richiesta della barra di scorrimento e viene calcolato l'incremento dello scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-126">When the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages are processed, the scroll bar request code is examined and the scrolling increment is calculated.</span></span> <span data-ttu-id="4fcdd-127">Dopo che l'incremento è stato applicato alla posizione di scorrimento corrente, la finestra viene spostata nella nuova posizione utilizzando la funzione [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) e la posizione della casella di scorrimento viene regolata utilizzando la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="4fcdd-127">After the increment is applied to the current scrolling position, the window is scrolled to the new position by using the [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) function, and the position of the scroll box is adjusted by using the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span>

<span data-ttu-id="4fcdd-128">Dopo lo scorrimento di una finestra, parte dell'area client viene resa non valida.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-128">After a window is scrolled, part of its client area is made invalid.</span></span> <span data-ttu-id="4fcdd-129">Per assicurarsi che l'area non valida venga aggiornata, viene usata la funzione [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) per generare un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="4fcdd-129">To ensure that the invalid region is updated, the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function is used to generate a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

### <a name="processing-the-wm_paint-message"></a><span data-ttu-id="4fcdd-130">Elaborazione del \_ messaggio di disegno WM</span><span class="sxs-lookup"><span data-stu-id="4fcdd-130">Processing the WM\_PAINT Message</span></span>

<span data-ttu-id="4fcdd-131">Quando si elabora il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) , è consigliabile disegnare le righe di testo che si desidera visualizzare nella parte non valida della finestra.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-131">When processing the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, it is convenient to draw the lines of text that you want to appear in the invalid portion of the window.</span></span> <span data-ttu-id="4fcdd-132">Nell'esempio seguente vengono usate la posizione di scorrimento corrente e le dimensioni dell'area non valida per determinare l'intervallo di righe all'interno dell'area non valida per visualizzarle.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-132">The following example uses the current scrolling position and the dimensions of the invalid region to determine the range of lines within the invalid region in order to display them.</span></span>

## <a name="example-of-scrolling-text"></a><span data-ttu-id="4fcdd-133">Esempio di scorrimento del testo</span><span class="sxs-lookup"><span data-stu-id="4fcdd-133">Example of Scrolling Text</span></span>

<span data-ttu-id="4fcdd-134">Nell'esempio seguente viene illustrata una procedura di finestra per una finestra che Visualizza il testo nella relativa area client.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-134">The following example is a window procedure for a window that displays text in its client area.</span></span> <span data-ttu-id="4fcdd-135">Nell'esempio viene illustrato come scorrere il testo in risposta all'input dalle barre di scorrimento orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="4fcdd-135">The example demonstrates how to scroll the text in response to input from the horizontal and vertical scroll bars.</span></span>


```C++
#include "strsafe.h"

LRESULT CALLBACK MyTextWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
HDC hdc; 
PAINTSTRUCT ps; 
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
size_t abcLength;        // length of an abc[] item 

// Create an array of lines to display. 
#define LINES 28 
static TCHAR *abc[] = { 
       TEXT("anteater"),  TEXT("bear"),      TEXT("cougar"), 
       TEXT("dingo"),     TEXT("elephant"),  TEXT("falcon"), 
       TEXT("gazelle"),   TEXT("hyena"),     TEXT("iguana"), 
       TEXT("jackal"),    TEXT("kangaroo"),  TEXT("llama"), 
       TEXT("moose"),     TEXT("newt"),      TEXT("octopus"), 
       TEXT("penguin"),   TEXT("quail"),     TEXT("rat"), 
       TEXT("squid"),     TEXT("tortoise"),  TEXT("urus"), 
       TEXT("vole"),      TEXT("walrus"),    TEXT("xylophone"), 
       TEXT("yak"),       TEXT("zebra"),
       TEXT("This line contains words, but no character. Go figure."),
       TEXT("")
     }; 
 
switch (uMsg) 
{ 
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hwnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hwnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0; 
 
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
        SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
        return 0; 
    case WM_HSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;

        // Save the position for comparison later on.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;
        switch (LOWORD (wParam))
        {
        // User clicked the left arrow.
        case SB_LINELEFT: 
            si.nPos -= 1;
            break;
              
        // User clicked the right arrow.
        case SB_LINERIGHT: 
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft left of the scroll box.
        case SB_PAGELEFT:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft right of the scroll box.
        case SB_PAGERIGHT:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK: 
            si.nPos = si.nTrackPos;
            break;
              
        default :
            break;
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_HORZ, &si, TRUE);
        GetScrollInfo (hwnd, SB_HORZ, &si);
         
        // If the position has changed, scroll the window.
        if (si.nPos != xPos)
        {
            ScrollWindow(hwnd, xChar * (xPos - si.nPos), 0, NULL, NULL);
        }

        return 0;
         
    case WM_VSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hwnd, SB_VERT, &si);

        // Save the position for comparison later on.
        yPos = si.nPos;
        switch (LOWORD (wParam))
        {

        // User clicked the HOME keyboard key.
        case SB_TOP:
            si.nPos = si.nMin;
            break;
              
        // User clicked the END keyboard key.
        case SB_BOTTOM:
            si.nPos = si.nMax;
            break;
              
        // User clicked the top arrow.
        case SB_LINEUP:
            si.nPos -= 1;
            break;
              
        // User clicked the bottom arrow.
        case SB_LINEDOWN:
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft above the scroll box.
        case SB_PAGEUP:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft below the scroll box.
        case SB_PAGEDOWN:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK:
            si.nPos = si.nTrackPos;
            break;
              
        default:
            break; 
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_VERT, &si, TRUE);
        GetScrollInfo (hwnd, SB_VERT, &si);

        // If the position has changed, scroll window and update it.
        if (si.nPos != yPos)
        {                    
            ScrollWindow(hwnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
            UpdateWindow (hwnd);
        }

        return 0;
         
    case WM_PAINT :
        // Prepare the window for painting.
        hdc = BeginPaint (hwnd, &ps);

        // Get vertical scroll bar position.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_POS;
        GetScrollInfo (hwnd, SB_VERT, &si);
        yPos = si.nPos;

        // Get horizontal scroll bar position.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;

        // Find painting limits.
        FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
        LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
        for (i = FirstLine; i <= LastLine; i++)
        {
            x = xChar * (1 - xPos);
            y = yChar * (i - yPos);
              
            // Note that "55" in the following depends on the 
            // maximum size of an abc[] item. Also, you must include
            // strsafe.h to use the StringCchLength function.
            hr = StringCchLength(abc[i], 55, &abcLength);
            if ((FAILED(hr))|(abcLength == NULL))
            {
                //
                // TODO: write error handler
                //
            }

            // Write a line of text to the client area.
            TextOut(hdc, x, y, abc[i], abcLength); 
        }

        // Indicate that painting is finished.
        EndPaint (hwnd, &ps);
        return 0;
         
    case WM_DESTROY :
        PostQuitMessage (0);
        return 0;
    }

    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a><span data-ttu-id="4fcdd-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4fcdd-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fcdd-137">Uso delle barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="4fcdd-137">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="4fcdd-138">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="4fcdd-138">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 