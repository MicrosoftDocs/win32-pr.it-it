---
title: Uso di DXCore per enumerare gli adapter
description: Esaminare le funzionalità principali di DXCore con alcuni esempi di codice, nonché un elenco di codice sorgente completo di un'applicazione DXCore minima.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: fc2120c85b48b89478d1a10c8cf853c947e6553d
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812360"
---
# <a name="using-dxcore-to-enumerate-adapters"></a>Uso di DXCore per enumerare gli adapter

DXCore è un'API di enumerazione degli adattatori per i dispositivi DirectX, quindi alcune delle sue funzionalità si sovrappongono a quelle di [DXGI.](../direct3ddxgi/dx-graphics-dxgi.md)

DXCore consente l'esposizione di nuovi tipi di dispositivi alla modalità utente, ad esempio MCDM (Microsoft Compute Driver Model), per l'uso con [Direct3D 12,](../direct3d12/directx-12-programming-guide.md) [DirectML](/windows/ai/directml/dml) [e Windows Machine Learning](/windows/ai/windows-ml/). DXCore, a differenza di DXGI, non fornisce informazioni sulla tecnologia o sulle proprietà correlate alla visualizzazione

Nelle prossime sezioni verranno descritte le funzionalità principali di DXCore con alcuni esempi di codice (scritti in [C++/WinRT).](/windows/uwp/cpp-and-winrt-apis) Gli esempi di codice illustrati di seguito sono estratti dal listato di codice sorgente completo che è possibile trovare nell'argomento [Applicazione DXCore minima](dxcore-source-code.md).

## <a name="create-an-adapter-factory"></a>Creare una factory di adapter

Per iniziare l'enumerazione dell'adattatore DXCore, creare un oggetto adapter factory, rappresentato [**dall'interfaccia IDXCoreAdapterFactory.**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) Per creare una factory, includere il `dxcore.h` file di intestazione e chiamare la funzione gratuita [**DXCoreCreateAdapterFactory.**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md)

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Recuperare un elenco di adapter

A differenza di DXGI, una factory di adattatori DXCore appena creata non crea automaticamente uno snapshot dello stato dell'adattatore del sistema. DXCore crea invece lo snapshot quando si recupera in modo esplicito un oggetto elenco di adapter, rappresentato [**dall'interfaccia IDXCoreAdapterList.**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md)

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Selezionare un adattatore appropriato dall'elenco

In questa sezione viene illustrato come, dato un oggetto elenco di schede, è possibile trovare la prima scheda hardware nell'elenco.

Il [**metodo IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) indica il numero di elementi nell'elenco e [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) recupera un adattatore specifico in base all'indice.

È quindi possibile eseguire una query delle proprietà dell'adapter seguendo questa procedura.

- Prima di tutto, per verificare che sia valido recuperare il valore di una determinata proprietà per questo adapter in questa versione del sistema operativo, chiamare [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md). Passare un valore [**dell'enumerazione DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) per identificare la proprietà su cui si esegue una query.
- Facoltativamente, verificare le dimensioni del valore della proprietà con una chiamata a [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md). Per una proprietà come **DXCoreAdapterProperty::IsHardware,** che è un valore booleano semplice, questo passaggio non è necessario.
- Infine, recuperare il valore della proprietà chiamando [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Selezionare l'adattatore preferito ordinando un elenco di adapter

È possibile ordinare un elenco di adattatori DXCore chiamando il [metodo IDXCoreAdapterList::Sort.](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md)

[L'enumerazione DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) definisce i valori che rappresentano i criteri di ordinamento. Passare una matrice di tali valori a **Sort** e quindi leggere il primo adattatore nell'elenco ordinato risultante.

Per determinare se un tipo di ordinamento verrà riconosciuto da **Sort,** chiamare [prima IDXCoreAdapterList::IsAdapterPreferenceSupported.](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)

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

## <a name="query-and-set-adapter-state-properties"></a>Eseguire query e impostare lo stato dell'adapter (proprietà)

È possibile recuperare e impostare lo stato di un elemento di stato specificato di un adattatore chiamando i [**metodi IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) e [**IDXCoreAdapter::SetState.**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md)

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

In pratica, prima di chiamare **QueryState** e **SetState,** è necessario chiamare [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di query sul tipo di stato sia disponibile per questa scheda e sistema operativo.

## <a name="adapter-list-freshness"></a>Freshness dell'elenco di adapter

Se un elenco di adattatori diventa obsoleto a causa della modifica delle condizioni di sistema, verrà contrassegnato come tale. È possibile determinare l'aggiornamento di un elenco di adattatori tramite il polling del relativo [**metodo IDXCoreAdapterList::IsStale.**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md)

In modo più pratico, tuttavia, è possibile sottoscrivere le notifiche per condizioni quali il non aggiornamento. A tale scopo, passare [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) a [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)e archiviare in modo sicuro il cookie restituito per usarlo in un secondo momento.

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

È quindi possibile generare un nuovo oggetto elenco di adapter corrente dall'oggetto factory già presente. La gestione di queste condizioni è fondamentale per la capacità di rispondere facilmente a eventi come l'arrivo e la rimozione di schede (che si tratta di una GPU o di un adattatore di calcolo specializzato) e di spostare in modo appropriato i carichi di lavoro in risposta.

Prima di eliminare l'oggetto elenco di adapter, è necessario usare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Se non si annulla la registrazione, viene generata un'eccezione irreversibile quando viene rilevata la situazione.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Visualizzare le informazioni

> [!NOTE]
> DXCore non fornisce alcuna informazione di visualizzazione. Se necessario, è necessario usare la Windows [**Runtime DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) per recuperare queste informazioni. LuiD di [](/windows/win32/api/winnt/ns-winnt-luid) un adapter fornisce un identificatore comune che è possibile usare per eseguire il mapping di un adattatore DXCore alle [**informazioni DisplayMonitor.DisplayAdapterId.**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) Per ottenere il LUID di un adapter, passare [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) al [**metodo IDXCoreAdapter::GetProperty.**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md)

## <a name="see-also"></a>Vedi anche

* [Applicazione DXCore minima](dxcore-source-code.md)
* [Informazioni di riferimento su DXCore](./dxcore-reference.md)
* [Grafica Direct3D 12](../direct3d12/direct3d-12-graphics.md)