---
title: Rilevamento e rilevamento di più punti di tocco
description: Rilevamento e rilevamento di più punti di tocco
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Touch, più punti di tocco
- rilevamento di più punti di tocco
- rilevamento di più punti di tocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473779"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a><span data-ttu-id="2dd5e-106">Rilevamento e rilevamento di più punti di tocco</span><span class="sxs-lookup"><span data-stu-id="2dd5e-106">Detecting and Tracking Multiple Touch Points</span></span>

<span data-ttu-id="2dd5e-107">Nei passaggi seguenti viene illustrato come tenere traccia di più punti di tocco utilizzando Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-107">The following steps explain how to track multiple touch points using Windows Touch.</span></span>

1.  <span data-ttu-id="2dd5e-108">Creare un'applicazione e abilitare Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-108">Create an application and enable Windows Touch.</span></span>
2.  <span data-ttu-id="2dd5e-109">Aggiungere un gestore per i punti di controllo [**WM \_**](wm-touchdown.md) e track point.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-109">Add a handler for [**WM\_TOUCH**](wm-touchdown.md) and track points.</span></span>
3.  <span data-ttu-id="2dd5e-110">Creare i punti.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-110">Draw the points.</span></span>

<span data-ttu-id="2dd5e-111">Dopo che l'applicazione è in esecuzione, eseguirà il rendering dei cerchi sotto ogni tocco.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-111">After you have your application running, it will render circles under each touch.</span></span> <span data-ttu-id="2dd5e-112">Lo screenshot seguente mostra il modo in cui l'applicazione potrebbe apparire durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-112">The following screen shot shows how your application might look while running.</span></span>

![screenshot che mostra un'applicazione che esegue il rendering di punti di tocco come cerchi verde e giallo](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a><span data-ttu-id="2dd5e-114">Creare un'applicazione e abilitare Windows Touch</span><span class="sxs-lookup"><span data-stu-id="2dd5e-114">Create an Application and Enable Windows Touch</span></span>

<span data-ttu-id="2dd5e-115">Iniziare con un'applicazione Microsoft Win32 usando la procedura guidata di Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-115">Start with a Microsoft Win32 application using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="2dd5e-116">Dopo aver completato la procedura guidata, aggiungere il supporto per i messaggi di Windows Touch impostando la versione di Windows in targetver. h e includendo Windows. h e WINDOWSX. h nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-116">After you have completed the wizard, add support for Windows Touch messages by setting the Windows version in targetver.h and including windows.h and windowsx.h in your application.</span></span> <span data-ttu-id="2dd5e-117">Nel codice seguente viene illustrato come impostare la versione di Windows in targetver. h.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-117">The following code shows how to set the Windows version in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



<span data-ttu-id="2dd5e-118">Il codice seguente illustra come aggiungere le direttive include.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-118">The following code shows how your include directives should be added.</span></span> <span data-ttu-id="2dd5e-119">Inoltre, è possibile creare alcune variabili globali che verranno usate in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-119">Also, you can create some global variables that will be used later.</span></span>


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a><span data-ttu-id="2dd5e-120">Aggiungere un gestore per i punti di controllo e di traccia di WM \_</span><span class="sxs-lookup"><span data-stu-id="2dd5e-120">Add Handler for WM\_TOUCH and Track Points</span></span>

<span data-ttu-id="2dd5e-121">Dichiarare innanzitutto alcune variabili usate dal gestore [**WM \_ touch**](wm-touchdown.md) in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2dd5e-121">First, declare some variables that are used by the [**WM\_TOUCH**](wm-touchdown.md) handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span></span>


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



<span data-ttu-id="2dd5e-122">A questo punto, inizializzare le variabili usate per archiviare i punti di tocco e registrare la finestra per l'input tocco dal metodo **InitInstance** .</span><span class="sxs-lookup"><span data-stu-id="2dd5e-122">Now, initialize the variables used for storing touch points and register the window for touch input from the **InitInstance** method.</span></span>


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



<span data-ttu-id="2dd5e-123">Gestire quindi il messaggio [**WM \_ touch**](wm-touchdown.md) dal metodo [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2dd5e-123">Next, handle the [**WM\_TOUCH**](wm-touchdown.md) message from the [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) method.</span></span> <span data-ttu-id="2dd5e-124">Il codice seguente illustra un'implementazione del gestore per **WM \_ touch**.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-124">The following code shows an implementation of the handler for **WM\_TOUCH**.</span></span>


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> <span data-ttu-id="2dd5e-125">Per usare la funzione [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , è necessario disporre di un supporto DPI elevato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-125">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="2dd5e-126">Per ulteriori informazioni sul supporto di valori DPI alti, vedere la sezione relativa a [DPI elevata]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) di MSDN.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-126">For more information on supporting high DPI, see the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

 

<span data-ttu-id="2dd5e-127">A questo punto, quando un utente tocca lo schermo, le posizioni che sta toccando verranno archiviate nella matrice points.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-127">Now when a user touches the screen, the positions that he or she is touching will be stored in the points array.</span></span> <span data-ttu-id="2dd5e-128">Il membro **dwID** della struttura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) archivia un identificatore che dipende dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-128">The **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure stores an identifier that will be hardware dependent.</span></span>

<span data-ttu-id="2dd5e-129">Per risolvere il problema del membro dwID dipendente dall'hardware, il gestore [**WM \_ touch**](wm-touchdown.md) case usa una funzione, **GetContactIndex**, che esegue il mapping del membro **dwID** della struttura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) a un punto disegnato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-129">To address the issue of the dwID member being dependent on hardware, the [**WM\_TOUCH**](wm-touchdown.md) case handler uses a function, **GetContactIndex**, that maps the **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to a point that is drawn on the screen.</span></span> <span data-ttu-id="2dd5e-130">Nel codice seguente viene illustrata un'implementazione di questa funzione.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-130">The following code shows an implementation of this function.</span></span>


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a><span data-ttu-id="2dd5e-131">Creare punti</span><span class="sxs-lookup"><span data-stu-id="2dd5e-131">Draw the Points</span></span>

<span data-ttu-id="2dd5e-132">Dichiarare le variabili seguenti per la routine di disegno.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-132">Declare the following variables for the drawing routine.</span></span>


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



<span data-ttu-id="2dd5e-133">Il contesto di visualizzazione della memoria *memDC* viene usato per archiviare un contesto grafico temporaneo che viene scambiato con il contesto di visualizzazione di cui è stato eseguito il rendering, *HDC*, per eliminare lo sfarfallio.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-133">The memory display context *memDC* is used for storing a temporary graphics context that is swapped with the rendered display context, *hdc*, to eliminate flickering.</span></span> <span data-ttu-id="2dd5e-134">Implementare la routine di disegno, che accetta i punti archiviati e disegna un cerchio nei punti.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-134">Implement the drawing routine, which takes the points you have stored and draws a circle at the points.</span></span> <span data-ttu-id="2dd5e-135">Il codice seguente illustra come implementare il gestore di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="2dd5e-135">The following code shows how you could implement the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) handler.</span></span>


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



<span data-ttu-id="2dd5e-136">Quando si esegue l'applicazione, ora dovrebbe essere simile a quella illustrata all'inizio di questa sezione.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-136">When you run your application, it now should look something like the illustration at the beginning of this section.</span></span>

<span data-ttu-id="2dd5e-137">Per divertimento, è possibile creare alcune linee aggiuntive intorno ai punti di tocco.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-137">For fun, you can draw some extra lines around the touch points.</span></span> <span data-ttu-id="2dd5e-138">Lo screenshot seguente mostra il modo in cui l'applicazione può apparire con alcune linee aggiuntive disegnate intorno ai cerchi.</span><span class="sxs-lookup"><span data-stu-id="2dd5e-138">The following screen shot shows how the application could look with a few extra lines drawn around the circles.</span></span>

![screenshot che mostra un'applicazione che esegue il rendering di punti di tocco come cerchi con linee attraverso i centri e interseca i bordi dei punti di tocco](images/multitouchpointsfun.png)

## <a name="related-topics"></a><span data-ttu-id="2dd5e-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2dd5e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dd5e-141">Input Windows Touch</span><span class="sxs-lookup"><span data-stu-id="2dd5e-141">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 