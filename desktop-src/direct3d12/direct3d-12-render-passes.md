---
title: Passaggi di rendering di Direct3D 12
description: La funzionalità di rendering passa consente al renderer di migliorare l'efficienza della GPU riducendo il traffico di memoria alla/dalla memoria fuori chip; Questa operazione consente all'applicazione di identificare meglio i requisiti di ordinamento per il rendering delle risorse e le dipendenze dei dati.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: f776729f17ac0017d713c6f37bc71de7302a7c08
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/26/2020
ms.locfileid: "104548779"
---
# <a name="direct3d-12-render-passes"></a>Passaggi di rendering di Direct3D 12

La funzionalità di passaggio di rendering è una novità di Windows 10, versione 1809 (10,0; Build 17763) e introduce il concetto di passaggio di rendering di Direct3D 12. Un passaggio di rendering è costituito da un subset dei comandi registrati in un elenco di comandi.

Per dichiarare l'inizio e la fine di ogni passaggio di rendering, nidificare i comandi che appartengono a che passano nelle chiamate a [**ID3D12GraphicsCommandList4:: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) e [**EndRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass). Di conseguenza, qualsiasi elenco di comandi contiene zero, uno o più passaggi di rendering.

## <a name="scenarios"></a>Scenari

Il rendering passa può migliorare le prestazioni del renderer se è basato su Tile-Based rendering posticipato (TBDR), tra le altre tecniche. In particolare, la tecnica consente al renderer di migliorare l'efficienza della GPU riducendo il traffico di memoria alla/dalla memoria fuori chip consentendo all'applicazione di identificare meglio i requisiti di ordinamento per il rendering delle risorse e le dipendenze dei dati.

Un driver di visualizzazione scritto espressamente per sfruttare la funzionalità di passaggio di rendering fornisce i migliori risultati. Tuttavia, le API di rendering passano possono essere eseguite anche su driver preesistenti, anche se non necessariamente con miglioramenti delle prestazioni.

Questi sono gli scenari in cui il passaggio di rendering è progettato per fornire un valore.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Consentire all'applicazione di evitare carichi/archivi di risorse non necessari da/verso la memoria principale in un'architettura Tile-Based rendering posticipato (TBDR)

Una delle proposte di valore del passaggio di rendering è che fornisce una posizione centrale per indicare le dipendenze dei dati dell'applicazione per un set di operazioni di rendering. Tali dipendenze consentono al driver di visualizzazione di ispezionare i dati in fase di binding/barriera e di emettere istruzioni per ridurre al minimo i caricamenti/archivi delle risorse da e verso la memoria principale.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Consenti all'architettura TBDR di opportunisticamente risorse persistenti nella cache su chip tra i passaggi di rendering (anche in elenchi di comandi separati)

> [!NOTE]
> In particolare, questo scenario è limitato ai casi in cui si sta scrivendo sulle stesse destinazioni di rendering tra più elenchi di comandi.

Un modello di rendering comune prevede che l'applicazione esegua il rendering delle stesse destinazioni di rendering in più elenchi di comandi in modo seriale, anche se i comandi di rendering vengono generati in parallelo. L'uso dei passaggi di rendering in questo scenario consente di combinare questi passaggi in modo tale che, poiché l'applicazione sa che riprende il rendering nell'elenco dei comandi immediatamente successivi, che il driver di visualizzazione può evitare uno scaricamento nella memoria principale nei limiti dell'elenco dei comandi.

## <a name="your-applications-responsibilities"></a>Responsabilità dell'applicazione

Anche con la funzionalità di passaggio di rendering, né il runtime di Direct3D 12 né il driver di visualizzazione assumono la responsabilità di dedurre le opportunità di riordinare/evitare i carichi e gli archivi. Per sfruttare correttamente la funzionalità di passaggio di rendering, l'applicazione ha queste responsabilità.

- Identificare correttamente le dipendenze di dati/ordini per le relative operazioni.
- Ordinare gli invii in modo da ridurre al minimo gli scaricamenti, per ridurre al minimo l'uso dei flag di **_PRESERVE** .
- Usare correttamente le barriere delle risorse e tenere traccia dello stato delle risorse.
- Evitare copie/cancellazioni non necessarie. Per facilitarne l'identificazione, è possibile usare gli avvisi di prestazioni automatici dallo [strumento pix per Windows](https://devblogs.microsoft.com/pix/).

## <a name="using-the-render-pass-feature"></a>Uso della funzionalità di passaggio di rendering

### <a name="what-is-a-render-pass"></a>Che cos'è un *passaggio di rendering*?

Un passaggio di rendering viene definito da questi elementi.

- Set di associazioni di output fisse per la durata del passaggio di rendering. Queste associazioni sono a una o più visualizzazioni di destinazione di rendering (RTVs) e/o a una vista depth stencil (DSV).
- Elenco di operazioni GPU destinate a tale set di associazioni di output.
- Metadati che descrivono le dipendenze di caricamento/archiviazione per tutte le associazioni di output di destinazione del passaggio di rendering.

### <a name="declare-your-output-bindings"></a>Dichiarare le associazioni di output

All'inizio di un passaggio di rendering, si dichiarano i binding alle destinazioni di rendering e/o al buffer di profondità/stencil. Si tratta di un'associazione facoltativa a destinazioni di rendering ed è facoltativa per l'associazione a un buffer di profondità/stencil. Tuttavia, è necessario eseguire l'associazione ad almeno uno dei due e nell'esempio di codice riportato di seguito viene associato a entrambe.

Questi binding vengono dichiarati in una chiamata a [**ID3D12GraphicsCommandList4:: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

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

Il primo campo della struttura [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) viene impostato sull'handle descrittore CPU corrispondente a una o più visualizzazioni di destinazione di rendering (RTVs). Analogamente, [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) contiene l'handle del descrittore della CPU corrispondente a una visualizzazione depth stencil (DSV). Gli handle del descrittore di CPU sono gli stessi che verrebbero altrimenti passati a [**ID3D12GraphicsCommandList:: OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets). Analogamente a **OMSetRenderTargets**, i descrittori di CPU vengono *bloccati* dal rispettivo heap (descrittore della CPU) al momento della chiamata a **BeginRenderPass**.

RTVs e DSV non vengono ereditati nel passaggio di rendering. Ma devono essere impostati. Né RTVs e DSV dichiarati in **BeginRenderPass** vengono propagati all'elenco dei comandi. Sono invece in uno stato non definito che segue il passaggio di rendering.

### <a name="render-passes-and-workloads"></a>Passaggi e carichi di lavoro di rendering

Non è possibile nidificare i passaggi di rendering e non è possibile avere un passaggio di rendering a cavalcioni di più di un elenco di comandi (devono iniziare e terminare durante la registrazione in un unico elenco di comandi). Le ottimizzazioni progettate per consentire una generazione efficiente di passaggi di rendering sono illustrate nella sezione [ flag di passaggio di rendering](#render-pass-flags), più avanti.

Una scrittura eseguita dall'interno di un passaggio di rendering non è *valida* per la lettura fino a un passaggio di rendering successivo. Che impedisce alcuni tipi di barriere all'interno del passaggio &mdash; di rendering, ad esempio, la barriera da **RENDER_TARGET** a **SHADER_RESOURCE** sulla destinazione di rendering attualmente associata. Per altre informazioni, vedere la sezione [passaggi di rendering e barriere delle risorse](#render-passes-and-resource-barriers), più avanti.

L'unica eccezione al vincolo Write-Read appena citata riguarda le letture implicite che si verificano come parte del test di profondità e della fusione della destinazione di rendering.
Queste API non sono quindi consentite in un passaggio di rendering (il runtime principale rimuove l'elenco dei comandi se uno di essi viene chiamato durante la registrazione).

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
- [**ID3D12GraphicsCommandList::D patch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1::ResolveSubresourceRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3::SetProtectedResourceSession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Passaggi di rendering e barriere delle risorse

Non è possibile leggere o utilizzare una scrittura che si è verificata nello stesso passaggio di rendering. Alcune barriere non sono conformi a questo vincolo, ad esempio da **D3D12_RESOURCE_STATE_RENDER_TARGET** a **\* _SHADER_RESOURCE** sulla destinazione di rendering attualmente associata (e il livello di debug genera un errore a tale scopo). Tuttavia, la stessa barriera in una destinazione di rendering scritta al di *fuori* del passaggio di rendering corrente è conforme, perché le scritture vengono completate prima dell'avvio del passaggio di rendering corrente.
È possibile trarre vantaggio dalla conoscenza di determinate ottimizzazioni che possono essere apportate da un driver di visualizzazione in questo senso. Dato un carico di lavoro conforme, un driver di visualizzazione potrebbe spostare eventuali barriere rilevate nel passaggio di rendering all'inizio del passaggio di rendering. In questo caso possono essere unite (senza interferire con le operazioni di affiancamento/suddivisione in contenitori). Si tratta di un'ottimizzazione valida purché tutte le operazioni di scrittura siano completate prima dell'avvio del passaggio di rendering corrente.

Di seguito è riportato un esempio di ottimizzazione del driver più completo, che presuppone che si disponga di un motore di rendering con una progettazione di associazione di risorse precedente a Direct3D 12 che &mdash; esegue le barriere *su richiesta* in base alla modalità di associazione delle risorse. Quando si scrive in una visualizzazione di accesso non ordinata (UAV) verso la fine di un frame (per essere utilizzato nel frame seguente), il motore potrebbe lasciare la risorsa nello stato **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** alla conclusione del frame. Nel frame seguente, quando il motore passa a associare la risorsa come visualizzazione risorse dello shader (SRV), si noterà che la risorsa non è nello stato corretto e che verrà rilasciata una barriera da **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** a **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE**. Se tale ostacolo si verifica all'interno del passaggio di rendering, il driver di visualizzazione è giustificato nel presupposto che tutte le Scritture si siano già verificate al di *fuori* di questo passaggio di rendering corrente e, di conseguenza, ed è in questo caso che l'ottimizzazione venga avviata, il driver visualizzato potrebbe *spostare* la barriera fino all'inizio del passaggio di rendering. Anche in questo caso, si tratta di un valore valido, purché il codice sia conforme al vincolo Write-Read descritto in questa sezione e l'ultimo.


Di seguito sono riportati alcuni esempi di barriere conformi.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** **\* _SHADER_RESOURCE**.

E sono esempi di barriere non conformi.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** lo stato di lettura su RTVs/viste origine dati attualmente associati.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** lo stato di lettura su RTVs/viste origine dati attualmente associati.
- Qualsiasi barriera di aliasing.
- Barriere per la visualizzazione di accesso non ordinato (UAV). 

### <a name="resource-access-declaration"></a>Dichiarazione di accesso alle risorse

In fase di **BeginRenderPass** , oltre a dichiarare tutte le risorse che fungono da RTVs e/o vista origine dati all'interno di tale passaggio, è necessario specificare anche le caratteristiche di *accesso* iniziale e finale. Come si può notare nell'esempio di codice nella sezione [dichiarare i binding di output](#declare-your-output-bindings) precedente, è possibile eseguire questa operazione con le strutture [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) e [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) .

Per ulteriori informazioni, vedere le strutture [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) e [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) e le enumerazioni [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) e [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) .

### <a name="render-pass-flags"></a>Flag di passaggio di rendering

L'ultimo parametro passato a **BeginRenderPass** è un flag di passaggio di rendering (un valore dell'enumerazione [**D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) ).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>Scritture UAV in un passaggio di rendering

Le Scritture per la visualizzazione di accesso non ordinato (UAV) sono consentite in un passaggio di rendering, ma è necessario indicare in modo specifico che le Scritture UAV verranno rilasciate nel passaggio di rendering specificando **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES**, in modo che il driver di visualizzazione possa rifiutare esplicitamente l'affiancamento, se necessario.

Gli accessi UAV devono seguire il vincolo Write-Read descritto in precedenza (le Scritture in un passaggio di rendering non sono valide per la lettura fino a un passaggio di rendering successivo). Le barriere UAV non sono consentite in un passaggio di rendering.

Le associazioni UAV (tramite tabelle radice o descrittori radice) vengono ereditate in passaggi di rendering e vengono propagate all'esterno dei passaggi di rendering.

#### <a name="suspending-passes-and-resuming-passes"></a>Sospensione-passaggi e ripresa-passaggi

È possibile indicare un passaggio di rendering intero come un passaggio di sospensione e/o un passaggio di ripresa. Una coppia di sospensione seguito da una coppia deve avere viste o flag di accesso identici tra i passaggi, e potrebbero non includere operazioni GPU (ad esempio, Draw, repliche, eliminazioni, cancellazioni, copie, aggiornamento-affiancato, mapping, Write-buffer-immediate, query, Risolvi query) tra il passaggio di rendering di sospensione e il passaggio di rendering di ripresa.

Il caso d'uso previsto è il rendering multithread, in cui ad esempio quattro elenchi di comandi (ognuno con i rispettivi passaggi di rendering) possono avere come destinazione le stesse destinazioni di rendering. Quando i passaggi di rendering vengono sospesi o ripresi tra gli elenchi di comandi, gli elenchi di comandi devono essere eseguiti nella stessa chiamata a [**ID3D12CommandQueue:: oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Una sessione di rendering può essere ripresa e sospesa. Nell'esempio multithread appena specificato, gli elenchi di comandi 2 e 3 dovrebbero riprendere rispettivamente da 1 a 2. E allo stesso tempo 2 e 3 verrebbero sospesi rispettivamente a 3 e 4.

## <a name="query-for-render-passes-feature-support"></a>Query per il supporto delle funzionalità delle sessioni di rendering

È possibile chiamare [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) per eseguire una query sulla misura in cui un driver di dispositivo e/o l'hardware supporta in modo efficiente i passaggi di rendering.

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

A causa della logica di mapping del runtime, il rendering passa sempre alla funzione. Tuttavia, a seconda del supporto delle funzionalità, non forniranno sempre un vantaggio. È possibile usare codice simile all'esempio di codice precedente per determinare se/quando è necessario eseguire i comandi come passaggi di rendering e quando il Runtime sta semplicemente eseguendo il mapping alla superficie dell'API esistente (in questo caso, L'esecuzione di questo controllo è particolarmente importante se si usa [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)).

Per una descrizione dei tre livelli di supporto, vedere l'enumerazione [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) .
