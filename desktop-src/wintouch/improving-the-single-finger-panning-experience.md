---
title: Miglioramento dell'esperienza di Single-Finger Panoramica
description: Se si compila un'applicazione destinata a Windows Touch, fornisce automaticamente il supporto per la Panoramica di base. Tuttavia, è possibile usare il \_ messaggio di movimento WM per fornire supporto avanzato per la panoramica su un singolo dito.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Touch, panoramica a singolo dito
- Windows Touch, panoramica
- Windows Touch, barre di scorrimento
- Windows Touch, gesti rapidi
- Windows Touch, messaggi di Pan di movimento
- Windows Touch, commenti sui limiti
- Panoramica su un solo dito
- Panoramica, Single-Finger
- Panoramica, commenti sui limiti
- barre di scorrimento, panoramica a dito singolo
- scorrimenti rapidi, panoramica a singolo dito
- barre di scorrimento, disabilitazione
- gesti rapidi, disabilitazione
- movimenti, messaggi di Pan di movimento
- Panoramica, messaggi di Pan movimento
- Commenti sui limiti, panoramica su un singolo dito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728018"
---
# <a name="improving-the-single-finger-panning-experience"></a>Miglioramento dell'esperienza di Single-Finger Panoramica

Se si compila un'applicazione destinata a Windows Touch, fornisce automaticamente il supporto per la Panoramica di base. Tuttavia, è possibile usare il messaggio di [**\_ movimento WM**](wm-gesture.md) per fornire supporto avanzato per la panoramica su un singolo dito.

## <a name="overview"></a>Panoramica

Per migliorare l'esperienza di panning a dito singolo, attenersi alla procedura descritta nelle sezioni successive di questo argomento:

-   Creare un'applicazione con le barre di scorrimento e con i gesti rapidi disabilitati.
-   Aggiunta del supporto per i messaggi di Pan di movimento.
-   Abilita rimbalzo.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Creare un'applicazione con le barre di scorrimento e con i gesti rapidi disabilitati

Prima di iniziare, è necessario creare un'applicazione con barre di scorrimento. Questo processo è illustrato nella sezione [supporto legacy per la panoramica con le barre di scorrimento](legacy-support-for-panning-with-scrollbars.md) . Se si vuole iniziare con il contenuto di esempio, passare alla sezione e creare un'applicazione con le barre di scorrimento e quindi disabilitare i gesti rapidi. Se si dispone già di un'applicazione con barre di scorrimento funzionanti, disabilitare i gesti rapidi come descritto in questa sezione.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Aggiunta del supporto personalizzato per la panoramica dei movimenti

Per supportare i messaggi del Pan di movimento, è necessario gestirli nel metodo **WndProc** . I messaggi di movimento vengono utilizzati per determinare i Delta orizzontali e verticali per i messaggi di Pan. I Delta vengono usati per aggiornare l'oggetto barra di scorrimento, che aggiorna l'interfaccia utente.

Aggiornare innanzitutto le impostazioni della versione di Windows nel file targetver. h per abilitare Windows Touch. Nel codice seguente vengono illustrate le diverse impostazioni della versione di Windows che devono essere sostituite in targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Aggiungere quindi il file UXTheme. h al progetto e aggiungere la libreria uxtheme. lib alle dipendenze aggiuntive del progetto.


```C++
#include <uxtheme.h>
```



Aggiungere quindi le variabili seguenti all'inizio della funzione **WndProc** . Questi verranno utilizzati nei calcoli per la panoramica.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Aggiungere quindi il gestore per il messaggio [**di \_ movimento WM**](wm-gesture.md) in modo che le barre di scorrimento vengano aggiornate con i Delta basati sui movimenti di panoramica. In questo modo si ottiene un controllo più dettagliato della panoramica.

Il codice seguente ottiene la struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) da *lParam*, Salva l'ultima coordinata y dalla struttura e determina la modifica della posizione per aggiornare l'oggetto barra di scorrimento. Il codice seguente deve essere inserito nell'istruzione switch **WndProc** .


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



A questo punto, quando si esegue il movimento della panoramica sulla finestra, viene visualizzato lo scorrimento del testo con inerzia. A questo punto, potrebbe essere necessario modificare il testo in modo da avere più righe, in modo da poter esplorare sezioni di testo di grandi dimensioni.

## <a name="boundary-feedback-in-wndproc"></a>Commenti sui limiti in WndProc

Il feedback dei limiti è un tipo di feedback visivo assegnato agli utenti quando raggiungono la fine di un'area a cui è possibile accedere. Viene attivato dall'applicazione quando viene raggiunto un limite. Nell'implementazione di esempio precedente del messaggio [**del \_ movimento WM**](wm-gesture.md) , la condizione finale `(si.nPos == si.yPos)` dal caso **del \_ movimento WM** viene utilizzata per verificare che sia stata raggiunta la fine di un'area di cui è possibile eseguire il provisioning. Le variabili seguenti vengono utilizzate per tenere traccia dei valori e verificare gli errori.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



Il caso di movimento Pan viene aggiornato per attivare il feedback del limite. Nel codice riportato di seguito viene illustrato il caso della **\_ Panoramica GID** dal gestore di messaggi con [**\_ movimento WM**](wm-gesture.md) .


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



A questo punto, la finestra dell'applicazione deve avere un feedback sui limiti quando un utente passa dalla parte inferiore dell'area della barra di scorrimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Movimenti tocco di Windows](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 