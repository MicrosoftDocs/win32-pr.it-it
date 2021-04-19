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
# <a name="c-event-sinks-sample"></a><span data-ttu-id="fc35f-105">Esempio di sink di evento C++</span><span class="sxs-lookup"><span data-stu-id="fc35f-105">C++ Event Sinks Sample</span></span>

<span data-ttu-id="fc35f-106">Questo programma illustra come creare un'applicazione che acquisisce gli eventi InkCollector usando solo C++.</span><span class="sxs-lookup"><span data-stu-id="fc35f-106">This program demonstrates how you can build an application that captures InkCollector events using only C++.</span></span> <span data-ttu-id="fc35f-107">Questo programma crea un oggetto [**InkCollector**](inkcollector-class.md) per abilitare l'input penna nella finestra.</span><span class="sxs-lookup"><span data-stu-id="fc35f-107">This program co-creates an [**InkCollector**](inkcollector-class.md) object to ink -enable the window.</span></span> <span data-ttu-id="fc35f-108">Viene visualizzata una finestra di messaggio ogni volta che viene ricevuto un evento [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="fc35f-108">It displays a message box whenever a [**Stroke**](inkcollector-stroke.md) event is received.</span></span>

## <a name="defining-a-wrapper-for-ink-collector-events"></a><span data-ttu-id="fc35f-109">Definizione di un wrapper per eventi dell'agente di raccolta input penna</span><span class="sxs-lookup"><span data-stu-id="fc35f-109">Defining a Wrapper for Ink Collector Events</span></span>

<span data-ttu-id="fc35f-110">La `InkCollectorEvents` classe gestisce il passaggio degli eventi dell'agente di raccolta input penna dall'agente di raccolta input penna all'utente di questa classe.</span><span class="sxs-lookup"><span data-stu-id="fc35f-110">The `InkCollectorEvents` Class handles passing ink collector events from the ink collector to the user of this class.</span></span> <span data-ttu-id="fc35f-111">Il `AdviseInkCollector` metodo configura la connessione tra l'oggetto [**InkCollector**](inkcollector-class.md) e questa classe.</span><span class="sxs-lookup"><span data-stu-id="fc35f-111">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="fc35f-112">Il `Invoke` metodo converte la notifica degli eventi [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in una chiamata a una funzione virtuale che può essere sostituita dall'utente di questa classe per elaborare un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="fc35f-112">The `Invoke` method converts the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) event notification into a call to a virtual function that the user of this class can override to process a particular event.</span></span>

> [!Note]  
> <span data-ttu-id="fc35f-113">Per ottenere tale evento, è necessario eseguire l'override della funzione virtuale per un gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="fc35f-113">You must do more than override the virtual function for an event handler to get that event.</span></span> <span data-ttu-id="fc35f-114">Per tutti gli eventi, tranne quelli predefiniti, è necessario chiamare il metodo [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) dell'agente di raccolta input penna per garantire l'ottenimento di un evento.</span><span class="sxs-lookup"><span data-stu-id="fc35f-114">For all but default events, you have to call the ink collector's [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) method to guarantee getting an event.</span></span> <span data-ttu-id="fc35f-115">In secondo luogo, questo oggetto esegue il marshalling di se stesso, in modo che tutti i gestori eventi implementati debbano essere anche a thread libero.</span><span class="sxs-lookup"><span data-stu-id="fc35f-115">Secondly, this object marshals itself free threaded so all implemented event handlers need to be free threaded as well.</span></span> <span data-ttu-id="fc35f-116">Di particolare importanza è l'uso delle API di Windows, che può causare un passaggio a un altro thread perché non è garantito che il gestore eventi sia in esecuzione nello stesso thread della finestra connessa con l'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="fc35f-116">Of particular importance is using Windows APIs, which may cause a switch to another thread as the event handler is not guaranteed to be running on the same thread as the window connected with the ink collector.</span></span>

 


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



<span data-ttu-id="fc35f-117">Il `Init` metodo chiama [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) per configurare un gestore di marshalling a thread libero.</span><span class="sxs-lookup"><span data-stu-id="fc35f-117">The `Init` method calls [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) to set up a free threaded marshaler.</span></span>


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



<span data-ttu-id="fc35f-118">Il `AdviseInkCollector` metodo configura la connessione tra l'oggetto [**InkCollector**](inkcollector-class.md) e questa classe.</span><span class="sxs-lookup"><span data-stu-id="fc35f-118">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="fc35f-119">Viene innanzitutto recuperato un punto di connessione all'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="fc35f-119">It first retrieves a connection point to the ink collector.</span></span> <span data-ttu-id="fc35f-120">Viene quindi recuperato un puntatore a in `IInkCollectorEvents` modo che sia possibile stabilire una connessione consultiva al controllo.</span><span class="sxs-lookup"><span data-stu-id="fc35f-120">Then it retrieves a pointer to the `IInkCollectorEvents` so that it may establish an advisory connection to the control.</span></span>


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



<span data-ttu-id="fc35f-121">Il `UnadviseInkCollector` metodo rilascia le connessioni che l'oggetto ha al controllo.</span><span class="sxs-lookup"><span data-stu-id="fc35f-121">The `UnadviseInkCollector` method releases the connections the object has to the control.</span></span>


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a><span data-ttu-id="fc35f-122">Definizione di un gestore eventi dell'agente di raccolta input penna</span><span class="sxs-lookup"><span data-stu-id="fc35f-122">Defining an Ink Collector Events Handler</span></span>

<span data-ttu-id="fc35f-123">La classe CMyInkEvents esegue l'override del comportamento predefinito del gestore dell'evento [**Stroke**](inkcollector-stroke.md) della classe InkCollectorEvents.</span><span class="sxs-lookup"><span data-stu-id="fc35f-123">The CMyInkEvents Class overrides the default behavior of the [**Stroke**](inkcollector-stroke.md) event handler of the InkCollectorEvents Class.</span></span> <span data-ttu-id="fc35f-124">Il metodo Stroke Visualizza una finestra di messaggio quando l'oggetto [**InkCollector**](inkcollector-class.md) riceve un evento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="fc35f-124">The Stroke method displays a message box when the [**InkCollector**](inkcollector-class.md) receives a **Stroke** event.</span></span>


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



## <a name="defining-an-ink-collector-wrapper"></a><span data-ttu-id="fc35f-125">Definizione di un wrapper dell'agente di raccolta input penna</span><span class="sxs-lookup"><span data-stu-id="fc35f-125">Defining an Ink Collector Wrapper</span></span>

<span data-ttu-id="fc35f-126">Il metodo Init della classe CMyInkCollector dichiara e Inizializza un oggetto CMyInkEvents.</span><span class="sxs-lookup"><span data-stu-id="fc35f-126">The CMyInkCollector Class's Init method declares and initializes a CMyInkEvents object.</span></span> <span data-ttu-id="fc35f-127">Viene quindi creato un oggetto [**InkCollector**](inkcollector-class.md) e vengono associati l'agente di raccolta input penna e il gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="fc35f-127">It then creates an [**InkCollector**](inkcollector-class.md) object and associates the ink collector and the event handler.</span></span> <span data-ttu-id="fc35f-128">Infine, l'oggetto **InkCollector** viene collegato alla finestra e attivato.</span><span class="sxs-lookup"><span data-stu-id="fc35f-128">Finally, the **InkCollector** is attached to the window and enabled.</span></span>


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a><span data-ttu-id="fc35f-129">Accesso alle interfacce di Tablet PC e alle classi wrapper</span><span class="sxs-lookup"><span data-stu-id="fc35f-129">Accessing the Tablet PC Interfaces and the Wrapper Classes</span></span>

<span data-ttu-id="fc35f-130">Includere innanzitutto le intestazioni per le interfacce di automazione dei Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="fc35f-130">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="fc35f-131">Vengono installate con Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition Development Kit 1,7.</span><span class="sxs-lookup"><span data-stu-id="fc35f-131">These are installed with the Microsoft<entity type="reg"/> Windows<entity type="reg"/> XP Tablet PC Edition Development Kit 1.7.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="fc35f-132">Includere quindi le intestazioni per le classi wrapper e il gestore eventi [**InkCollector**](inkcollector-class.md) definito.</span><span class="sxs-lookup"><span data-stu-id="fc35f-132">Then, include the headers for the wrapper classes and [**InkCollector**](inkcollector-class.md) event handler was defined.</span></span>


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a><span data-ttu-id="fc35f-133">Chiamata alle classi wrapper</span><span class="sxs-lookup"><span data-stu-id="fc35f-133">Calling the Wrapper Classes</span></span>

<span data-ttu-id="fc35f-134">Quando viene creata la finestra, la procedura finestra Crea un wrapper dell'agente di raccolta input penna e inizializza il wrapper.</span><span class="sxs-lookup"><span data-stu-id="fc35f-134">When the window is created, the Window procedure creates an ink collector wrapper and initializes the wrapper.</span></span> <span data-ttu-id="fc35f-135">Quando la finestra viene distrutta, la routine della finestra Elimina il wrapper dell'agente di raccolta dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="fc35f-135">When the window is destroyed, the Window procedure deletes the ink collector wrapper.</span></span> <span data-ttu-id="fc35f-136">Il wrapper dell'agente di raccolta dell'input penna gestisce la creazione e l'eliminazione del gestore eventi associato.</span><span class="sxs-lookup"><span data-stu-id="fc35f-136">The ink collector wrapper handles the creation and deletion of its associated event handler.</span></span>


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



 

 
