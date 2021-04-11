---
title: Aggiunta del supporto per la manipolazione nel codice non gestito
description: In questa sezione viene illustrato come aggiungere il supporto per la manipolazione a codice non gestito implementando un sink di evento per l' \_ interfaccia IManipulationEvents.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Touch, modifiche
- Windows Touch, interfaccia _IManipulationEvents
- Windows Touch, interfaccia IManipulationProcessor
- manipolazioni, aggiunta del supporto nel codice non gestito
- manipolazioni, supporto del codice non gestito
- manipolazioni, supporto nel codice non gestito
- manipolazioni, interfaccia _IManipulationEvents
- manipolazioni, interfaccia IManipulationProcessor
- Interfaccia _IManipulationEvents, supporto di manipolazione nel codice non gestito
- Interfaccia IManipulationProcessor, supporto della manipolazione nel codice non gestito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2e000b6d3518c4e90eb5ae03b581e81037edf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118179"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Aggiunta del supporto per la manipolazione nel codice non gestito

In questa sezione viene illustrato come aggiungere il supporto per la manipolazione a codice non gestito implementando un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

Nell'immagine seguente viene illustrata l'architettura di manipolazione.

![illustrazione che mostra i messaggi di Windows Touch passati al processore di manipolazione di un oggetto, che gestisce gli eventi con l' \- interfaccia IManipulationEvents](images/manipulation-arch.png)

I dati di tocco ricevuti dai messaggi [**WM \_ touch**](wm-touchdown.md) vengono passati al [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) insieme all'ID contatto dal messaggio di tocco. In base alla sequenza di messaggi, l'interfaccia **IManipulationProcessor** calcolerà il tipo di trasformazione che viene eseguito e i valori associati a questa trasformazione. **IManipulationProcessor** genererà [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) che vengono gestite da un sink di evento. Il sink di evento può quindi utilizzare questi valori per eseguire operazioni personalizzate sull'oggetto trasformato.

Per aggiungere il supporto per la manipolazione all'applicazione, è necessario attenersi alla procedura seguente:

1.  Implementare un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .
2.  Creare un'istanza di un'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .
3.  Creare un'istanza del sink di evento e configurare gli eventi di tocco.
4.  Inviare i dati dell'evento Touch al processore di manipolazione.

In questa sezione vengono illustrati i passaggi da seguire per aggiungere il supporto per la modifica all'applicazione. Il codice viene fornito a ogni passaggio per iniziare.

> [!Note]  
> Non è possibile utilizzare le modifiche e i movimenti allo stesso tempo perché i messaggi di movimento e tocco si escludono a vicenda.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implementare un sink di evento per l' \_ interfaccia IManipualtionEvents

Prima di poter creare un'istanza del sink di evento, è necessario creare una classe che implementi l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) per la gestione degli eventi. Si tratta del sink di evento. Gli eventi generati dall'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) vengono gestiti dal sink di evento. Nel codice seguente viene illustrata un'intestazione di esempio per una classe che eredita l'interfaccia **\_ IManipulationEvents** .

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

Data l'intestazione, è necessario creare un'implementazione dell'interfaccia eventi in modo che la classe esegua le azioni che si desidera vengano eseguite dal processore di manipolazione. Il codice seguente è un modello che implementa la funzionalità minima di un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

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

Prestare particolare attenzione alle implementazioni dei metodi [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) nella classe. Questi sono i metodi più probabili nell'interfaccia che richiedono l'esecuzione di operazioni in base alle informazioni di manipolazione passate nell'evento. Si noti inoltre che il secondo parametro del costruttore è l'oggetto utilizzato nelle manipolazioni degli eventi. Nel codice usato per produrre l'esempio, hWnd per l'applicazione viene inviato al costruttore in modo che possa essere riposizionato e ridimensionato.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Creare un'istanza di un'interfaccia IManipulationProcessor

Nel codice in cui si utilizzeranno le modifiche, è necessario creare un'istanza di un'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Per prima cosa, è necessario aggiungere il supporto per la classe Manipulation. Il codice seguente illustra come è possibile eseguire questa operazione nella classe.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Quando si dispone della variabile per il processore di manipolazione e sono state incluse le intestazioni per le modifiche, è necessario creare un'istanza dell'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Si tratta di un oggetto COM. Pertanto, è necessario chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), quindi creare un'istanza del riferimento a **IManipulationProcessor**. Nel codice seguente viene illustrato come è possibile creare un'istanza di questa interfaccia.

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

Includere la definizione per la classe sink di evento nel codice e quindi aggiungere una variabile per la classe sink dell'evento di manipolazione. Nell'esempio di codice seguente è inclusa l'intestazione per l'implementazione della classe e viene impostata una variabile globale per archiviare il sink di evento.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Dopo aver creato la variabile e avere incluso la definizione per la nuova classe sink di evento, è possibile creare la classe usando il processore di manipolazione configurato nel passaggio precedente. Il codice seguente illustra come creare un'istanza di questa classe da **OnInitDialog**.

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> La modalità di creazione di un'istanza del sink di evento dipende da ciò che si sta eseguendo con i dati di manipolazione. Nella maggior parte dei casi, si creerà un sink di evento del processore di manipolazione che non ha lo stesso costruttore di questo esempio.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Inviare i dati dell'evento Touch al processore di manipolazione

Ora che il processore di manipolazione e il sink di evento sono stati impostati, è necessario inviare i dati di tocco al processore di manipolazione per attivare gli eventi di manipolazione.

> [!Note]  
> Si tratta della stessa procedura descritta in [Introduzione con i messaggi di Windows Touch](getting-started-with-multi-touch-messages.md).

Innanzitutto, si creerà del codice per decodificare i messaggi [**WM \_ touch**](wm-touchdown.md) e inviarli all'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) per generare eventi. Nel codice seguente viene illustrata un'implementazione di esempio chiamata dal metodo **WndProc** e viene restituito un **LRESULT** per la messaggistica.

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

Ora che è disponibile un metodo di utilità per la decodifica del messaggio [**WM \_ touch**](wm-touchdown.md) , è necessario passare i messaggi **WM \_ touch** alla funzione di utilità dal metodo **WndProc** . Il codice seguente illustra come è possibile eseguire questa operazione.

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

I metodi personalizzati implementati nel sink di evento dovrebbero ora funzionare. In questo esempio, il tocco della finestra lo sposta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche](getting-started-with-manipulations.md)
</dt> </dl>


 