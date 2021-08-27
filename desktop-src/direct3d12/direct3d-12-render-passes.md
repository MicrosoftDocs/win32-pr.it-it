---
title: Passaggi di rendering Direct3D 12
description: La funzionalità dei passaggi di rendering consente al renderer di migliorare l'efficienza della GPU riducendo il traffico di memoria da e verso la memoria off chip; Ciò consente all'applicazione di identificare meglio i requisiti di ordinamento del rendering delle risorse e le dipendenze dei dati.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: 96ed14cecd518a3e03672f2667306ee0a4b8d64999aab01aa72aae04975f0a83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069691"
---
# <a name="direct3d-12-render-passes"></a>Passaggi di rendering Direct3D 12

La funzionalità dei passaggi di rendering è una novità Windows 10, versione 1809 (10.0; Build 17763) e introduce il concetto di passaggio di rendering Direct3D 12. Un passaggio di rendering è costituito da un subset dei comandi registrati in un elenco di comandi.

Per dichiarare dove inizia e termina ogni passaggio di rendering, annidare i comandi appartenenti a che passano all'interno di chiamate [**a ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) ed [**EndRenderPass.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass) Di conseguenza, qualsiasi elenco di comandi contiene zero, uno o più passaggi di rendering.

## <a name="scenarios"></a>Scenari

I passaggi di rendering possono migliorare le prestazioni del renderer se è basato su Tile-Based rendering posticipato (TBDR), tra le altre tecniche. In particolare, la tecnica consente al renderer di migliorare l'efficienza della GPU riducendo il traffico di memoria da e verso la memoria fuori chip consentendo all'applicazione di identificare meglio i requisiti di ordinamento del rendering delle risorse e le dipendenze dei dati.

Un driver video scritto espressamente per sfruttare la funzionalità dei passaggi di rendering offre i risultati migliori. Ma le API per i passaggi di rendering possono essere eseguite anche su driver preesistnti ,anche se non necessariamente con miglioramenti delle prestazioni.

Questi sono gli scenari in cui i passaggi di rendering sono progettati per fornire valore.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Consentire all'applicazione di evitare carichi/archivi di risorse non necessari dalla/alla memoria principale in un'architettura Tile-Based rendering posticipato (TBDR)

Una delle proposta di valore dei passaggi di rendering è che offre una posizione centrale per indicare le dipendenze dei dati dell'applicazione per un set di operazioni di rendering. Queste dipendenze dei dati consentono al driver di visualizzazione di esaminare questi dati in fase di associazione/barriera e di rilasciare istruzioni che riducono al minimo i carichi/archivi di risorse dalla/alla memoria principale.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Consentire all'architettura TBDR di rendere disponibili risorse opportunisticamente persistenti nella cache su chip tra i passaggi di rendering (anche in elenchi di comandi separati)

> [!NOTE]
> In particolare, questo scenario è limitato ai casi in cui si scrive nelle stesse destinazione di rendering in più elenchi di comandi.

Un modello di rendering comune è quello in cui l'applicazione esegue il rendering in serie delle stesse destinazione di rendering tra più elenchi di comandi, anche se i comandi di rendering vengono generati in parallelo. L'uso dei passaggi di rendering in questo scenario consente la combinazione di questi passaggi in modo tale (poiché l'applicazione sa che riprenderà il rendering nell'elenco di comandi immediatamente completato) che il driver di visualizzazione può evitare uno scaricamento nella memoria principale sui limiti dell'elenco dei comandi.

## <a name="your-applications-responsibilities"></a>Responsabilità dell'applicazione

Anche con la funzionalità dei passaggi di rendering, né il runtime Direct3D 12 né il driver di visualizzazione si assume la responsabilità di dedurre le opportunità di riordinare/evitare caricamenti e archivi. Per sfruttare correttamente la funzionalità dei passaggi di rendering, l'applicazione ha queste responsabilità.

- Identificare correttamente le dipendenze di dati/ordinamento per le operazioni.
- Ordinare gli invii in modo da ridurre al minimo gli scaricamenti( in modo da ridurre al minimo l'uso **_PRESERVE** flag.
- Usare correttamente le barriere delle risorse e tenere traccia dello stato delle risorse.
- Evitare copie/cancellazioni non necessario. Per identificarlo, è possibile usare gli avvisi di prestazioni automatizzati da [PIX Windows strumento](https://devblogs.microsoft.com/pix/).

## <a name="using-the-render-pass-feature"></a>Uso della funzionalità di passaggio di rendering

### <a name="what-is-a-render-pass"></a>Che cos'è *un passaggio di rendering?*

Un passaggio di rendering è definito da questi elementi.

- Set di associazioni di output fisse per la durata del passaggio di rendering. Queste associazioni sono a una o più visualizzazioni di destinazione di rendering (RTV) e/o a una vista depth stencil (DSV).
- Elenco di operazioni GPU che hanno come destinazione il set di associazioni di output.
- Metadati che descrivono le dipendenze di caricamento/archiviazione per tutte le associazioni di output di destinazione del passaggio di rendering.

### <a name="declare-your-output-bindings"></a>Dichiarare le associazioni di output

All'inizio di un passaggio di rendering, dichiari i binding alle destinazione o alle destinazione di rendering e/o al buffer depth/stencil. È facoltativo eseguire il binding per eseguire il rendering delle destinazione ed è facoltativo eseguire il binding a un buffer di profondità/stencil. Tuttavia, è necessario eseguire l'associazione ad almeno uno dei due e nell'esempio di codice seguente viene associato a entrambi.

Queste associazioni vengono dichiarate in una chiamata a [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

```cppwinrt
void render_passes(::ID3D12GraphicsCommandList4 * pIGCL4,
    D3D12_CPU_DESCRIPTOR_HANDLE const& rtvCPUDescriptorHandle,
    D3D12_CPU_DESCRIPTOR_HANDLE const& dsvCPUDescriptorHandle)
{
    const float clearColor4[]{ 0.f, 0.f, 0.f, 0.f };
    CD3DX12_CLEAR_VALUE clearValue{ DXGI_FORMAT_R32G32B32_FLOAT, clearColor4 };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessClear{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, { clearValue } };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessPreserve{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, {} };
    D3D12_RENDER_PASS_RENDER_TARGET_DESC renderPassRenderTargetDesc{ rtvCPUDescriptorHandle, renderPassBeginningAccessClear, renderPassEndingAccessPreserve };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessNoAccess{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessNoAccess{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_DEPTH_STENCIL_DESC renderPassDepthStencilDesc{ dsvCPUDescriptorHandle, renderPassBeginningAccessNoAccess, renderPassBeginningAccessNoAccess, renderPassEndingAccessNoAccess, renderPassEndingAccessNoAccess };

    pIGCL4->BeginRenderPass(1, &renderPassRenderTargetDesc, &renderPassDepthStencilDesc, D3D12_RENDER_PASS_FLAG_NONE);
    // Record command list.
    pIGCL4->EndRenderPass();
    // Begin/End further render passes and then execute the command list(s).
}
```

Impostare il primo campo della struttura di [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) sull'handle del descrittore della CPU corrispondente a una o più visualizzazioni di destinazione di rendering (RTV). Analogamente, [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) contiene l'handle del descrittore della CPU corrispondente a una vista depth stencil (DSV). Gli handle del descrittore della CPU sono gli stessi che altrimenti verrebbero passati a [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets). Come per **OMSetRenderTargets,** i descrittori della  CPU vengono ancorati dai rispettivi heap (descrittore CPU) al momento della chiamata a **BeginRenderPass.**

Le rtv e le DSV non vengono ereditate nel passaggio di rendering. Devono invece essere impostate. Né le rtv e le DSV dichiarate in **BeginRenderPass** vengono propagate all'elenco di comandi. Sono invece in uno stato non definito dopo il passaggio di rendering.

### <a name="render-passes-and-workloads"></a>Passaggi di rendering e carichi di lavoro

Non è possibile annidare i passaggi di rendering e non è possibile avere un passaggio di rendering a livello di più di un elenco di comandi (devono iniziare e terminare durante la registrazione in un singolo elenco di comandi). Le ottimizzazioni progettate per consentire una generazione multi-thread efficiente di passaggi di rendering sono illustrate nella sezione Flag di [ passaggio del rendering,](#render-pass-flags)riportata di seguito.

Una scrittura che si esegue dall'interno di un passaggio di rendering non *è* valida per la lettura fino a un passaggio di rendering successivo. Ciò preclude alcuni tipi di barriere dall'interno del passaggio di rendering, ad esempio la barriera dal RENDER_TARGET al SHADER_RESOURCE nella destinazione di rendering &mdash; attualmente associata.   Per altre informazioni, vedere la sezione Passaggi di rendering e [barriere delle risorse](#render-passes-and-resource-barriers)più avanti.

L'unica eccezione al vincolo di scrittura/lettura appena menzionato riguarda le operazioni di lettura implicita che si verificano nell'ambito del test di profondità e della fusione della destinazione di rendering.
Pertanto, queste API non sono consentite all'interno di un passaggio di rendering (il runtime principale rimuove l'elenco di comandi se una di esse viene chiamata durante la registrazione).

- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList::ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList::ClearState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList::D iscardResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1::ResolveSubresourceRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3::SetProtectedResourceSession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Passaggi di rendering e barriere di risorse

Non è possibile leggere o utilizzare una scrittura che si è verificata all'interno dello stesso passaggio di rendering. Alcune barriere non sono conformi a questo vincolo, ad esempio da **D3D12_RESOURCE_STATE_RENDER_TARGET** **\* a _SHADER_RESOURCE** nella destinazione di rendering attualmente associata (e il livello di debug restituirà un errore a tale scopo). Tuttavia, la stessa barriera in una  destinazione di rendering scritta all'esterno del passaggio di rendering corrente è conforme, perché le scritture verranno completate prima dell'inizio del passaggio di rendering corrente.
È possibile trarre vantaggio dalla conoscenza di alcune ottimizzazioni che un driver video può eseguire in questo senso. Dato un carico di lavoro conforme, un driver di visualizzazione potrebbe spostare tutte le barriere incontrate nel passaggio di rendering all'inizio del passaggio di rendering. In questo caso, possono essere coalesced (e non interferire con le operazioni di affiancamento/binning). Si tratta di un'ottimizzazione valida a condizione che tutte le scritture siano state completate prima dell'inizio del passaggio di rendering corrente.

Di seguito è riportato un esempio di ottimizzazione del driver più completo, che presuppone la disponibilità di un motore di rendering con una progettazione di associazione di risorse pre-Direct3D 12 che effettua barriere su richiesta in base al modo in cui vengono associate le &mdash; risorse.  Quando si scrive in una visualizzazione di accesso non ordinato verso la fine di un frame (da utilizzare nel frame seguente), il motore potrebbe lasciare la risorsa nello stato **D3D12_RESOURCE_STATE_UNORDERED_ACCESS al** termine del frame. Nel frame seguente, quando il motore passa ad associare la risorsa come visualizzazione risorse shader (SRV), scoprirà che la risorsa non si trova nello stato corretto e rilascerà una barriera da **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** a **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE**. Se tale barriera si verifica all'interno del passaggio di rendering, il  driver di visualizzazione è giustificato presupponendo che tutte le scritture siano già  state eseguite all'esterno di questo passaggio di rendering corrente e di conseguenza (ed è qui che entra in esecuzione l'ottimizzazione) il driver di visualizzazione potrebbe spostare la barriera fino all'inizio del passaggio di rendering. Anche in questo caso, questa operazione è valida, purché il codice sia conforme al vincolo di lettura/scrittura descritto in questa sezione e nell'ultima.


Questi sono esempi di barriere conformi.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** a **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** a **\* _SHADER_RESOURCE**.

Questi sono esempi di barriere non conformi.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** a qualsiasi stato di lettura in RTV/DSV attualmente associati.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** a qualsiasi stato di lettura in RTV/DSV attualmente associati.
- Qualsiasi barriera di aliasing.
- Barriere di visualizzazione di accesso non ordinato (UAV, Unordered Access View). 

### <a name="resource-access-declaration"></a>Dichiarazione di accesso alle risorse

Al **momento di BeginRenderPass,** oltre a dichiarare tutte le risorse che servono come RTV e/o DSV all'interno di tale passaggio, è necessario specificare anche le caratteristiche di accesso iniziale e *finale.* Come si può vedere nell'esempio di codice nella sezione Dichiarare le [](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) [associazioni](#declare-your-output-bindings) di output precedente, eseguire questa operazione con le D3D12_RENDER_PASS_RENDER_TARGET_DESC e D3D12_RENDER_PASS_DEPTH_STENCIL_DESC [**seguenti.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc)

Per altri dettagli, vedere le [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) e [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) e le [**enumerazioni**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE e [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type)

### <a name="render-pass-flags"></a>Flag di passaggio di rendering

L'ultimo parametro passato a **BeginRenderPass** è un flag di passaggio di rendering (un valore [**dell'enumerazione**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) D3D12_RENDER_PASS_FLAGS di rendering).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>Scritture UAV all'interno di un passaggio di rendering

Le scritture UAV (Unordered Access View) sono consentite **all'interno** di un passaggio di rendering, ma è necessario indicare in modo specifico che verranno emesse scritture UAV all'interno del passaggio di rendering specificando D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES , in modo che il driver di visualizzazione possa rifiutare esplicitamente l'affiancamento, se necessario.

Gli accessi UAV devono seguire il vincolo write-read descritto in precedenza (le scritture in un passaggio di rendering non sono valide per la lettura fino a un passaggio di rendering successivo). Le barriere UAV non sono consentite all'interno di un passaggio di rendering.

Le associazioni UAV (tramite tabelle radice o descrittori radice) vengono ereditate nei passaggi di rendering e vengono propagate al di fuori dei passaggi di rendering.

#### <a name="suspending-passes-and-resuming-passes"></a>Sospensione dei passaggi e ripresa dei passaggi

È possibile indicare che un intero passaggio di rendering è un passaggio di sospensione e/o un passaggio di ripresa. Una coppia suspending-followed-by-a-resuming deve avere visualizzazioni/flag di accesso identici tra i passaggi e non può avere operazioni GPU interveninti (ad esempio, disegni, dispatch, eliminazioni, cancellazioni, copie, mapping update-tile,write-buffer-immediates, query, query risolte) tra il passaggio di rendering sospeso e il passaggio di rendering ripresa.

Il caso d'uso previsto è il rendering multi-thread, in cui ad esempio quattro elenchi di comandi (ognuno con i propri passaggi di rendering) possono essere destinati alle stesse destinazioni di rendering. Quando i passaggi di rendering vengono sospesi/ripresi tra gli elenchi di comandi, gli elenchi di comandi devono essere eseguiti nella stessa chiamata a [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Un passaggio di rendering può essere sia ripresa che sospesa. Nell'esempio multi-thread appena specificato, gli elenchi di comandi 2 e 3 riprenderebbero rispettivamente da 1 e 2. Allo stesso tempo, 2 e 3 verrebbero sospesi rispettivamente a 3 e 4.

## <a name="query-for-render-passes-feature-support"></a>Supporto della funzionalità query per i passaggi di rendering

È possibile chiamare [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) per eseguire query sulla misura in cui un driver di dispositivo e/o l'hardware supportano in modo efficiente i passaggi di rendering.

```cppwinrt
D3D12_RENDER_PASS_TIER get_render_passes_tier(::ID3D12Device * pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS5 featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS5, &featureSupport, sizeof(featureSupport))
    );
    return featureSupport.RenderPassesTier;
}
...
    D3D12_RENDER_PASS_TIER renderPassesTier{ get_render_passes_tier(pIDevice) };
```

A causa della logica di mapping del runtime, il rendering passa sempre la funzione . Tuttavia, a seconda del supporto delle funzionalità, non sempre offrono un vantaggio. È possibile usare codice simile all'esempio di codice precedente per determinare se e quando vale la pena eseguire comandi durante il passaggio del rendering e quando non è sicuramente un vantaggio, ovvero quando il runtime esegue solo il mapping alla superficie DELL'API esistente. L'esecuzione di questo controllo è particolarmente importante se si usa [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12).

Per una descrizione dei tre livelli di supporto, vedere [**l'enumerazione**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) D3D12_RENDER_PASS_TIER.
