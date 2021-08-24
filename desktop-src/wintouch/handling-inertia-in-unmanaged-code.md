---
title: Gestione dell'inerzia nel codice non gestito
description: Questa sezione illustra come usare l'interfaccia IInertiaProcessor per gestire l'inerzia nel codice non gestito.
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Windows Tocco, inerzia
- Windows Tocco, processore di manipolazione
- inerzia, codice non gestito
- inerzia, interfaccia IInertiaProcessor
- inerzia, processore di manipolazione
- processore di manipolazione, inerzia
- Interfaccia IInertiaProcessor, codice non gestito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e112605b1f998b850c3a04a045166b376fc3a12d98615b9c2af72e756a1c1b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346501"
---
# <a name="handling-inertia-in-unmanaged-code"></a>Gestione dell'inerzia nel codice non gestito

Questa sezione illustra come usare [**l'interfaccia IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) per gestire l'inerzia nel codice non gestito.

## <a name="overview"></a>Panoramica

Per usare l'inerzia nel codice non gestito, è necessario implementare sink di evento sia per il processore di manipolazione che per il processore di inerzia. Per iniziare, aggiungere il supporto della manipolazione all'applicazione come descritto nella sezione Aggiunta del supporto [della manipolazione al codice non gestito](adding-manipulation-support-in-unmanaged-code.md). Si noti che il supporto della manipolazione richiede l'uso di messaggi di tocco anziché di movimenti per inviare i dati degli eventi al processore di manipolazione. Dopo aver modificato il funzionamento, è necessario implementare anche un secondo sink di evento per gli eventi generati dall'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) o modificare il sink di evento esistente per supportare sia gli eventi generati dalle interfacce **IInertiaProcessor** che [**IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) Ai fini di questo esempio, è più semplice iniziare dal sink di evento creato per la sezione Aggiunta del supporto di manipolazione al codice non gestito e aggiungere un secondo costruttore che funzioni con il processore di inerzia anziché con il processore di manipolazione. In questo modo, l'implementazione del sink di evento può funzionare per il processore di manipolazione o il processore di inerzia. Oltre ad aggiungere un secondo costruttore, il sink di evento avrà una variabile che indica se eseguirà le operazioni in base all'input di inerzia anziché all'input di manipolazione.

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>Aggiungere il supporto per l'inerzia a un sink di evento del processore di manipolazione

Il codice seguente illustra il nuovo costruttore del sink di evento, le nuove variabili membro per [**un'interfaccia IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) e un flag che indica se il sink sta estrapolando per l'inerzia.


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



Dopo che l'intestazione della classe ha i nuovi costruttori e un flag che indica se si sta estrapolando, è possibile implementare il sink di evento per avere blocchi di gestione separati per gli eventi [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Il costruttore che accetta **un IManipulationProcessor** e **un IInertiaProcessor** deve impostare il flag **fExtrapolating** su false, che indica che si tratta di un gestore eventi **IManipulationProcessor.** Il codice seguente illustra come può essere implementato il costruttore per un sink di evento che usa **IManipulationProcessor.**


```C++
CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=FALSE;

    m_pManip = pManip;
    
    m_pInert = pInert;
    
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pManip->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit
        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }

    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}
```



Il codice seguente illustra come può essere implementato il costruttore per un sink di evento che usa [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Questo costruttore imposta il flag **fExtrapolating** su true, a indicare che questa istanza della classe di sink di evento eseguirà l'estrapolazione e eseguirà tutte le operazioni di spostamento eseguite in precedenza dagli eventi del processore di manipolazione.


```C++
CManipulationEventSink::CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    m_pInert = pInert;
    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=TRUE;

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pInert->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }
    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}   
```



> [!Note]  
> L'implementazione della classe di sink di evento dal sink di evento del processore di manipolazione viene riutilizzata come sink di evento per il processore di inerzia.

 

Ora, quando si costruisce questa classe, **CManipulationEventSink**, può essere costruita come sink di evento per un processore di manipolazione o come sink di evento per un processore di inerzia. Quando viene costruito come sink di evento del processore di inerzia, il flag **fExtrapolating** sarà impostato su true, a indicare che gli eventi di manipolazione devono essere estrapolati.

> [!Note]  
> [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) verrà generato dalle interfacce [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)

 

All'avvio della manipolazione, vengono impostate le [**proprietà dell'interfaccia IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Il codice seguente illustra come viene gestito l'evento started.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;       

    // set origins in manipulation processor
    m_pInert->put_InitialOriginX(x);
    m_pInert->put_InitialOriginY(y);
    
    RECT screenRect;

    HWND desktop = GetDesktopWindow();
    GetClientRect(desktop, &screenRect);

    // physics settings
    // deceleration is units per square millisecond
    m_pInert->put_DesiredDeceleration(.1f);

    // set the boundaries        
    screenRect.left-= 1024;
    m_pInert->put_BoundaryLeft  ( static_cast<float>(screenRect.left   * 100));
    m_pInert->put_BoundaryTop   ( static_cast<float>(screenRect.top    * 100));
    m_pInert->put_BoundaryRight ( static_cast<float>(screenRect.right  * 100));
    m_pInert->put_BoundaryBottom( static_cast<float>(screenRect.bottom * 100));
    
    
    // Elastic boundaries - I set these to 90% of the screen 
    // so... 5% at left, 95% right, 5% top,  95% bottom
    // Values are whole numbers because units are in centipixels
    m_pInert->put_ElasticMarginLeft  (static_cast<float>(screenRect.left   * 5));
    m_pInert->put_ElasticMarginTop   (static_cast<float>(screenRect.top    * 5));
    m_pInert->put_ElasticMarginRight (static_cast<float>(screenRect.right  * 95));
    m_pInert->put_ElasticMarginBottom(static_cast<float>(screenRect.bottom * 95));
    
    
    return S_OK;
}
```



In questo esempio vengono usati delta di manipolazione per spostare la finestra. Il codice seguente illustra come viene gestito l'evento delta.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;
        
    RECT rect;
            
    GetWindowRect(m_hWnd, &rect);
        
    int oldWidth =  rect.right-rect.left;
    int oldHeight = rect.bottom-rect.top;            

    // scale and translate the window size / position    
    MoveWindow(m_hWnd,                                              // the window to move
        static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
        static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
        static_cast<int>(oldWidth * scaleDelta),                    // width
        static_cast<int>(oldHeight * scaleDelta),                   // height
        TRUE);                                                      // redraw
                     
    return S_OK;
}
```



In questo esempio, gli eventi di manipolazione completata avviano o arrestano un timer che chiamerà [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) sull'interfaccia [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Il codice seguente illustra come viene gestito l'evento di manipolazione completato.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;

    // place your code handler here to do any operations based on the manipulation   
    
    if (fExtrapolating){
        //Inertia Complete, stop the timer used for processing      
        KillTimer(m_hWnd,0);        
    }else{ 
        // setup velocities for inertia processor
        float vX = 0.0f;
        float vY = 0.0f;
        float vA = 0.0f;
        m_pManip->GetVelocityX(&vX);
        m_pManip->GetVelocityY(&vY);
        m_pManip->GetAngularVelocity(&vA);

        // complete any previous processing
        m_pInert->Complete();
        
        // Reset sets the  initial timestamp
        m_pInert->Reset();
                
        // 
        m_pInert->put_InitialVelocityX(vX);
        m_pInert->put_InitialVelocityY(vY);        
        
        m_pInert->put_InitialOriginX(x);
        m_pInert->put_InitialOriginY(y);
        
           
        // Start a timer
        SetTimer(m_hWnd,0, 50, 0);        
    }

    return S_OK;
}
```



Il codice seguente illustra come interpretare i **messaggi WM \_ TIMER** in **WndProc** per eseguire chiamate a [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) sull'interfaccia [**IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>Reinizializzare il processore di inerzia e il processore di manipolazione e inizializzare i sink di evento

Dopo aver modificato il sink di evento per supportare [**sia IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) che [**IInertiaProcessor,**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)è possibile inizializzare i sink di evento e configurarli per l'esecuzione dall'applicazione. Il codice seguente illustra come vengono allocati i puntatori a interfaccia.


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



Nell'esempio di codice seguente viene illustrato come creare un'istanza delle interfacce.


```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
   
   hr = CoCreateInstance(CLSID_InertiaProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIInertProc)
   );
```



Nell'esempio di codice seguente viene illustrato come costruire i sink di evento dati i puntatori a interfaccia e registrare la finestra per l'input tocco.


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inerzia](getting-started-with-inertia.md)
</dt> </dl>

 

 




