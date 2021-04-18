---
description: Questo argomento descrive come implementare la registrazione degli errori nei servizi di modifica DirectShow.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Creazione di una classe di registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304321"
---
# <a name="creating-an-error-logging-class"></a><span data-ttu-id="dab77-103">Creazione di una classe di registrazione degli errori</span><span class="sxs-lookup"><span data-stu-id="dab77-103">Creating an Error Logging Class</span></span>

<span data-ttu-id="dab77-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="dab77-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dab77-105">Questo argomento descrive come implementare la registrazione degli errori nei [servizi di modifica DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="dab77-105">This topic describes how to implement error logging in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="dab77-106">Dichiarare prima di tutto una classe che implementerà la registrazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="dab77-106">First, declare a class that will implement error logging.</span></span> <span data-ttu-id="dab77-107">La classe eredita l'interfaccia [**IAMErrorLog**](iamerrorlog.md) .</span><span class="sxs-lookup"><span data-stu-id="dab77-107">The class inherits the [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="dab77-108">Contiene le dichiarazioni per i tre metodi **IUnknown** e per il singolo metodo in [IAMErrorLog](implementing-iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="dab77-108">It contains declarations for the three **IUnknown** methods, and for the single method in [IAMErrorLog](implementing-iamerrorlog.md).</span></span> <span data-ttu-id="dab77-109">La dichiarazione di classe è la seguente:</span><span class="sxs-lookup"><span data-stu-id="dab77-109">The class declaration is as follows:</span></span>


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



<span data-ttu-id="dab77-110">L'unica variabile membro nella classe è m \_ lRef, che include il conteggio dei riferimenti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dab77-110">The only member variable in the class is m\_lRef, which holds the object's reference count.</span></span>

<span data-ttu-id="dab77-111">Definire quindi i metodi in **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="dab77-111">Next, define the methods in **IUnknown**.</span></span> <span data-ttu-id="dab77-112">Nell'esempio seguente viene illustrata un'implementazione standard per questi metodi:</span><span class="sxs-lookup"><span data-stu-id="dab77-112">The following example shows a standard implementation for these methods:</span></span>


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



<span data-ttu-id="dab77-113">Con il Framework COM sul posto, è ora possibile implementare l'interfaccia **IAMErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="dab77-113">With the COM framework in place, you can now implement the **IAMErrorLog** interface.</span></span> <span data-ttu-id="dab77-114">La sezione successiva descrive come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="dab77-114">The next section describes how to do this.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dab77-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dab77-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab77-116">Errori di registrazione</span><span class="sxs-lookup"><span data-stu-id="dab77-116">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



