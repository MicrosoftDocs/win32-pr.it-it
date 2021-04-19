---
description: Questo programma illustra come creare un'applicazione che acquisisce gli eventi InkCollector usando solo C++. Questo programma crea un oggetto InkCollector per abilitare l'input penna nella finestra. Viene visualizzata una finestra di messaggio ogni volta che viene ricevuto un evento Stroke.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Esempio di sink di evento C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305354"
---
# <a name="c-event-sinks-sample"></a>Esempio di sink di evento C++

Questo programma illustra come creare un'applicazione che acquisisce gli eventi InkCollector usando solo C++. Questo programma crea un oggetto [**InkCollector**](inkcollector-class.md) per abilitare l'input penna nella finestra. Viene visualizzata una finestra di messaggio ogni volta che viene ricevuto un evento [**Stroke**](inkcollector-stroke.md) .

## <a name="defining-a-wrapper-for-ink-collector-events"></a>Definizione di un wrapper per eventi dell'agente di raccolta input penna

La `InkCollectorEvents` classe gestisce il passaggio degli eventi dell'agente di raccolta input penna dall'agente di raccolta input penna all'utente di questa classe. Il `AdviseInkCollector` metodo configura la connessione tra l'oggetto [**InkCollector**](inkcollector-class.md) e questa classe. Il `Invoke` metodo converte la notifica degli eventi [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in una chiamata a una funzione virtuale che può essere sostituita dall'utente di questa classe per elaborare un evento specifico.

> [!Note]  
> Per ottenere tale evento, è necessario eseguire l'override della funzione virtuale per un gestore eventi. Per tutti gli eventi, tranne quelli predefiniti, è necessario chiamare il metodo [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) dell'agente di raccolta input penna per garantire l'ottenimento di un evento. In secondo luogo, questo oggetto esegue il marshalling di se stesso, in modo che tutti i gestori eventi implementati debbano essere anche a thread libero. Di particolare importanza è l'uso delle API di Windows, che può causare un passaggio a un altro thread perché non è garantito che il gestore eventi sia in esecuzione nello stesso thread della finestra connessa con l'agente di raccolta input penna.

 


```C++
// Invoke translates from IDispatch to an event callout
//  that can be overriden by a subclass of this class.
STDMETHOD(Invoke)(
   DISPID dispidMember, 
    REFIID riid,
    LCID lcid, 
    WORD /*wFlags*/, 
    DISPPARAMS* pdispparams, 
    VARIANT* pvarResult,
    EXCEPINFO* /*pexcepinfo*/, 
    UINT* /*puArgErr*/)
{
    switch(dispidMember)
    {
        case DISPID_ICEStroke:
            Stroke(
                (IInkCursor*) pdispparams->rgvarg[2].pdispVal,
                (IInkStrokeDisp*) pdispparams->rgvarg[1].pdispVal,
                (VARIANT_BOOL *)pdispparams->rgvarg[0].pboolVal);
            break;
        ...
    }
    return S_OK;
}

virtual void Stroke(
    IInkCursor* Cursor,
    IInkStrokeDisp* Stroke,
    VARIANT_BOOL *Cancel)
{
    // This is a place holder designed to be overridden by
    //  user of this class.
    return;
}
...
```



Il `Init` metodo chiama [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) per configurare un gestore di marshalling a thread libero.


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



Il `AdviseInkCollector` metodo configura la connessione tra l'oggetto [**InkCollector**](inkcollector-class.md) e questa classe. Viene innanzitutto recuperato un punto di connessione all'agente di raccolta input penna. Viene quindi recuperato un puntatore a in `IInkCollectorEvents` modo che sia possibile stabilire una connessione consultiva al controllo.


```C++
// Set up connection between sink and InkCollector
HRESULT AdviseInkCollector(
    IInkCollector *pIInkCollector)
{
    // Get the connection point container
    IConnectionPointContainer *pIConnectionPointContainer;
    HRESULT hr = pIInkCollector->QueryInterface(IID_IConnectionPointContainer, (void **) &pIConnectionPointContainer);
        
    if (FAILED(hr))
        ...
    
    // Find the connection point for Ink Collector events
    hr = pIConnectionPointContainer->FindConnectionPoint(__uuidof(_IInkCollectorEvents), &m_pIConnectionPoint);
        
    if (SUCCEEDED(hr))
    {
        // Hook up sink to connection point
        hr = m_pIConnectionPoint->Advise(this, &m_dwCookie);
    }
    
    if (FAILED(hr))
        ...
    
    // Don't need the connection point container any more.
    pIConnectionPointContainer->Release();
    return hr;
}
```



Il `UnadviseInkCollector` metodo rilascia le connessioni che l'oggetto ha al controllo.


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>Definizione di un gestore eventi dell'agente di raccolta input penna

La classe CMyInkEvents esegue l'override del comportamento predefinito del gestore dell'evento [**Stroke**](inkcollector-stroke.md) della classe InkCollectorEvents. Il metodo Stroke Visualizza una finestra di messaggio quando l'oggetto [**InkCollector**](inkcollector-class.md) riceve un evento **Stroke** .


```C++
class CMyInkEvents : public InkCollectorEvents
{
public:

    // Event: Stroke
    virtual void Stroke(
        IInkCursor* Cursor,
        IInkStrokeDisp* Stroke,
        VARIANT_BOOL *Cancel)
    {
        // Demonstrate that the event notification was received.
        MessageBox(m_hWnd, "Stroke Event", "Event Received", MB_OK);
    }
    
    CMyInkEvents()
    {
        m_hWnd = NULL;
    }
    
    HRESULT Init(
        HWND hWnd)
    {
        m_hWnd = hWnd;
        return InkCollectorEvents::Init();
    }    
    
    HWND m_hWnd;
};
```



## <a name="defining-an-ink-collector-wrapper"></a>Definizione di un wrapper dell'agente di raccolta input penna

Il metodo Init della classe CMyInkCollector dichiara e Inizializza un oggetto CMyInkEvents. Viene quindi creato un oggetto [**InkCollector**](inkcollector-class.md) e vengono associati l'agente di raccolta input penna e il gestore eventi. Infine, l'oggetto **InkCollector** viene collegato alla finestra e attivato.


```C++
// Handle all initializaton
HRESULT Init(
HWND hWnd)
{
    // Initialize event sink. This consists of setting
    //  up the free threaded marshaler.
    HRESULT hr = m_InkEvents.Init(hWnd);

    if (FAILED(hr))
        ...

    // Create the ink collector
    hr = CoCreateInstance(CLSID_InkCollector, NULL, CLSCTX_ALL, IID_IInkCollector, (void **) &m_pInkCollector);

    if (FAILED(hr))
        ...

    // Set up connection between Ink Collector and our event sink
    hr = m_InkEvents.AdviseInkCollector(m_pInkCollector);

    if (FAILED(hr))
        ...

    // Attach Ink Collector to window
    hr = m_pInkCollector->put_hWnd((long) hWnd);

    if (FAILED(hr))
        ...

    // Allow Ink Collector to receive input.
    return m_pInkCollector->put_Enabled(VARIANT_TRUE);
}
```



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>Accesso alle interfacce di Tablet PC e alle classi wrapper

Includere innanzitutto le intestazioni per le interfacce di automazione dei Tablet PC. Vengono installate con Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition Development Kit 1,7.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Includere quindi le intestazioni per le classi wrapper e il gestore eventi [**InkCollector**](inkcollector-class.md) definito.


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>Chiamata alle classi wrapper

Quando viene creata la finestra, la procedura finestra Crea un wrapper dell'agente di raccolta input penna e inizializza il wrapper. Quando la finestra viene distrutta, la routine della finestra Elimina il wrapper dell'agente di raccolta dell'input penna. Il wrapper dell'agente di raccolta dell'input penna gestisce la creazione e l'eliminazione del gestore eventi associato.


```C++
case WM_CREATE:

    // Allocate and initialize memory for object
    pmic = new CMyInkCollector();

    if (pmic != NULL)
    {
        // Real initialization. This consists of creating
        //  an ink collector object and attaching it to
        //  the current window. 
        if (SUCCEEDED(pmic->Init(hWnd)))
        {
            return 0;
        }
        
        // Failure free resources.
        delete pmic;
        pmic = NULL;
    }
    
    return -1;
...
case WM_DESTROY:
    // The destructor for the object handles releasing the
    //  InkCollector and disconnecting the InkCollector
    //  from the object's event sink. 
    delete pmic;
    pmic = NULL;
    PostQuitMessage(0);
    break;
```



 

 
