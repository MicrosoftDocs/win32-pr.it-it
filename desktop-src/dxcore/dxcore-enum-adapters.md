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
# <a name="using-dxcore-to-enumerate-adapters"></a>Uso di DXCore per enumerare gli adapter

DXCore è un'API di enumerazione degli adapter per i dispositivi DirectX, quindi alcune delle sue funzionalità si sovrappongono a quelle di [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).

DXCore consente l'esposizione dei nuovi tipi di dispositivo alla modalità utente, ad esempio MCDM (modello di driver di calcolo Microsoft), per l'uso con [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)e [Windows Machine Learning](/windows/ai/windows-ml/). DXCore, a differenza di DXGI, non fornisce informazioni sulla tecnologia o sulle proprietà correlate alla visualizzazione

Nelle prossime sezioni verranno esaminate le principali funzionalità di DXCore con alcuni esempi di codice (scritti in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)). Gli esempi di codice illustrati di seguito sono estratti dal listato di codice sorgente completo che è possibile trovare nell'argomento [applicazione DXCore minima](dxcore-source-code.md).

## <a name="create-an-adapter-factory"></a>Creare una factory di adapter

Per iniziare l'enumerazione degli adapter di DXCore, è necessario creare un oggetto factory di adapter, rappresentato dall'interfaccia [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) . Per creare una factory, includere il `dxcore.h` file di intestazione e chiamare la funzione [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free.

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Recuperare un elenco di adapter

A differenza di DXGI, una factory di adapter DXCore appena creata non crea automaticamente uno snapshot dello stato dell'adapter del sistema. Invece, DXCore crea tale snapshot quando si recupera in modo esplicito un oggetto elenco di adapter, rappresentato dall'interfaccia [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Selezionare una scheda appropriata dall'elenco

In questa sezione viene illustrato come, dato un oggetto elenco di adapter, è possibile trovare la prima scheda hardware nell'elenco.

Il metodo [**IDXCoreAdapterList:: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) indica il numero di elementi nell'elenco e [**IDXCoreAdapterList:: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) recupera un adapter specifico in base all'indice.

È quindi possibile eseguire una query sulle proprietà dell'adapter attenendosi alla seguente procedura.

- Per prima cosa, per verificare che sia valido recuperare il valore di una determinata proprietà per questo adapter in questa versione del sistema operativo, chiamare [**IDXCoreAdapter:: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md). Passare un valore dell'enumerazione [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) per identificare la proprietà su cui si sta eseguendo una query.
- Facoltativamente, verificare la dimensione del valore della proprietà con una chiamata a [**IDXCoreAdapter:: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md). Per una proprietà, ad esempio **DXCoreAdapterProperty:: hardware**, che è un valore booleano semplice, questo passaggio non è necessario.
- Infine, recuperare il valore della proprietà chiamando [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Selezionare la scheda preferita ordinando un elenco di adapter

È possibile ordinare un elenco di adapter DXCore chiamando il metodo [IDXCoreAdapterList:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .

L'enumerazione [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) definisce i valori che rappresentano i criteri di ordinamento. Passare una matrice di tali valori da **ordinare**, quindi leggere il primo adapter nell'elenco ordinato risultante.

Per determinare se un tipo di ordinamento verrà interpretato da **Sort**, chiamare prima [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

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

È possibile recuperare e impostare lo stato di un elemento di stato specificato di un adapter chiamando il metodo [**IDXCoreAdapter:: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) e [**IDXCoreAdapter:: sestate**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .

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

In pratica, prima di chiamare **QueryState** e **sestate**, è necessario chiamare [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per questo adapter e il sistema operativo.

## <a name="adapter-list-freshness"></a>Aggiornamento dell'elenco degli adapter

Se un elenco di adapter diventa obsoleto a causa delle mutevoli condizioni del sistema, verrà contrassegnato come tale. È possibile determinare l'aggiornamento di un elenco di adapter eseguendo il polling del metodo [**IDXCoreAdapterList::**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) IsValid.

Più facilmente, tuttavia, è possibile sottoscrivere le notifiche per le condizioni, ad esempio l'obsolescenza. A tale scopo, passare [**DXCoreNotificationType:: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) a [**IDXCoreAdapterFactory:: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)e archiviare in modo sicuro il cookie restituito per utilizzarlo in un secondo momento.

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

È quindi possibile generare un nuovo oggetto elenco di adapter corrente dall'oggetto Factory già esistente. La gestione di queste condizioni è essenziale per la capacità di rispondere in modo semplice a eventi quali l'arrivo e la rimozione degli adapter, sia che si tratti di una GPU o di un adattatore di calcolo specializzato, sia per spostare in modo appropriato i carichi di lavoro in risposta.

Prima di eliminare l'oggetto elenco di adapter, è necessario utilizzare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Se non si annulla la registrazione, viene generata un'eccezione irreversibile quando viene rilevata la situazione.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Visualizza informazioni

> [!NOTE]
> DXCore non fornisce alcuna informazione di visualizzazione. Se necessario, usare la classe Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) per recuperare queste informazioni. Il [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) di un adapter fornisce un identificatore comune che è possibile usare per eseguire il mapping di una scheda DXCore alle informazioni di [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) . Per ottenere il LUID di un adapter, passare [**DXCoreAdapterProperty:: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) al metodo [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .

## <a name="see-also"></a>Vedi anche

* [Applicazione DXCore minima](dxcore-source-code.md)
* [Riferimento a DXCore](./dxcore-reference.md)
* [Grafica Direct3D 12](../direct3d12/direct3d-12-graphics.md)