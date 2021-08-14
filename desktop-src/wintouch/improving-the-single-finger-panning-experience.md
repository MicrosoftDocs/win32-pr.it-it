---
title: Miglioramento dell'Single-Finger panoramica
description: Se si compila un'applicazione destinata a Windows Touch, fornisce automaticamente il supporto per la panoramica di base. È tuttavia possibile usare il messaggio WM GESTURE per fornire supporto avanzato per la panoramica \_ con un solo dito.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Tocco, panoramica con un dito
- Windows Tocco, panoramica
- Windows Tocco, barre di scorrimento
- Windows Tocco, gesti rapidi
- Windows Tocco, messaggi di panoramica dei movimenti
- Windows Tocco, feedback sui limiti
- panoramica con un solo dito
- panoramica, dito singolo
- panoramica, feedback sui limiti
- barre di scorrimento, panoramica con un dito
- gesti rapidi, panoramica con un solo dito
- barre di scorrimento, disabilitazione
- gesti rapidi, disabilitazione
- movimenti, messaggi di panoramica dei movimenti
- panoramica, messaggi di panoramica dei movimenti
- feedback sui limiti, panoramica con un dito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf740d673e8bd2d2711238902d3de6c89d21a01fe330524b910db050011872f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435444"
---
# <a name="improving-the-single-finger-panning-experience"></a>Miglioramento dell'Single-Finger panoramica

Se si compila un'applicazione destinata a Windows Touch, fornisce automaticamente il supporto per la panoramica di base. È tuttavia possibile usare il messaggio [**WM \_ GESTURE**](wm-gesture.md) per fornire supporto avanzato per la panoramica con un solo dito.

## <a name="overview"></a>Panoramica

Per migliorare l'esperienza di panoramica con un solo dito, seguire questa procedura, come illustrato nelle sezioni successive di questo argomento:

-   Creare un'applicazione con barre di scorrimento e gesti rapidi disabilitati.
-   Aggiunta del supporto per i messaggi di panoramica dei movimenti.
-   Abilitare il bounce.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Creare un'applicazione con barre di scorrimento e gesti rapidi disabilitati

Prima di iniziare, è necessario creare un'applicazione con barre di scorrimento. La sezione [Supporto legacy per la panoramica con barre di scorrimento](legacy-support-for-panning-with-scrollbars.md) illustra questo processo. Se si vuole iniziare con il contenuto di esempio, passare a tale sezione e creare un'applicazione con barre di scorrimento e quindi disabilitare i gesti rapidi. Se si dispone già di un'applicazione con barre di scorrimento funzionanti, disabilitare i gesti rapidi come descritto in tale sezione.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Aggiungere il supporto per la panoramica personalizzata per i messaggi di panoramica movimenti

Per supportare i messaggi di panoramica dei movimenti, è necessario gestirli nel **metodo WndProc.** I messaggi di movimento vengono usati per determinare i delta orizzontali e verticali per i messaggi di panoramica. I delta vengono usati per aggiornare l'oggetto barra di scorrimento, che aggiorna l'interfaccia utente.

Prima di tutto, aggiornare Windows le impostazioni della versione nel file targetver.h per abilitare Windows Touch. Il codice seguente illustra le varie impostazioni Windows versione che devono sostituire quelle in targetver.h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Aggiungere quindi il file UXTheme.h al progetto e aggiungere la libreria uxtheme.lib alle dipendenze aggiuntive del progetto.


```C++
#include <uxtheme.h>
```



Aggiungere quindi le variabili seguenti all'inizio della **funzione WndProc.** Questi verranno usati nei calcoli per la panoramica.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Aggiungere quindi il gestore per il messaggio [**WM \_ GESTURE**](wm-gesture.md) in modo che le barre di scorrimento siano aggiornate con delta in base ai movimenti di panoramica. In questo modo si ha un controllo molto più granulare della panoramica.

Il codice seguente ottiene la struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) da *lParam*, salva l'ultima coordinata y dalla struttura e determina la modifica della posizione per aggiornare l'oggetto barra di scorrimento. Il codice seguente deve essere inserito **nell'istruzione switch WndProc.**


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



A questo punto, quando si esegue il movimento di panoramica nella finestra, il testo scorre con inerzia. A questo punto, è possibile modificare il testo in modo che abbia più righe in modo da poter esplorare la panoramica di sezioni di testo di grandi dimensioni.

## <a name="boundary-feedback-in-wndproc"></a>Feedback sui limiti in WndProc

Il feedback sui limiti è un tipo di feedback visivo fornito agli utenti quando raggiungono la fine di un'area panoramica. Viene attivato dall'applicazione quando viene raggiunto un limite. Nell'implementazione di esempio precedente del messaggio [**WM \_ GESTURE**](wm-gesture.md) viene usata la condizione finale del caso WM GESTURE per verificare che sia stata raggiunta la fine di un'area `(si.nPos == si.yPos)` **\_** panoramica. Le variabili seguenti vengono usate per tenere traccia dei valori e degli errori di test.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



Il caso del movimento di panoramica viene aggiornato per attivare il feedback sui limiti. Il codice seguente illustra il case **GID \_ PAN** del gestore [**di messaggi WM \_ GESTURE.**](wm-gesture.md)


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



Ora la finestra dell'applicazione deve avere un feedback sui limiti quando un utente esegue una panoramica oltre la parte inferiore dell'area della barra di scorrimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Movimenti tocco](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 