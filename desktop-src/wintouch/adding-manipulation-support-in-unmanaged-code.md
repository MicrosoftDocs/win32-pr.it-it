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
# <a name="adding-manipulation-support-in-unmanaged-code"></a><span data-ttu-id="137bb-113">Aggiunta del supporto per la manipolazione nel codice non gestito</span><span class="sxs-lookup"><span data-stu-id="137bb-113">Adding Manipulation Support in Unmanaged Code</span></span>

<span data-ttu-id="137bb-114">In questa sezione viene illustrato come aggiungere il supporto per la manipolazione a codice non gestito implementando un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="137bb-114">This section explains how to add manipulation support to unmanaged code by implementing an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

<span data-ttu-id="137bb-115">Nell'immagine seguente viene illustrata l'architettura di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-115">The following image outlines the manipulation architecture.</span></span>

![illustrazione che mostra i messaggi di Windows Touch passati al processore di manipolazione di un oggetto, che gestisce gli eventi con l' \- interfaccia IManipulationEvents](images/manipulation-arch.png)

<span data-ttu-id="137bb-117">I dati di tocco ricevuti dai messaggi [**WM \_ touch**](wm-touchdown.md) vengono passati al [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) insieme all'ID contatto dal messaggio di tocco.</span><span class="sxs-lookup"><span data-stu-id="137bb-117">Touch data that is received from [**WM\_TOUCH**](wm-touchdown.md) messages is passed to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) together with the contact ID from the touch message.</span></span> <span data-ttu-id="137bb-118">In base alla sequenza di messaggi, l'interfaccia **IManipulationProcessor** calcolerà il tipo di trasformazione che viene eseguito e i valori associati a questa trasformazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-118">Based on the message sequence, the **IManipulationProcessor** interface will calculate what kind of transformation is being performed and what the values associated with this transformation are.</span></span> <span data-ttu-id="137bb-119">**IManipulationProcessor** genererà [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) che vengono gestite da un sink di evento.</span><span class="sxs-lookup"><span data-stu-id="137bb-119">The **IManipulationProcessor** will then generate [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) which are handled by an event sink.</span></span> <span data-ttu-id="137bb-120">Il sink di evento può quindi utilizzare questi valori per eseguire operazioni personalizzate sull'oggetto trasformato.</span><span class="sxs-lookup"><span data-stu-id="137bb-120">The event sink can then use these values to perform custom operations on the object being transformed.</span></span>

<span data-ttu-id="137bb-121">Per aggiungere il supporto per la manipolazione all'applicazione, è necessario attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="137bb-121">To add manipulation support to your application, you must follow these steps:</span></span>

1.  <span data-ttu-id="137bb-122">Implementare un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="137bb-122">Implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>
2.  <span data-ttu-id="137bb-123">Creare un'istanza di un'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="137bb-123">Create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>
3.  <span data-ttu-id="137bb-124">Creare un'istanza del sink di evento e configurare gli eventi di tocco.</span><span class="sxs-lookup"><span data-stu-id="137bb-124">Create an instance of your event sink and set up touch events.</span></span>
4.  <span data-ttu-id="137bb-125">Inviare i dati dell'evento Touch al processore di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-125">Send touch event data to the manipulation processor.</span></span>

<span data-ttu-id="137bb-126">In questa sezione vengono illustrati i passaggi da seguire per aggiungere il supporto per la modifica all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-126">This section explains the steps that you must follow to add manipulation support to your application.</span></span> <span data-ttu-id="137bb-127">Il codice viene fornito a ogni passaggio per iniziare.</span><span class="sxs-lookup"><span data-stu-id="137bb-127">Code is provided at each step to get you started.</span></span>

> [!Note]  
> <span data-ttu-id="137bb-128">Non è possibile utilizzare le modifiche e i movimenti allo stesso tempo perché i messaggi di movimento e tocco si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="137bb-128">You cannot use manipulations and gestures at the same time because gesture and touch messages are mutually exclusive.</span></span>

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a><span data-ttu-id="137bb-129">Implementare un sink di evento per l' \_ interfaccia IManipualtionEvents</span><span class="sxs-lookup"><span data-stu-id="137bb-129">Implement an Event Sink for \_IManipualtionEvents Interface</span></span>

<span data-ttu-id="137bb-130">Prima di poter creare un'istanza del sink di evento, è necessario creare una classe che implementi l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) per la gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="137bb-130">Before you can create an instance of your event sink, you must create a class that implements the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface for eventing.</span></span> <span data-ttu-id="137bb-131">Si tratta del sink di evento.</span><span class="sxs-lookup"><span data-stu-id="137bb-131">This is your event sink.</span></span> <span data-ttu-id="137bb-132">Gli eventi generati dall'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) vengono gestiti dal sink di evento.</span><span class="sxs-lookup"><span data-stu-id="137bb-132">Events generated by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface are handled by your event sink.</span></span> <span data-ttu-id="137bb-133">Nel codice seguente viene illustrata un'intestazione di esempio per una classe che eredita l'interfaccia **\_ IManipulationEvents** .</span><span class="sxs-lookup"><span data-stu-id="137bb-133">The following code shows an example header for a class that inherits the **\_IManipulationEvents** interface.</span></span>

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

<span data-ttu-id="137bb-134">Data l'intestazione, è necessario creare un'implementazione dell'interfaccia eventi in modo che la classe esegua le azioni che si desidera vengano eseguite dal processore di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-134">Given the header, you must create an implementation of the events interface so that your class performs the actions that you want the manipulation processor to perform.</span></span> <span data-ttu-id="137bb-135">Il codice seguente è un modello che implementa la funzionalità minima di un sink di evento per l'interfaccia [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="137bb-135">The following code is a template that implements the minimum functionality of an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

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

<span data-ttu-id="137bb-136">Prestare particolare attenzione alle implementazioni dei metodi [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) nella classe.</span><span class="sxs-lookup"><span data-stu-id="137bb-136">Pay extra attention to implementations of [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) methods in the class.</span></span> <span data-ttu-id="137bb-137">Questi sono i metodi più probabili nell'interfaccia che richiedono l'esecuzione di operazioni in base alle informazioni di manipolazione passate nell'evento.</span><span class="sxs-lookup"><span data-stu-id="137bb-137">These are the most likely methods in the interface that will require you to perform operations based on the manipulation information that is passed around in the event.</span></span> <span data-ttu-id="137bb-138">Si noti inoltre che il secondo parametro del costruttore è l'oggetto utilizzato nelle manipolazioni degli eventi.</span><span class="sxs-lookup"><span data-stu-id="137bb-138">Note also that the second parameter in the constructor is the object that is used in the event manipulations.</span></span> <span data-ttu-id="137bb-139">Nel codice usato per produrre l'esempio, hWnd per l'applicazione viene inviato al costruttore in modo che possa essere riposizionato e ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="137bb-139">In the code used for producing the sample, the hWnd for the application is sent to the constructor so that it can be repositioned and resized.</span></span>

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a><span data-ttu-id="137bb-140">Creare un'istanza di un'interfaccia IManipulationProcessor</span><span class="sxs-lookup"><span data-stu-id="137bb-140">Create an instance of an IManipulationProcessor Interface</span></span>

<span data-ttu-id="137bb-141">Nel codice in cui si utilizzeranno le modifiche, è necessario creare un'istanza di un'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="137bb-141">In the code where you will use manipulations, you must create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="137bb-142">Per prima cosa, è necessario aggiungere il supporto per la classe Manipulation.</span><span class="sxs-lookup"><span data-stu-id="137bb-142">First you must add support for the manipulations class.</span></span> <span data-ttu-id="137bb-143">Il codice seguente illustra come è possibile eseguire questa operazione nella classe.</span><span class="sxs-lookup"><span data-stu-id="137bb-143">The following code shows how you can do this in your class.</span></span>

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

<span data-ttu-id="137bb-144">Quando si dispone della variabile per il processore di manipolazione e sono state incluse le intestazioni per le modifiche, è necessario creare un'istanza dell'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="137bb-144">After you have your variable for the manipulation processor and you have included the headers for manipulations, you have to create an instance of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="137bb-145">Si tratta di un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="137bb-145">This is a COM object.</span></span> <span data-ttu-id="137bb-146">Pertanto, è necessario chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), quindi creare un'istanza del riferimento a **IManipulationProcessor**.</span><span class="sxs-lookup"><span data-stu-id="137bb-146">Therefore, you must call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), and then create an instance of your reference to the **IManipulationProcessor**.</span></span> <span data-ttu-id="137bb-147">Nel codice seguente viene illustrato come è possibile creare un'istanza di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="137bb-147">The following code shows how you can create an instance of this interface.</span></span>

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a><span data-ttu-id="137bb-148">Creare un'istanza del sink di evento e configurare gli eventi di tocco</span><span class="sxs-lookup"><span data-stu-id="137bb-148">Create an instance of your Event Sink and set up Touch Events</span></span>

<span data-ttu-id="137bb-149">Includere la definizione per la classe sink di evento nel codice e quindi aggiungere una variabile per la classe sink dell'evento di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-149">Include the definition for your event sink class to your code and then add a variable for the manipulation event sink class.</span></span> <span data-ttu-id="137bb-150">Nell'esempio di codice seguente è inclusa l'intestazione per l'implementazione della classe e viene impostata una variabile globale per archiviare il sink di evento.</span><span class="sxs-lookup"><span data-stu-id="137bb-150">The following code example includes the header for the class implementation and sets up a global variable to store the event sink.</span></span>

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

<span data-ttu-id="137bb-151">Dopo aver creato la variabile e avere incluso la definizione per la nuova classe sink di evento, è possibile creare la classe usando il processore di manipolazione configurato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="137bb-151">After you have the variable and have included your definition for the new event sink class, you can construct the class by using the manipulation processor that you have set up in the previous step.</span></span> <span data-ttu-id="137bb-152">Il codice seguente illustra come creare un'istanza di questa classe da **OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="137bb-152">The following code shows how an instance of this class would be created from **OnInitDialog**.</span></span>

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> <span data-ttu-id="137bb-153">La modalità di creazione di un'istanza del sink di evento dipende da ciò che si sta eseguendo con i dati di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-153">The way that you create an instance of your event sink depends on what you are doing with the manipulation data.</span></span> <span data-ttu-id="137bb-154">Nella maggior parte dei casi, si creerà un sink di evento del processore di manipolazione che non ha lo stesso costruttore di questo esempio.</span><span class="sxs-lookup"><span data-stu-id="137bb-154">In most cases, you will create a manipulation processor event sink that does not have the same constructor as this example.</span></span>

### <a name="send-touch-event-data-to-the-manipulation-processor"></a><span data-ttu-id="137bb-155">Inviare i dati dell'evento Touch al processore di manipolazione</span><span class="sxs-lookup"><span data-stu-id="137bb-155">Send Touch Event Data to the Manipulation Processor</span></span>

<span data-ttu-id="137bb-156">Ora che il processore di manipolazione e il sink di evento sono stati impostati, è necessario inviare i dati di tocco al processore di manipolazione per attivare gli eventi di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-156">Now that you have your manipulation processor and event sink set up, you must feed touch data to the manipulation processor to trigger manipulation events.</span></span>

> [!Note]  
> <span data-ttu-id="137bb-157">Si tratta della stessa procedura descritta in [Introduzione con i messaggi di Windows Touch](getting-started-with-multi-touch-messages.md).</span><span class="sxs-lookup"><span data-stu-id="137bb-157">This is the same procedure as discussed in [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md).</span></span>

<span data-ttu-id="137bb-158">Innanzitutto, si creerà del codice per decodificare i messaggi [**WM \_ touch**](wm-touchdown.md) e inviarli all'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) per generare eventi.</span><span class="sxs-lookup"><span data-stu-id="137bb-158">First, you will create some code to decode the [**WM\_TOUCH**](wm-touchdown.md) messages and send them to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface to raise events.</span></span> <span data-ttu-id="137bb-159">Nel codice seguente viene illustrata un'implementazione di esempio chiamata dal metodo **WndProc** e viene restituito un **LRESULT** per la messaggistica.</span><span class="sxs-lookup"><span data-stu-id="137bb-159">The following code shows an example implementation that is called from the **WndProc** method and return an **LRESULT** for messaging.</span></span>

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

<span data-ttu-id="137bb-160">Ora che è disponibile un metodo di utilità per la decodifica del messaggio [**WM \_ touch**](wm-touchdown.md) , è necessario passare i messaggi **WM \_ touch** alla funzione di utilità dal metodo **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="137bb-160">Now that you have a utility method for decoding the [**WM\_TOUCH**](wm-touchdown.md) message, you must pass the **WM\_TOUCH** messages to the utility function from your **WndProc** method.</span></span> <span data-ttu-id="137bb-161">Il codice seguente illustra come è possibile eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="137bb-161">The following code shows how you can do this.</span></span>

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

<span data-ttu-id="137bb-162">I metodi personalizzati implementati nel sink di evento dovrebbero ora funzionare.</span><span class="sxs-lookup"><span data-stu-id="137bb-162">The custom methods that you have implemented in your event sink should now work.</span></span> <span data-ttu-id="137bb-163">In questo esempio, il tocco della finestra lo sposta.</span><span class="sxs-lookup"><span data-stu-id="137bb-163">In this example, touching the window will move it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="137bb-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="137bb-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="137bb-165">Modifiche</span><span class="sxs-lookup"><span data-stu-id="137bb-165">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>


 