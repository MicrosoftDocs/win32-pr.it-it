---
title: Uso di DXCore per enumerare gli adapter
description: Vengono esaminate le principali funzionalità di DXCore con alcuni esempi di codice, nonché un elenco completo di codice sorgente di un'applicazione DXCore minima.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: f1c21971f2daea69de1f317d1db8eceb9ec00118
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299816"
---
# <a name="using-dxcore-to-enumerate-adapters"></a><span data-ttu-id="b3efd-103">Uso di DXCore per enumerare gli adapter</span><span class="sxs-lookup"><span data-stu-id="b3efd-103">Using DXCore to enumerate adapters</span></span>

<span data-ttu-id="b3efd-104">DXCore è un'API di enumerazione degli adapter per i dispositivi DirectX, quindi alcune delle sue funzionalità si sovrappongono a quelle di [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="b3efd-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

<span data-ttu-id="b3efd-105">DXCore consente l'esposizione dei nuovi tipi di dispositivo alla modalità utente, ad esempio MCDM (modello di driver di calcolo Microsoft), per l'uso con [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)e [Windows Machine Learning](/windows/ai/windows-ml/).</span><span class="sxs-lookup"><span data-stu-id="b3efd-105">DXCore enables the exposure of new device types to user mode, such as MCDM (Microsoft Compute Driver Model), for use with [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md), and [Windows Machine Learning](/windows/ai/windows-ml/).</span></span> <span data-ttu-id="b3efd-106">DXCore, a differenza di DXGI, non fornisce informazioni sulla tecnologia o sulle proprietà correlate alla visualizzazione</span><span class="sxs-lookup"><span data-stu-id="b3efd-106">DXCore, unlike DXGI, does not provide any information about display-related technology or properties</span></span>

<span data-ttu-id="b3efd-107">Nelle prossime sezioni verranno esaminate le principali funzionalità di DXCore con alcuni esempi di codice (scritti in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span><span class="sxs-lookup"><span data-stu-id="b3efd-107">In the next few sections, we'll take a look at the main features of DXCore with some code examples (written in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span></span> <span data-ttu-id="b3efd-108">Gli esempi di codice illustrati di seguito sono estratti dal listato di codice sorgente completo che è possibile trovare nell'argomento [applicazione DXCore minima](dxcore-source-code.md).</span><span class="sxs-lookup"><span data-stu-id="b3efd-108">The code examples shown below are extracted from the full source code listing that you can find in the topic [Minimal DXCore application](dxcore-source-code.md).</span></span>

## <a name="create-an-adapter-factory"></a><span data-ttu-id="b3efd-109">Creare una factory di adapter</span><span class="sxs-lookup"><span data-stu-id="b3efd-109">Create an adapter factory</span></span>

<span data-ttu-id="b3efd-110">Per iniziare l'enumerazione degli adapter di DXCore, è necessario creare un oggetto factory di adapter, rappresentato dall'interfaccia [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="b3efd-110">You begin DXCore adapter enumeration by creating an adapter factory object, which is represented by the [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span> <span data-ttu-id="b3efd-111">Per creare una factory, includere il `dxcore.h` file di intestazione e chiamare la funzione [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free.</span><span class="sxs-lookup"><span data-stu-id="b3efd-111">To create a factory, include the `dxcore.h` header file, and call the [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free function.</span></span>

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a><span data-ttu-id="b3efd-112">Recuperare un elenco di adapter</span><span class="sxs-lookup"><span data-stu-id="b3efd-112">Retrieve an adapter list</span></span>

<span data-ttu-id="b3efd-113">A differenza di DXGI, una factory di adapter DXCore appena creata non crea automaticamente uno snapshot dello stato dell'adapter del sistema.</span><span class="sxs-lookup"><span data-stu-id="b3efd-113">Unlike with DXGI, a newly-created DXCore adapter factory doesn't automatically create a snapshot of the adapter state of the system.</span></span> <span data-ttu-id="b3efd-114">Invece, DXCore crea tale snapshot quando si recupera in modo esplicito un oggetto elenco di adapter, rappresentato dall'interfaccia [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .</span><span class="sxs-lookup"><span data-stu-id="b3efd-114">Instead, DXCore creates that snapshot when you explicitly retrieve an adapter list object, which is represented by the [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface.</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a><span data-ttu-id="b3efd-115">Selezionare una scheda appropriata dall'elenco</span><span class="sxs-lookup"><span data-stu-id="b3efd-115">Select an appropriate adapter from the list</span></span>

<span data-ttu-id="b3efd-116">In questa sezione viene illustrato come, dato un oggetto elenco di adapter, è possibile trovare la prima scheda hardware nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3efd-116">This section demonstrates how, given an adapter list object, you could find the first hardware adapter in the list.</span></span>

<span data-ttu-id="b3efd-117">Il metodo [**IDXCoreAdapterList:: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) indica il numero di elementi nell'elenco e [**IDXCoreAdapterList:: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) recupera un adapter specifico in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="b3efd-117">The [**IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) method tells you the number of elements in the list, and [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) retrieves a specific adapter by index.</span></span>

<span data-ttu-id="b3efd-118">È quindi possibile eseguire una query sulle proprietà dell'adapter attenendosi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="b3efd-118">You can then query the properties of that adapter, by following these steps.</span></span>

- <span data-ttu-id="b3efd-119">Per prima cosa, per verificare che sia valido recuperare il valore di una determinata proprietà per questo adapter in questa versione del sistema operativo, chiamare [**IDXCoreAdapter:: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span><span class="sxs-lookup"><span data-stu-id="b3efd-119">First, to confirm that it's valid to retrieve the value of a given property for this adapter on this operating system version, you call [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span></span> <span data-ttu-id="b3efd-120">Passare un valore dell'enumerazione [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) per identificare la proprietà su cui si sta eseguendo una query.</span><span class="sxs-lookup"><span data-stu-id="b3efd-120">Pass a value of the [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) enumeration to identify which property you're querying about.</span></span>
- <span data-ttu-id="b3efd-121">Facoltativamente, verificare la dimensione del valore della proprietà con una chiamata a [**IDXCoreAdapter:: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span><span class="sxs-lookup"><span data-stu-id="b3efd-121">Optionally confirm the size of the property value with a call to [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span></span> <span data-ttu-id="b3efd-122">Per una proprietà, ad esempio **DXCoreAdapterProperty:: hardware**, che è un valore booleano semplice, questo passaggio non è necessario.</span><span class="sxs-lookup"><span data-stu-id="b3efd-122">For a property such as **DXCoreAdapterProperty::IsHardware**, which is a simple Boolean, this step isn't necessary.</span></span>
- <span data-ttu-id="b3efd-123">Infine, recuperare il valore della proprietà chiamando [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b3efd-123">And, finally, retrieve the property's value by calling [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

const uint32_t count{ d3D12CoreComputeAdapters->GetAdapterCount() };

for (uint32_t i = 0; i < count; ++i)
{
    winrt::com_ptr<IDXCoreAdapter> candidateAdapter;
    winrt::check_hresult(
        d3D12CoreComputeAdapters->GetAdapter(i, candidateAdapter.put()));

    bool isHardware{ false };
    winrt::check_hresult(candidateAdapter->GetProperty(
        DXCoreAdapterProperty::IsHardware,
        &isHardware));

    if (isHardware)
    {
        // Choose the first hardware adapter, and stop looping.
        preferredAdapter = candidateAdapter;
        break;
    }

    // Otherwise, ensure that (as long as there are *any* adapters) we'll
    // at least choose one.
    if (!preferredAdapter)
    {
        preferredAdapter = candidateAdapter;
    }
}
```

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a><span data-ttu-id="b3efd-124">Selezionare la scheda preferita ordinando un elenco di adapter</span><span class="sxs-lookup"><span data-stu-id="b3efd-124">Select the preferred adapter by sorting an adapter list</span></span>

<span data-ttu-id="b3efd-125">È possibile ordinare un elenco di adapter DXCore chiamando il metodo [IDXCoreAdapterList:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .</span><span class="sxs-lookup"><span data-stu-id="b3efd-125">You can sort a DXCore adapter list by calling the [IDXCoreAdapterList::Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) method.</span></span>

<span data-ttu-id="b3efd-126">L'enumerazione [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) definisce i valori che rappresentano i criteri di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="b3efd-126">The [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) enumeration defines values that representing sort criteria.</span></span> <span data-ttu-id="b3efd-127">Passare una matrice di tali valori da **ordinare**, quindi leggere il primo adapter nell'elenco ordinato risultante.</span><span class="sxs-lookup"><span data-stu-id="b3efd-127">Pass an array of those values to **Sort**, and then read off the first adapter in the resulting sorted list.</span></span>

<span data-ttu-id="b3efd-128">Per determinare se un tipo di ordinamento verrà interpretato da **Sort**, chiamare prima [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="b3efd-128">To determine whether a sort type is going to be understood by **Sort**, first call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> TryFindHardwareHighPerformanceGraphicsAdapter()
{
    // You begin DXCore adapter enumeration by creating an adapter factory.
    winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
    winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));

    // From the factory, retrieve a list of all the Direct3D 12 Graphics adapters.
    winrt::com_ptr<IDXCoreAdapterList> d3D12GraphicsAdapters;
    GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS };
    winrt::check_hresult(
        adapterFactory->CreateAdapterList(_countof(attributes),
            attributes,
            d3D12GraphicsAdapters.put()));

    DXCoreAdapterPreference sortPreferences[]{
        DXCoreAdapterPreference::Hardware, DXCoreAdapterPreference::HighPerformance };

    // Ask the OS to sort for the highest performance hardware adapter.
    winrt::check_hresult(d3D12GraphicsAdapters->Sort(_countof(sortPreferences), sortPreferences));

    winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

    if (d3D12GraphicsAdapters->GetAdapterCount() > 0)
    {
        winrt::check_hresult(d3D12GraphicsAdapters->GetAdapter(0, preferredAdapter.put()));
    }

    return preferredAdapter;
}
```

## <a name="query-and-set-adapter-state-properties"></a><span data-ttu-id="b3efd-129">Eseguire query e impostare lo stato dell'adapter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="b3efd-129">Query and set adapter state (properties)</span></span>

<span data-ttu-id="b3efd-130">È possibile recuperare e impostare lo stato di un elemento di stato specificato di un adapter chiamando il metodo [**IDXCoreAdapter:: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) e [**IDXCoreAdapter:: sestate**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="b3efd-130">You can retrieve and set the state of a specified state item of an adapter by calling the [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) and [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) methods.</span></span>

```cppwinrt
void SetDesiredMemoryReservation(winrt::com_ptr<IDXCoreAdapter> const& adapter, uint64_t reservation)
{
    DXCoreAdapterMemoryBudgetNodeSegmentGroup nodeSegmentGroup{};
    nodeSegmentGroup.nodeIndex = 0;
    nodeSegmentGroup.segmentGroup = DXCoreSegmentGroup::Local;

    DXCoreAdapterMemoryBudget memoryBudget{};
    winrt::check_hresult(adapter->QueryState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &memoryBudget));

    // Clamp the reservation to what's available.
    reservation = std::min<uint64_t>(reservation, memoryBudget.availableForReservation);

    winrt::check_hresult(adapter->SetState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &reservation));
}
```

<span data-ttu-id="b3efd-131">In pratica, prima di chiamare **QueryState** e **sestate**, è necessario chiamare [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per questo adapter e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b3efd-131">In practice, before calling **QueryState** and **SetState**, you should call [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="adapter-list-freshness"></a><span data-ttu-id="b3efd-132">Aggiornamento dell'elenco degli adapter</span><span class="sxs-lookup"><span data-stu-id="b3efd-132">Adapter list freshness</span></span>

<span data-ttu-id="b3efd-133">Se un elenco di adapter diventa obsoleto a causa delle mutevoli condizioni del sistema, verrà contrassegnato come tale.</span><span class="sxs-lookup"><span data-stu-id="b3efd-133">Should an adapter list become stale due to changing system conditions, it will be marked as such.</span></span> <span data-ttu-id="b3efd-134">È possibile determinare l'aggiornamento di un elenco di adapter eseguendo il polling del metodo [**IDXCoreAdapterList::**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) IsValid.</span><span class="sxs-lookup"><span data-stu-id="b3efd-134">You can determine an adapter list's freshness by polling its [**IDXCoreAdapterList::IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) method.</span></span>

<span data-ttu-id="b3efd-135">Più facilmente, tuttavia, è possibile sottoscrivere le notifiche per le condizioni, ad esempio l'obsolescenza.</span><span class="sxs-lookup"><span data-stu-id="b3efd-135">More conveniently, though, you can subscribe to notifications for conditions such as staleness.</span></span> <span data-ttu-id="b3efd-136">A tale scopo, passare [**DXCoreNotificationType:: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) a [**IDXCoreAdapterFactory:: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)e archiviare in modo sicuro il cookie restituito per utilizzarlo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b3efd-136">To do that, pass [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) to [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), and safely store the returned cookie for use later.</span></span>

```cppwinrt
uint32_t m_eventCookie = 0;
...
winrt::check_hresult(factory->RegisterEventNotification(
    m_adapters.get(),
    DXCoreNotificationType::AdapterListStale,
    OnAdapterListStale,
    this,
    &m_eventCookie));
...
static void WINAPI OnAdapterListStale(
    DXCoreNotificationType notificationType,
    IUnknown* staleObject,
    void* context)
{
    ...
}
```

<span data-ttu-id="b3efd-137">È quindi possibile generare un nuovo oggetto elenco di adapter corrente dall'oggetto Factory già esistente.</span><span class="sxs-lookup"><span data-stu-id="b3efd-137">You can then generate a new, current, adapter list object from the factory object that you already have.</span></span> <span data-ttu-id="b3efd-138">La gestione di queste condizioni è essenziale per la capacità di rispondere in modo semplice a eventi quali l'arrivo e la rimozione degli adapter, sia che si tratti di una GPU o di un adattatore di calcolo specializzato, sia per spostare in modo appropriato i carichi di lavoro in risposta.</span><span class="sxs-lookup"><span data-stu-id="b3efd-138">Handling these conditions is critical to your ability to seamlessly respond to events such as adapter arrival and removal (whether that be a GPU, or a specialized compute adapter), and to appropriately shift workloads in response.</span></span>

<span data-ttu-id="b3efd-139">Prima di eliminare l'oggetto elenco di adapter, è necessario utilizzare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span><span class="sxs-lookup"><span data-stu-id="b3efd-139">Before you destroy the adapter list object, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span></span> <span data-ttu-id="b3efd-140">Se non si annulla la registrazione, viene generata un'eccezione irreversibile quando viene rilevata la situazione.</span><span class="sxs-lookup"><span data-stu-id="b3efd-140">If you don't unregister, then a fatal exception is raised when the situation is detected.</span></span>

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a><span data-ttu-id="b3efd-141">Visualizza informazioni</span><span class="sxs-lookup"><span data-stu-id="b3efd-141">Display information</span></span>

> [!NOTE]
> <span data-ttu-id="b3efd-142">DXCore non fornisce alcuna informazione di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b3efd-142">DXCore doesn't itself provide any display information.</span></span> <span data-ttu-id="b3efd-143">Se necessario, usare la classe Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="b3efd-143">Where necessary, you should use the Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) class to retrieve this information.</span></span> <span data-ttu-id="b3efd-144">Il [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) di un adapter fornisce un identificatore comune che è possibile usare per eseguire il mapping di una scheda DXCore alle informazioni di [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) .</span><span class="sxs-lookup"><span data-stu-id="b3efd-144">An adapter's [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) provides a common identifier that you can use to map a DXCore adapter to [**DisplayMonitor.DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) information.</span></span> <span data-ttu-id="b3efd-145">Per ottenere il LUID di un adapter, passare [**DXCoreAdapterProperty:: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) al metodo [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b3efd-145">To obtain an adapter's LUID, pass [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) to the [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3efd-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3efd-146">See also</span></span>

* [<span data-ttu-id="b3efd-147">Applicazione DXCore minima</span><span class="sxs-lookup"><span data-stu-id="b3efd-147">Minimal DXCore application</span></span>](dxcore-source-code.md)
* [<span data-ttu-id="b3efd-148">Riferimento a DXCore</span><span class="sxs-lookup"><span data-stu-id="b3efd-148">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="b3efd-149">Grafica Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b3efd-149">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)