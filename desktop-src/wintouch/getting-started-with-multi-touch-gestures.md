---
title: Introduzione con i movimenti tocco di Windows
description: In questa sezione vengono descritti i passaggi di base per l'utilizzo di movimenti multitouch.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows Touch, movimenti
- Windows Touch, messaggi
- movimenti, informazioni
- movimenti, messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395390"
---
# <a name="getting-started-with-windows-touch-gestures"></a><span data-ttu-id="e2756-107">Introduzione con i movimenti tocco di Windows</span><span class="sxs-lookup"><span data-stu-id="e2756-107">Getting Started with Windows Touch Gestures</span></span>

<span data-ttu-id="e2756-108">In questa sezione vengono descritti i passaggi di base per l'utilizzo di movimenti multitouch.</span><span class="sxs-lookup"><span data-stu-id="e2756-108">This section describes the basic steps for using multitouch gestures.</span></span>

<span data-ttu-id="e2756-109">I passaggi seguenti vengono in genere eseguiti quando si utilizzano i movimenti tocco di Windows:</span><span class="sxs-lookup"><span data-stu-id="e2756-109">The following steps are typically performed when using Windows Touch gestures:</span></span>

1.  <span data-ttu-id="e2756-110">Configurare una finestra per la ricezione dei movimenti.</span><span class="sxs-lookup"><span data-stu-id="e2756-110">Set up a window for receiving gestures.</span></span>
2.  <span data-ttu-id="e2756-111">Gestire i messaggi di movimento.</span><span class="sxs-lookup"><span data-stu-id="e2756-111">Handle the gesture messages.</span></span>
3.  <span data-ttu-id="e2756-112">Interpretare i messaggi di movimento.</span><span class="sxs-lookup"><span data-stu-id="e2756-112">Interpret the gesture messages.</span></span>

## <a name="setting-up-a-window-to-receive-gestures"></a><span data-ttu-id="e2756-113">Impostazione di una finestra per la ricezione di movimenti</span><span class="sxs-lookup"><span data-stu-id="e2756-113">Setting up a Window to Receive Gestures</span></span>

<span data-ttu-id="e2756-114">Per impostazione predefinita, si ricevono messaggi di [**\_ movimento WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="e2756-114">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="e2756-115">Se si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), si smette di ricevere messaggi di [**\_ movimento WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="e2756-115">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="e2756-116">Se non si ricevono messaggi **di \_ movimento WM** , assicurarsi che non sia stato chiamato **RegisterTouchWindow**.</span><span class="sxs-lookup"><span data-stu-id="e2756-116">If you are not receiving **WM\_GESTURE** messages, make sure that you haven't called **RegisterTouchWindow**.</span></span>

 

<span data-ttu-id="e2756-117">Nel codice seguente viene illustrata un'implementazione di InitInstance semplice.</span><span class="sxs-lookup"><span data-stu-id="e2756-117">The following code shows a simple InitInstance implementation.</span></span>


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a><span data-ttu-id="e2756-118">Gestione dei messaggi di movimento</span><span class="sxs-lookup"><span data-stu-id="e2756-118">Handling Gesture Messages</span></span>

<span data-ttu-id="e2756-119">Analogamente alla gestione dei messaggi di input Windows Touch, è possibile gestire i messaggi di movimento in molti modi.</span><span class="sxs-lookup"><span data-stu-id="e2756-119">Similar to handling Windows Touch input messages, you can handle gesture messages in many ways.</span></span> <span data-ttu-id="e2756-120">Se si usa Win32, è possibile cercare il messaggio di [**\_ movimento WM**](wm-gesture.md) in WndProc.</span><span class="sxs-lookup"><span data-stu-id="e2756-120">If you are using Win32, you can check for the [**WM\_GESTURE**](wm-gesture.md) message in WndProc.</span></span> <span data-ttu-id="e2756-121">Se si sta creando un altro tipo di applicazione, è possibile aggiungere il messaggio di **\_ movimento WM** alla mappa messaggi e quindi implementare un gestore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e2756-121">If you are creating another type of application, you can add the **WM\_GESTURE** message to the message map and then implement a custom handler.</span></span>

<span data-ttu-id="e2756-122">Nel codice seguente viene illustrato come gestire i messaggi di movimento.</span><span class="sxs-lookup"><span data-stu-id="e2756-122">The following code shows how gesture messages could be handled.</span></span>


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a><span data-ttu-id="e2756-123">Interpretazione dei messaggi di movimento</span><span class="sxs-lookup"><span data-stu-id="e2756-123">Interpreting the Gesture Messages</span></span>

<span data-ttu-id="e2756-124">La funzione [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) viene usata per interpretare un messaggio di movimento in una struttura che descrive il movimento.</span><span class="sxs-lookup"><span data-stu-id="e2756-124">The [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) function is used to interpret a gesture message into a structure describing the gesture.</span></span> <span data-ttu-id="e2756-125">La struttura, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), contiene informazioni sul movimento, ad esempio la posizione in cui è stato eseguito il movimento e il tipo di movimento.</span><span class="sxs-lookup"><span data-stu-id="e2756-125">The structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), has information about the gesture such as the location where the gesture was performed and the type of gesture.</span></span> <span data-ttu-id="e2756-126">Nel codice seguente viene illustrato come è possibile recuperare e interpretare un messaggio di movimento.</span><span class="sxs-lookup"><span data-stu-id="e2756-126">The following code shows how you can retrieve and interpret a gesture message.</span></span>


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a><span data-ttu-id="e2756-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2756-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2756-128">Movimenti tocco di Windows</span><span class="sxs-lookup"><span data-stu-id="e2756-128">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




