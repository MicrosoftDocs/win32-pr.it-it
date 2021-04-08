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
# <a name="improving-the-single-finger-panning-experience"></a><span data-ttu-id="a1905-120">Miglioramento dell'esperienza di Single-Finger Panoramica</span><span class="sxs-lookup"><span data-stu-id="a1905-120">Improving the Single-Finger Panning Experience</span></span>

<span data-ttu-id="a1905-121">Se si compila un'applicazione destinata a Windows Touch, fornisce automaticamente il supporto per la Panoramica di base.</span><span class="sxs-lookup"><span data-stu-id="a1905-121">If you build an application that targets Windows Touch, it automatically provides basic panning support.</span></span> <span data-ttu-id="a1905-122">Tuttavia, è possibile usare il messaggio di [**\_ movimento WM**](wm-gesture.md) per fornire supporto avanzato per la panoramica su un singolo dito.</span><span class="sxs-lookup"><span data-stu-id="a1905-122">However, you can use the [**WM\_GESTURE**](wm-gesture.md) message to provide enhanced support for single-finger panning.</span></span>

## <a name="overview"></a><span data-ttu-id="a1905-123">Panoramica</span><span class="sxs-lookup"><span data-stu-id="a1905-123">Overview</span></span>

<span data-ttu-id="a1905-124">Per migliorare l'esperienza di panning a dito singolo, attenersi alla procedura descritta nelle sezioni successive di questo argomento:</span><span class="sxs-lookup"><span data-stu-id="a1905-124">To improve the single-finger panning experience, use these steps, as explained in subsequent sections of this topic:</span></span>

-   <span data-ttu-id="a1905-125">Creare un'applicazione con le barre di scorrimento e con i gesti rapidi disabilitati.</span><span class="sxs-lookup"><span data-stu-id="a1905-125">Create an application with scroll bars and with flicks disabled.</span></span>
-   <span data-ttu-id="a1905-126">Aggiunta del supporto per i messaggi di Pan di movimento.</span><span class="sxs-lookup"><span data-stu-id="a1905-126">Add support for gesture pan messages.</span></span>
-   <span data-ttu-id="a1905-127">Abilita rimbalzo.</span><span class="sxs-lookup"><span data-stu-id="a1905-127">Enable bounce.</span></span>

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a><span data-ttu-id="a1905-128">Creare un'applicazione con le barre di scorrimento e con i gesti rapidi disabilitati</span><span class="sxs-lookup"><span data-stu-id="a1905-128">Create an Application with Scroll Bars and with Flicks Disabled</span></span>

<span data-ttu-id="a1905-129">Prima di iniziare, è necessario creare un'applicazione con barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a1905-129">Before you begin, you must create an application with scroll bars.</span></span> <span data-ttu-id="a1905-130">Questo processo è illustrato nella sezione [supporto legacy per la panoramica con le barre di scorrimento](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="a1905-130">The section [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) explains this process.</span></span> <span data-ttu-id="a1905-131">Se si vuole iniziare con il contenuto di esempio, passare alla sezione e creare un'applicazione con le barre di scorrimento e quindi disabilitare i gesti rapidi.</span><span class="sxs-lookup"><span data-stu-id="a1905-131">If you want to start with the example content, go to that section and create an application with scroll bars and then disable flicks.</span></span> <span data-ttu-id="a1905-132">Se si dispone già di un'applicazione con barre di scorrimento funzionanti, disabilitare i gesti rapidi come descritto in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="a1905-132">If you already have an application with functioning scroll bars, disable flicks as described in that section.</span></span>

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a><span data-ttu-id="a1905-133">Aggiunta del supporto personalizzato per la panoramica dei movimenti</span><span class="sxs-lookup"><span data-stu-id="a1905-133">Add Custom Panning Support for Gesture Pan Messages</span></span>

<span data-ttu-id="a1905-134">Per supportare i messaggi del Pan di movimento, è necessario gestirli nel metodo **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="a1905-134">To support gesture pan messages, you must handle them in the **WndProc** method.</span></span> <span data-ttu-id="a1905-135">I messaggi di movimento vengono utilizzati per determinare i Delta orizzontali e verticali per i messaggi di Pan.</span><span class="sxs-lookup"><span data-stu-id="a1905-135">The gesture messages are used to determine horizontal and vertical deltas for pan messages.</span></span> <span data-ttu-id="a1905-136">I Delta vengono usati per aggiornare l'oggetto barra di scorrimento, che aggiorna l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a1905-136">The deltas are used to update the scroll bar object, which updates the user interface.</span></span>

<span data-ttu-id="a1905-137">Aggiornare innanzitutto le impostazioni della versione di Windows nel file targetver. h per abilitare Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="a1905-137">First, update the Windows version settings in the targetver.h file to enable Windows Touch.</span></span> <span data-ttu-id="a1905-138">Nel codice seguente vengono illustrate le diverse impostazioni della versione di Windows che devono essere sostituite in targetver. h.</span><span class="sxs-lookup"><span data-stu-id="a1905-138">The following code shows the various Windows version settings that should replace those in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



<span data-ttu-id="a1905-139">Aggiungere quindi il file UXTheme. h al progetto e aggiungere la libreria uxtheme. lib alle dipendenze aggiuntive del progetto.</span><span class="sxs-lookup"><span data-stu-id="a1905-139">Next, add the UXTheme.h file to your project and add the uxtheme.lib library to the additional dependencies of your project.</span></span>


```C++
#include <uxtheme.h>
```



<span data-ttu-id="a1905-140">Aggiungere quindi le variabili seguenti all'inizio della funzione **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="a1905-140">Next, add the following variables to the top of the **WndProc** function.</span></span> <span data-ttu-id="a1905-141">Questi verranno utilizzati nei calcoli per la panoramica.</span><span class="sxs-lookup"><span data-stu-id="a1905-141">These will be used in calculations for panning.</span></span>


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



<span data-ttu-id="a1905-142">Aggiungere quindi il gestore per il messaggio [**di \_ movimento WM**](wm-gesture.md) in modo che le barre di scorrimento vengano aggiornate con i Delta basati sui movimenti di panoramica.</span><span class="sxs-lookup"><span data-stu-id="a1905-142">Next, add the handler for the [**WM\_GESTURE**](wm-gesture.md) message so that the scroll bars are updated with deltas based on panning gestures.</span></span> <span data-ttu-id="a1905-143">In questo modo si ottiene un controllo più dettagliato della panoramica.</span><span class="sxs-lookup"><span data-stu-id="a1905-143">This gives you a much finer-grained control of panning.</span></span>

<span data-ttu-id="a1905-144">Il codice seguente ottiene la struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) da *lParam*, Salva l'ultima coordinata y dalla struttura e determina la modifica della posizione per aggiornare l'oggetto barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a1905-144">The following code gets the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure from the *lParam*, saves the last y-coordinate from the structure, and determines the change in position to update the scroll bar object.</span></span> <span data-ttu-id="a1905-145">Il codice seguente deve essere inserito nell'istruzione switch **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="a1905-145">The following code should be placed in your **WndProc** switch statement.</span></span>


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



<span data-ttu-id="a1905-146">A questo punto, quando si esegue il movimento della panoramica sulla finestra, viene visualizzato lo scorrimento del testo con inerzia.</span><span class="sxs-lookup"><span data-stu-id="a1905-146">Now, when you perform the pan gesture on your window, you will see the text scroll with inertia.</span></span> <span data-ttu-id="a1905-147">A questo punto, potrebbe essere necessario modificare il testo in modo da avere più righe, in modo da poter esplorare sezioni di testo di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a1905-147">At this point, you might want to change the text to have more lines so that you can explore panning large sections of text.</span></span>

## <a name="boundary-feedback-in-wndproc"></a><span data-ttu-id="a1905-148">Commenti sui limiti in WndProc</span><span class="sxs-lookup"><span data-stu-id="a1905-148">Boundary Feedback in WndProc</span></span>

<span data-ttu-id="a1905-149">Il feedback dei limiti è un tipo di feedback visivo assegnato agli utenti quando raggiungono la fine di un'area a cui è possibile accedere.</span><span class="sxs-lookup"><span data-stu-id="a1905-149">Boundary feedback is a type of visual feedback given to users when they reach the end of a pannable area.</span></span> <span data-ttu-id="a1905-150">Viene attivato dall'applicazione quando viene raggiunto un limite.</span><span class="sxs-lookup"><span data-stu-id="a1905-150">It is triggered by the application when a boundary is reached.</span></span> <span data-ttu-id="a1905-151">Nell'implementazione di esempio precedente del messaggio [**del \_ movimento WM**](wm-gesture.md) , la condizione finale `(si.nPos == si.yPos)` dal caso **del \_ movimento WM** viene utilizzata per verificare che sia stata raggiunta la fine di un'area di cui è possibile eseguire il provisioning.</span><span class="sxs-lookup"><span data-stu-id="a1905-151">In the previous example implementation of the [**WM\_GESTURE**](wm-gesture.md) message, the end condition `(si.nPos == si.yPos)` from the **WM\_GESTURE** case is used to test that you have reached the end of a pannable region.</span></span> <span data-ttu-id="a1905-152">Le variabili seguenti vengono utilizzate per tenere traccia dei valori e verificare gli errori.</span><span class="sxs-lookup"><span data-stu-id="a1905-152">The following variables are used to track values and test errors.</span></span>


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



<span data-ttu-id="a1905-153">Il caso di movimento Pan viene aggiornato per attivare il feedback del limite.</span><span class="sxs-lookup"><span data-stu-id="a1905-153">The pan gesture case is updated to trigger boundary feedback.</span></span> <span data-ttu-id="a1905-154">Nel codice riportato di seguito viene illustrato il caso della **\_ Panoramica GID** dal gestore di messaggi con [**\_ movimento WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="a1905-154">The following code illustrates the **GID\_PAN** case from the [**WM\_GESTURE**](wm-gesture.md) message handler.</span></span>


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



<span data-ttu-id="a1905-155">A questo punto, la finestra dell'applicazione deve avere un feedback sui limiti quando un utente passa dalla parte inferiore dell'area della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a1905-155">Now your application's window should have boundary feedback when a user pans past the bottom of the scroll bar region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1905-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1905-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1905-157">Movimenti tocco di Windows</span><span class="sxs-lookup"><span data-stu-id="a1905-157">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="a1905-158">**BeginPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="a1905-158">**BeginPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[<span data-ttu-id="a1905-159">**EndPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="a1905-159">**EndPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[<span data-ttu-id="a1905-160">**UpdatePanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="a1905-160">**UpdatePanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 