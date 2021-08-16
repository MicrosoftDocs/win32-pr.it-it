---
title: Rilevamento e rilevamento di più punti di tocco
description: Rilevamento e rilevamento di più punti di tocco
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Tocco, più punti di tocco
- rilevamento di più punti di tocco
- rilevamento di più punti di tocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5b8086988dc1a87b5596d5a0ac74ec1f1df5ce4b85d928cbe306b791d17b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436068"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Rilevamento e rilevamento di più punti di tocco

La procedura seguente illustra come tenere traccia di più punti di tocco usando Windows Touch.

1.  Creare un'applicazione e abilitare Windows Touch.
2.  Aggiungere un gestore per [**WM \_ TOUCH**](wm-touchdown.md) e i punti di traccia.
3.  Disegnare i punti.

Dopo l'esecuzione, l'applicazione eseguirà il rendering dei cerchi sotto ogni tocco. La schermata seguente mostra l'aspetto dell'applicazione durante l'esecuzione.

![Screenshot che mostra un'applicazione che esegue il rendering dei punti tocco come cerchi verdi e gialli](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Creare un'applicazione e abilitare Windows Touch

Iniziare con un'applicazione Microsoft Win32 usando la Microsoft Visual Studio guidata. Dopo aver completato la procedura guidata, aggiungere il supporto per i messaggi Windows Touch impostando la versione di Windows in targetver.h e includendo windows.h e windowsx.h nell'applicazione. Il codice seguente illustra come impostare la versione Windows in targetver.h.


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



Il codice seguente illustra come aggiungere le direttive di inclusione. È anche possibile creare alcune variabili globali che verranno usate in un secondo momento.


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



## <a name="add-handler-for-wm_touch-and-track-points"></a>Aggiungere un gestore per WM \_ TOUCH e track point

Dichiarare prima di tutto alcune variabili usate dal gestore [**WM \_ TOUCH**](wm-touchdown.md) in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



Inizializzare ora le variabili usate per archiviare i punti di tocco e registrare la finestra per l'input tocco dal **metodo InitInstance.**


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



Gestire quindi il [**messaggio WM \_ TOUCH**](wm-touchdown.md) dal [**metodo WndProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Il codice seguente illustra un'implementazione del gestore per **WM \_ TOUCH.**


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
> Per usare la funzione [**ScreenToClient,**](/windows/desktop/api/winuser/nf-winuser-screentoclient) è necessario avere un supporto DPI elevato nell'applicazione. Per altre informazioni sul supporto di valori DPI elevati, vedere la [sezione high DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) di MSDN.

 

Ora, quando un utente tocca lo schermo, le posizioni toccate verranno archiviate nella matrice di punti. Il **membro dwID** della struttura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) archivia un identificatore che dipenderà dall'hardware.

Per risolvere il problema del membro dwID dipendente dall'hardware, il gestore del case [**WM \_ TOUCH**](wm-touchdown.md) usa una funzione, **GetContactIndex**, che esegue il mapping del membro **dwID** della struttura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) a un punto disegnato sullo schermo. Il codice seguente illustra un'implementazione di questa funzione.


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



## <a name="draw-the-points"></a>Disegnare i punti

Dichiarare le variabili seguenti per la routine di disegno.


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



Il contesto di visualizzazione della memoria *memDC* viene usato per archiviare un contesto grafico temporaneo scambiato con il contesto di visualizzazione sottoposto a rendering, *hdc*, per eliminare lo sfarfallio. Implementare la routine di disegno, che accetta i punti archiviati e disegna un cerchio in corrispondenza dei punti. Il codice seguente illustra come implementare il [**gestore WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)


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



Quando si esegue l'applicazione, l'aspetto dovrebbe essere simile a quello illustrato all'inizio di questa sezione.

Per divertimento, è possibile disegnare alcune linee aggiuntive intorno ai punti di tocco. Lo screenshot seguente mostra l'aspetto dell'applicazione con alcune linee aggiuntive disegnate intorno ai cerchi.

![Screenshot che mostra un'applicazione che esegue il rendering dei punti di tocco come cerchi con linee che attraversano i centri e intersecano i bordi dei punti di tocco](images/multitouchpointsfun.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Input tocco](guide-multi-touch-input.md)
</dt> </dl>

 

 