---
title: Gestione degli eventi in C++
description: Gestione degli eventi in C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- Modello a oggetti di Windows Media Player, C++
- modello a oggetti, C++
- Windows Media Player Mobile, C++
- Controllo ActiveX di Windows Media Player, C++
- Controllo ActiveX Windows Media Player Mobile, C++
- Controllo ActiveX, C++
- Incorporamento del programma C++
- incorporamento, programmi C++
- Controllo ActiveX Windows Media Player, gestione eventi
- Controllo ActiveX Windows Media Player Mobile, gestione eventi
- Controllo ActiveX, gestione eventi
- eventi, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116861"
---
# <a name="handling-events-in-c"></a><span data-ttu-id="31549-116">Gestione degli eventi in C++</span><span class="sxs-lookup"><span data-stu-id="31549-116">Handling Events in C++</span></span>

<span data-ttu-id="31549-117">È possibile ricevere eventi da Windows Media Player in due modi.</span><span class="sxs-lookup"><span data-stu-id="31549-117">You can receive events from Windows Media Player in two ways.</span></span>

-   <span data-ttu-id="31549-118">Tramite **IDispatch** usando l'interfaccia **\_ WMPOCXEvents** .</span><span class="sxs-lookup"><span data-stu-id="31549-118">Through **IDispatch** by using the **\_WMPOCXEvents** interface.</span></span> <span data-ttu-id="31549-119">Si tratta dell'interfaccia da utilizzare per la maggior parte degli scenari di incorporamento.</span><span class="sxs-lookup"><span data-stu-id="31549-119">This is the interface to use for most embedding scenarios.</span></span>
-   <span data-ttu-id="31549-120">Tramite l'interfaccia **IWMPEvents** .</span><span class="sxs-lookup"><span data-stu-id="31549-120">Through the **IWMPEvents** interface.</span></span> <span data-ttu-id="31549-121">Questa interfaccia è disponibile quando il codice è connesso al lettore in modalità completa, ad esempio quando si esegue la comunicazione remota del controllo Media Player Windows o in un plug-in dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="31549-121">This interface is available when your code is connected to the full mode Player, such as when remoting the Windows Media Player control or in a UI plug-in.</span></span>

<span data-ttu-id="31549-122">In ogni scenario si inizia ad ascoltare gli eventi usando i punti di connessione COM.</span><span class="sxs-lookup"><span data-stu-id="31549-122">In each scenario, you start listening to events by using COM connection points.</span></span>

<span data-ttu-id="31549-123">Il codice di esempio seguente usa tre variabili membro:</span><span class="sxs-lookup"><span data-stu-id="31549-123">The following example code uses three member variables:</span></span>


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



<span data-ttu-id="31549-124">Per recuperare un punto di connessione, è necessario innanzitutto **QueryInterface** per il contenitore del punto di connessione.</span><span class="sxs-lookup"><span data-stu-id="31549-124">To retrieve a connection point, you first **QueryInterface** for the connection point container.</span></span>


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



<span data-ttu-id="31549-125">Successivamente, richiedere il punto di connessione per l'interfaccia evento che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="31549-125">Next, request the connection point for the event interface you want to use.</span></span> <span data-ttu-id="31549-126">Il codice di esempio seguente tenta prima di usare **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="31549-126">The following example code first attempts to use **IWMPEvents**.</span></span> <span data-ttu-id="31549-127">Se l'interfaccia non è disponibile, viene usato **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="31549-127">If that interface isn't available, it uses **\_WMPOCXEvents**.</span></span>


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



<span data-ttu-id="31549-128">Infine, chiamare **IConnectionPoint:: Advise** per richiedere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="31549-128">Finally, call **IConnectionPoint::Advise** to request events.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



<span data-ttu-id="31549-129">Nell'esempio precedente, il primo parametro presuppone che la classe chiamante implementi sia **IWMPEvents** che **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="31549-129">In the preceding example, the first parameter assumes that the calling class implements both **IWMPEvents** and **\_WMPOCXEvents**.</span></span> <span data-ttu-id="31549-130">Il secondo parametro è un valore restituito che viene usato per arrestare l'ascolto degli eventi, ad esempio quando il programma viene chiuso, usando un codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="31549-130">The second parameter is a return value that you use to stop listening to events, such as when your program exits, using code similar to the following:</span></span>


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



<span data-ttu-id="31549-131">L'implementazione dei gestori eventi per **IWMPEvents** e **\_ WMPOCXEvents** è diversa.</span><span class="sxs-lookup"><span data-stu-id="31549-131">Implementing the event handlers for **IWMPEvents** and **\_WMPOCXEvents** differs.</span></span> <span data-ttu-id="31549-132">Per **IWMPEvents**, è necessario implementare una funzione per gestire ogni evento definito dall'interfaccia, anche se non si intende usare l'evento.</span><span class="sxs-lookup"><span data-stu-id="31549-132">For **IWMPEvents**, you must implement a function to handle every event defined by the interface, even if you don't intend to use the event.</span></span>


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



<span data-ttu-id="31549-133">Per implementare i gestori **\_ WMPOCXEvents** , è necessario usare **IDispatch:: Invoke**, ovvero un'unica implementazione del gestore eventi per tutti gli eventi che si verificano nell'interfaccia **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="31549-133">To implement **\_WMPOCXEvents** handlers, you must use **IDispatch::Invoke**, which is a single event handler implementation for all the events happening on the **IDispatch** interface.</span></span> <span data-ttu-id="31549-134">Ciò significa che è possibile scegliere di gestire solo determinati eventi e ignorarne altri.</span><span class="sxs-lookup"><span data-stu-id="31549-134">This means that you can choose to handle only certain events and ignore others.</span></span> <span data-ttu-id="31549-135">Il codice di esempio seguente mostra un gestore **\_ WMPOCXEvents** , che usa **Invoke**, che gestisce solo gli eventi **OpenStateChange** e **PlayStateChange** :</span><span class="sxs-lookup"><span data-stu-id="31549-135">The following example code shows a **\_WMPOCXEvents** handler, using **Invoke**, that handles only the **OpenStateChange** and **PlayStateChange** events:</span></span>


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



<span data-ttu-id="31549-136">Nel codice di esempio precedente, ogni case esegue semplicemente chiamate al gestore **IWMPEvents** per l'evento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="31549-136">In the preceding example code, each case simply calls through to the **IWMPEvents** handler for the corresponding event.</span></span> <span data-ttu-id="31549-137">Se il codice gestisce solo **\_ WMPOCXEvents**, è possibile chiamare semplicemente una funzione personalizzata o gestire l'evento inline dopo l'istruzione **case** .</span><span class="sxs-lookup"><span data-stu-id="31549-137">If your code only handles **\_WMPOCXEvents**, you can simply call a custom function or handle the event inline after the **case** statement.</span></span>

## <a name="receiving-events-from-windows-media-player-10-mobile"></a><span data-ttu-id="31549-138">Ricezione di eventi da Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="31549-138">Receiving Events from Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="31549-139">Il controllo Windows Media Player 10 Mobile supporta solo la ricezione di determinati eventi tramite **\_ WMPOCXEvents** e **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="31549-139">The Windows Media Player 10 Mobile control only supports receiving certain events through **\_WMPOCXEvents** and **IWMPEvents**.</span></span> <span data-ttu-id="31549-140">Per ulteriori informazioni, vedere la documentazione relativa a **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="31549-140">For more information, please see the documentation for **IWMPEvents**.</span></span>

## <a name="samples"></a><span data-ttu-id="31549-141">Esempi</span><span class="sxs-lookup"><span data-stu-id="31549-141">Samples</span></span>

<span data-ttu-id="31549-142">Il pacchetto di installazione di Windows Media Player installa un esempio che illustra la gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="31549-142">The Windows Media Player setup package installs a sample that demonstrates event handling.</span></span> <span data-ttu-id="31549-143">Per ulteriori informazioni, vedere l'esempio WMPHost.</span><span class="sxs-lookup"><span data-stu-id="31549-143">See the WMPHost sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31549-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31549-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31549-145">**Esempi**</span><span class="sxs-lookup"><span data-stu-id="31549-145">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="31549-146">**Uso del controllo Media Player di Windows in un programma C++**</span><span class="sxs-lookup"><span data-stu-id="31549-146">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




