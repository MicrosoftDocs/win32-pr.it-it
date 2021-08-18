---
title: Aggiunta del supporto per la manipolazione nel codice non gestito
description: Questa sezione illustra come aggiungere il supporto della manipolazione al codice non gestito implementando un sink di evento per \_ l'interfaccia IManipulationEvents.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Tocco, manipolazioni
- Windows Interfaccia touch,_IManipulationEvents
- Windows Tocco, interfaccia IManipulationProcessor
- manipolazioni, aggiunta di supporto nel codice non gestito
- manipolazioni, supporto di codice non gestito
- manipolazioni, supporto nel codice non gestito
- manipolazioni, _IManipulationEvents interfaccia
- manipolazioni, interfaccia IManipulationProcessor
- _IManipulationEvents,supporto della manipolazione nel codice non gestito
- Interfaccia IManipulationProcessor, supporto della manipolazione nel codice non gestito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff526c128b6da83fae3a74b88cd3bb21bc3a81c507c0a76a7c70dbddc5f76d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710001"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Aggiunta del supporto per la manipolazione nel codice non gestito

Questa sezione illustra come aggiungere il supporto della manipolazione al codice non gestito implementando un sink di evento per [**\_ l'interfaccia IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)

L'immagine seguente illustra l'architettura di manipolazione.

![illustrazione che mostra i messaggi di tocco di Windows passati al processore di manipolazione di un oggetto, che gestisce gli eventi con \- l'interfaccia imanipulationevents](images/manipulation-arch.png)

I dati di tocco ricevuti dai [**messaggi TOUCH WM \_**](wm-touchdown.md) vengono passati a [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) insieme all'ID contatto dal messaggio di tocco. In base alla sequenza di messaggi, l'interfaccia **IManipulationProcessor** calcolerà il tipo di trasformazione in esecuzione e i valori associati a questa trasformazione. **IManipulationProcessor** genererà quindi [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) che vengono gestiti da un sink di evento. Il sink di evento può quindi usare questi valori per eseguire operazioni personalizzate sull'oggetto da trasformare.

Per aggiungere il supporto per la manipolazione all'applicazione, è necessario seguire questa procedura:

1.  Implementare un sink di evento per [**\_ l'interfaccia IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)
2.  Creare un'istanza di [**un'interfaccia IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
3.  Creare un'istanza del sink di evento e configurare gli eventi di tocco.
4.  Inviare i dati degli eventi di tocco al processore di manipolazione.

Questa sezione illustra i passaggi da seguire per aggiungere il supporto per la manipolazione all'applicazione. Il codice viene fornito in ogni passaggio per iniziare.

> [!Note]  
> Non è possibile usare manipolazioni e movimenti contemporaneamente perché i messaggi di movimento e tocco si escludono a vicenda.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implementare un sink di evento \_ per l'interfaccia IManipualtionEvents

Prima di poter creare un'istanza del sink di evento, è necessario creare una classe che implementi [**\_ l'interfaccia IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) per l'evento. Si tratta del sink di evento. Gli eventi generati [**dall'interfaccia IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) vengono gestiti dal sink di evento. Il codice seguente illustra un'intestazione di esempio per una classe che eredita **\_ l'interfaccia IManipulationEvents.**

```C++
// Manipulation Header Files
#include <comdef.h>
#include <manipulations.h>
#include <ocidl.h>

class CManipulationEventSink : _IManipulationEvents
{
public:
    CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd);

    int GetStartedEventCount();
    int GetDeltaEventCount();
    int GetCompletedEventCount();
    double CManipulationEventSink::GetX();
    double CManipulationEventSink::GetY();        

    ~CManipulationEventSink();

    //////////////////////////////
    // IManipulationEvents methods
    //////////////////////////////
    virtual HRESULT STDMETHODCALLTYPE ManipulationStarted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationDelta( 
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
        /* [in] */ FLOAT cumulativeRotation);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationCompleted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);

    ////////////////////////////////////////////////////////////
    // IUnknown methods
    ////////////////////////////////////////////////////////////
    STDMETHOD_(ULONG, AddRef)(void);
    STDMETHOD_(ULONG, Release)(void);
    STDMETHOD(QueryInterface)(REFIID riid, LPVOID *ppvObj);

private:
    double m_fX;
    double m_fY;

    int m_cRefCount;
    int m_cStartedEventCount;
    int m_cDeltaEventCount;
    int m_cCompletedEventCount;

    IManipulationProcessor* m_pManip;

    IConnectionPointContainer* m_pConPointContainer;
    IConnectionPoint* m_pConnPoint;
    
    HWND m_hWnd;
};     
```

Data l'intestazione , è necessario creare un'implementazione dell'interfaccia degli eventi in modo che la classe esegua le azioni che il processore di manipolazione deve eseguire. Il codice seguente è un modello che implementa la funzionalità minima di un sink di evento per [**\_ l'interfaccia IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)

```C++
#include "stdafx.h"
#include "cmanipulationeventsink.h"

CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    m_pManip = manip;
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = manip->QueryInterface(
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

int CManipulationEventSink::GetStartedEventCount()
{
    return m_cStartedEventCount;
}

int CManipulationEventSink::GetDeltaEventCount()
{
    return m_cDeltaEventCount;
}

int CManipulationEventSink::GetCompletedEventCount()
{
    return m_cCompletedEventCount;
}

double CManipulationEventSink::GetX()
{
    return m_fX;
}

double CManipulationEventSink::GetY()
{
    return m_fY;
}

CManipulationEventSink::~CManipulationEventSink()
{
    //Cleanup.
}

///////////////////////////////////
//Implement IManipulationEvents
///////////////////////////////////

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;
    
    return S_OK;
}

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
    MoveWindow(m_hWnd,                                                     // the window to move
               static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
               static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
               static_cast<int>(oldWidth * scaleDelta),                    // width
               static_cast<int>(oldHeight * scaleDelta),                   // height
               TRUE);                                                      // redraw
                     
    return S_OK;
}

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

    return S_OK;
}


/////////////////////////////////
//Implement IUnknown
/////////////////////////////////

ULONG CManipulationEventSink::AddRef(void) 
{
    return ++m_cRefCount;
}

ULONG CManipulationEventSink::Release(void)
{ 
    m_cRefCount --;

    if(0 == m_cRefCount) {
        delete this;
        return 0;
    }

    return m_cRefCount;
}

HRESULT CManipulationEventSink::QueryInterface(REFIID riid, LPVOID *ppvObj) 
{
    if (IID__IManipulationEvents == riid) {
        *ppvObj = (_IManipulationEvents *)(this); AddRef(); return S_OK;
    } else if (IID_IUnknown == riid) {
        *ppvObj = (IUnknown *)(this); AddRef(); return S_OK;
    } else {
        return E_NOINTERFACE;
    }
}         
```

Prestare particolare attenzione alle implementazioni [**dei metodi ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) nella classe . Questi sono i metodi più probabili nell'interfaccia che richiedono l'esecuzione di operazioni in base alle informazioni di manipolazione passate nell'evento. Si noti anche che il secondo parametro nel costruttore è l'oggetto usato nelle modifiche degli eventi. Nel codice usato per la produzione dell'esempio, l'oggetto hWnd per l'applicazione viene inviato al costruttore in modo che possa essere riposizionato e ridimensionato.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Creare un'istanza di un'interfaccia IManipulationProcessor

Nel codice in cui si useranno le modifiche, è necessario creare un'istanza di [**un'interfaccia IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) Prima di tutto è necessario aggiungere il supporto per la classe manipulations. Il codice seguente illustra come eseguire questa operazione nella classe .

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Dopo aver creato la variabile per il processore di manipolazione e aver incluso le intestazioni per le modifiche, è necessario creare un'istanza [**dell'interfaccia IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) Si tratta di un oggetto COM. È quindi necessario chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e quindi creare un'istanza del riferimento a **IManipulationProcessor.** Nel codice seguente viene illustrato come creare un'istanza di questa interfaccia.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Creare un'istanza del sink di evento e configurare gli eventi di tocco

Includere la definizione per la classe del sink di evento nel codice e quindi aggiungere una variabile per la classe del sink di evento di manipolazione. L'esempio di codice seguente include l'intestazione per l'implementazione della classe e configura una variabile globale per archiviare il sink di evento.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Dopo aver creato la variabile e aver incluso la definizione per la nuova classe di sink di evento, è possibile costruire la classe usando il processore di manipolazione configurato nel passaggio precedente. Nel codice seguente viene illustrato come creare un'istanza di questa classe da **OnInitDialog.**

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> Il modo in cui si crea un'istanza del sink di evento dipende dalle operazioni che si stanno eseguendo con i dati di manipolazione. Nella maggior parte dei casi, si creerà un sink di evento del processore di manipolazione che non ha lo stesso costruttore di questo esempio.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Inviare i dati degli eventi di tocco al processore di manipolazione

Ora che il processore di manipolazione e il sink di eventi sono stati impostati, è necessario fornire i dati di tocco al processore di manipolazione per attivare gli eventi di manipolazione.

> [!Note]  
> Si tratta della stessa procedura descritta in Attività iniziali [con Windows touch.](getting-started-with-multi-touch-messages.md)

In primo luogo, si creerà codice per decodificare i messaggi [**WM \_ TOUCH**](wm-touchdown.md) e inviarli [**all'interfaccia IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) per generare eventi. Il codice seguente illustra un'implementazione di esempio che viene chiamata dal **metodo WndProc** e restituisce un **LRESULT** per la messaggistica.

```C++
LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam )
{
  UINT cInputs = LOWORD(wParam);
  PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
  
  BOOL bHandled = FALSE;
  
  if (NULL != pInputs) {
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
      cInputs,
      pInputs,
      sizeof(TOUCHINPUT))) {      
      for (UINT i=0; i<cInputs; i++){
        if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN){
            g_pIManipProc->ProcessDown(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_UP){
            g_pIManipProc->ProcessUp(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE){
            g_pIManipProc->ProcessMove(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
      }      
    } else {
      // GetLastError() and error handling
    }
    delete [] pInputs;
  } else {
    // error handling, presumably out of memory
  }
  if (bHandled){
    // if you don't want to pass to DefWindowProc, close the touch input handle
    if (!CloseTouchInputHandle((HTOUCHINPUT)lParam)) {
        // error handling
    }
    return 0;
  }else{
    return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
  }
}
```

Ora che è disponibile un metodo di utilità per decodificare il messaggio [**WM \_ TOUCH,**](wm-touchdown.md) è necessario passare i messaggi **WM \_ TOUCH** alla funzione di utilità dal **metodo WndProc.** Il codice seguente illustra come eseguire questa operazione.

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_TOUCH:
        return OnTouch(hWnd, wParam, lParam);
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &ps);
        // TODO: Add any drawing code here...
        EndPaint(hWnd, &ps);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```

I metodi personalizzati implementati nel sink di evento dovrebbero ora funzionare. In questo esempio, toccando la finestra verrà spostata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche](getting-started-with-manipulations.md)
</dt> </dl>


 