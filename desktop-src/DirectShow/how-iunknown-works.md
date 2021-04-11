---
description: Funzionamento di IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Funzionamento di IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123456"
---
# <a name="how-iunknown-works"></a><span data-ttu-id="a8175-103">Funzionamento di IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8175-103">How IUnknown Works</span></span>

<span data-ttu-id="a8175-104">I metodi in **IUnknown** consentono a un'applicazione di eseguire una query per le interfacce del componente e di gestire il conteggio dei riferimenti del componente.</span><span class="sxs-lookup"><span data-stu-id="a8175-104">The methods in **IUnknown** enable an application to query for interfaces on the component and manage the component's reference count.</span></span>

<span data-ttu-id="a8175-105">**Conteggio riferimenti**</span><span class="sxs-lookup"><span data-stu-id="a8175-105">**Reference Count**</span></span>

<span data-ttu-id="a8175-106">Il conteggio dei riferimenti è una variabile interna, incrementata nel metodo **AddRef** e decrementata nel metodo di **rilascio** .</span><span class="sxs-lookup"><span data-stu-id="a8175-106">The reference count is an internal variable, incremented in the **AddRef** method and decremented in the **Release** method.</span></span> <span data-ttu-id="a8175-107">Le classi base gestiscono il conteggio dei riferimenti e sincronizzano l'accesso al conteggio dei riferimenti tra più thread.</span><span class="sxs-lookup"><span data-stu-id="a8175-107">The base classes manage the reference count and synchronize access to the reference count among multiple threads.</span></span>

<span data-ttu-id="a8175-108">**Query di interfaccia**</span><span class="sxs-lookup"><span data-stu-id="a8175-108">**Interface Queries**</span></span>

<span data-ttu-id="a8175-109">Anche l'esecuzione di query per un'interfaccia è semplice.</span><span class="sxs-lookup"><span data-stu-id="a8175-109">Querying for an interface is also straightforward.</span></span> <span data-ttu-id="a8175-110">Il chiamante passa due parametri: un identificatore di interfaccia (IID) e l'indirizzo di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="a8175-110">The caller passes two parameters: an interface identifier (IID), and the address of a pointer.</span></span> <span data-ttu-id="a8175-111">Se il componente supporta l'interfaccia richiesta, imposta il puntatore sull'interfaccia, incrementa il proprio conteggio dei riferimenti e restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8175-111">If the component supports the requested interface, it sets the pointer to the interface, increments its own reference count, and returns S\_OK.</span></span> <span data-ttu-id="a8175-112">In caso contrario, imposta il puntatore su **null** E restituisce e \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="a8175-112">Otherwise, it sets the pointer to **NULL** and returns E\_NOINTERFACE.</span></span> <span data-ttu-id="a8175-113">Nello pseudocodice seguente viene illustrato il contorno generale del metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="a8175-113">The following pseudocode shows the general outline of the **QueryInterface** method.</span></span> <span data-ttu-id="a8175-114">L'aggregazione di componenti, descritta nella sezione successiva, introduce alcune complessità aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="a8175-114">Component aggregation, described in the next section, introduces some additional complexity.</span></span>


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



<span data-ttu-id="a8175-115">L'unica differenza tra il metodo **QueryInterface** di un componente e il metodo **QueryInterface** di un altro è l'elenco di IID testati da ogni componente.</span><span class="sxs-lookup"><span data-stu-id="a8175-115">The only difference between the **QueryInterface** method of one component and the **QueryInterface** method of another is the list of IIDs that each component tests.</span></span> <span data-ttu-id="a8175-116">Per ogni interfaccia supportata dal componente, il componente deve verificare l'IID di tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a8175-116">For every interface that the component supports, the component must test for the IID of that interface.</span></span>

<span data-ttu-id="a8175-117">**Aggregazione e delega**</span><span class="sxs-lookup"><span data-stu-id="a8175-117">**Aggregation and Delegation**</span></span>

<span data-ttu-id="a8175-118">L'aggregazione del componente deve essere trasparente per il chiamante.</span><span class="sxs-lookup"><span data-stu-id="a8175-118">Component aggregation must be transparent to the caller.</span></span> <span data-ttu-id="a8175-119">L'aggregazione deve pertanto esporre una singola interfaccia **IUnknown** , con il componente aggregato che fa riferimento all'implementazione del componente esterno.</span><span class="sxs-lookup"><span data-stu-id="a8175-119">Therefore, the aggregate must expose a single **IUnknown** interface, with the aggregated component deferring to the outer component's implementation.</span></span> <span data-ttu-id="a8175-120">In caso contrario, il chiamante vedrà due interfacce **IUnknown** diverse nella stessa aggregazione.</span><span class="sxs-lookup"><span data-stu-id="a8175-120">Otherwise, the caller would see two different **IUnknown** interfaces in the same aggregate.</span></span> <span data-ttu-id="a8175-121">Se il componente non è aggregato, viene utilizzata una propria implementazione.</span><span class="sxs-lookup"><span data-stu-id="a8175-121">If the component is not aggregated, it uses its own implementation.</span></span>

<span data-ttu-id="a8175-122">Per supportare questo comportamento, il componente deve aggiungere un livello di riferimento indiretto.</span><span class="sxs-lookup"><span data-stu-id="a8175-122">To support this behavior, the component must add a level of indirection.</span></span> <span data-ttu-id="a8175-123">Un *IUnknown* delegante delega il lavoro al posto appropriato: al componente esterno, se presente, o alla versione interna del componente.</span><span class="sxs-lookup"><span data-stu-id="a8175-123">A *delegating IUnknown* delegates the work to the appropriate place: to the outer component, if there is one, or to the component's internal version.</span></span> <span data-ttu-id="a8175-124">Un *IUnknown non delegante* esegue l'operazione, come descritto nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="a8175-124">A *nondelegating IUnknown* does the work, as described in the previous section.</span></span>

<span data-ttu-id="a8175-125">La versione di delega è Public e mantiene il nome **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a8175-125">The delegating version is public and keeps the name **IUnknown**.</span></span> <span data-ttu-id="a8175-126">La versione non delegante viene rinominata [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a8175-126">The nondelegating version is renamed [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="a8175-127">Questo nome non fa parte della specifica COM, perché non è un'interfaccia pubblica.</span><span class="sxs-lookup"><span data-stu-id="a8175-127">This name is not part of the COM specification, because it is not a public interface.</span></span>

<span data-ttu-id="a8175-128">Quando il client crea un'istanza del componente, chiama il metodo **IClassFactory:: CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="a8175-128">When the client creates an instance of the component, it calls the **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="a8175-129">Un parametro è un puntatore all'interfaccia **IUnknown** del componente di aggregazione o **null** se la nuova istanza non è aggregata.</span><span class="sxs-lookup"><span data-stu-id="a8175-129">One parameter is a pointer to the aggregating component's **IUnknown** interface, or **NULL** if the new instance is not aggregated.</span></span> <span data-ttu-id="a8175-130">Il componente usa questo parametro per archiviare una variabile membro che indica l'interfaccia **IUnknown** da usare, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="a8175-130">The component uses this parameter to store a member variable indicating which **IUnknown** interface to use, as shown in the following example:</span></span>


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



<span data-ttu-id="a8175-131">Ogni metodo nell' **IUnknown** delegante chiama la rispettiva controparte non delegante, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="a8175-131">Each method in the delegating **IUnknown** calls its nondelegating counterpart, as shown in the following example:</span></span>


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



<span data-ttu-id="a8175-132">Per la natura della delega, i metodi di delega hanno un aspetto identico in ogni componente.</span><span class="sxs-lookup"><span data-stu-id="a8175-132">By the nature of delegation, the delegating methods look identical in every component.</span></span> <span data-ttu-id="a8175-133">Vengono modificate solo le versioni non deleganti.</span><span class="sxs-lookup"><span data-stu-id="a8175-133">Only the nondelegating versions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8175-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8175-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8175-135">Come implementare IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8175-135">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



