---
title: Binding in DirectML
description: In DirectML, l'associazione si riferisce all'allegato di risorse alla pipeline per la GPU da usare durante l'inizializzazione e l'esecuzione degli operatori di machine learning.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: a04bf0bcc63fff810604e3db72fe507cc10040f5
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104548830"
---
# <a name="binding-in-directml"></a>Binding in DirectML

In DirectML, l' *associazione* si riferisce all'allegato di risorse alla pipeline per la GPU da usare durante l'inizializzazione e l'esecuzione degli operatori di machine learning. Queste risorse possono essere i tensori di input e di output, ad esempio, nonché le risorse temporanee o persistenti necessarie per l'operatore.

In questo argomento vengono illustrati i dettagli concettuali e procedurali dell'associazione. Si consiglia anche di leggere completamente la documentazione per le API chiamate, inclusi i parametri e le osservazioni.

## <a name="important-ideas-in-binding"></a>Idee importanti nell'associazione

L'elenco dei passaggi seguenti contiene una descrizione di alto livello delle attività correlate all'associazione. È necessario seguire questa procedura ogni volta che si esegue un oggetto [inviabile](/windows/desktop/api/directml/nn-directml-idmldispatchable) &mdash; un dispatcher è un inizializzatore di operatore o un operatore compilato. Questa procedura introduce le idee, le strutture e i metodi importanti necessari per l'associazione DirectML.

Le sezioni successive di questo argomento approfondiscono e spiegano in modo più dettagliato queste attività di associazione, con frammenti di codice illustrativi ricavati dall'esempio di codice [dell'applicazione DirectML minimo](dml-min-app.md) .

- Chiamare [**IDMLDispatchable:: GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) sul dispatcher per determinare il numero di descrittori necessari e anche le proprie esigenze di risorse temporanee/permanenti.
- Creare un heap del descrittore Direct3D 12 sufficientemente grande per i descrittori e associarlo alla pipeline.
- Chiamare [**IDMLDevice:: CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) per creare una tabella di associazione DirectML per rappresentare le risorse vincolate alla pipeline. Utilizzare la struttura [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) per descrivere la tabella di associazione, incluso il subset dei descrittori a cui punta nell'heap del descrittore.
- Creare risorse temporanee/permanenti come risorse buffer Direct3D 12, descriverle con [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) e [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) strutture e aggiungerle alla tabella di binding.
- Se l'oggetto inviabile è un operatore compilato, creare un buffer di elementi tensore come risorsa buffer Direct3D 12. Popolarlo o caricarlo, definirlo con **DML_BUFFER_BINDING** e **DML_BINDING_DESC** strutture e aggiungerlo alla tabella di associazione.
- Passare la tabella di associazione come parametro quando si chiama [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

## <a name="retrieve-the-binding-properties-of-a-dispatchable"></a>Recuperare le proprietà di binding di un oggetto inviabile

La struttura [**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties) descrive le esigenze di binding di un operatore inviabile (inizializzatore operatore o operatore compilato). Queste proprietà correlate all'associazione includono il numero di descrittori che è necessario associare al dispatcher, nonché le dimensioni in byte di qualsiasi risorsa temporanea e/o persistente di cui necessita.

> [!NOTE]
> Anche per più operatori dello stesso tipo, non fare supposizioni su di essi con gli stessi requisiti di binding. Eseguire una query sulle proprietà di binding per ogni inizializzatore e operatore creato.

Chiamare [**IDMLDispatchable:: GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) per recuperare un **DML_BINDING_PROPERTIES**.

```cppwinrt
winrt::com_ptr<::IDMLCompiledOperator> dmlCompiledOperator;
// Code to create and compile a DirectML operator goes here.

DML_BINDING_PROPERTIES executeDmlBindingProperties{
    dmlCompiledOperator->GetBindingProperties()
};

winrt::com_ptr<::IDMLOperatorInitializer> dmlOperatorInitializer;
// Code to create a DirectML operator initializer goes here.

DML_BINDING_PROPERTIES initializeDmlBindingProperties{
    dmlOperatorInitializer->GetBindingProperties()
};

UINT descriptorCount = ...
```

Il `descriptorCount` valore recuperato qui determina la dimensione (minima) dell'heap del descrittore e della tabella di associazione creata nei due passaggi successivi.

**DML_BINDING_PROPERTIES** contiene anche un `TemporaryResourceSize` membro, ovvero la dimensione minima, in byte, della risorsa temporanea che deve essere associata alla tabella di binding per questo oggetto inviabile. Un valore pari a zero indica che non è necessaria una risorsa temporanea.

E un `PersistentResourceSize` membro, ovvero la dimensione minima, in byte, della risorsa persistente che deve essere associata alla tabella di associazione per questo oggetto inviabile. Un valore pari a zero indica che non è necessaria una risorsa permanente. Una risorsa persistente, se necessaria, deve essere fornita durante l'inizializzazione di un operatore compilato (dove è associato come output dell'inizializzatore di operatore) e durante l'esecuzione. Altre informazioni su questo argomento sono disponibili più avanti in questo argomento. Solo gli operatori compilati hanno risorse persistenti: gli inizializzatori di operatore restituiscono sempre un valore pari a 0 per il membro.

Se si chiama **IDMLDispatchable:: GetBindingProperties** in un inizializzatore di operatore sia prima che dopo una chiamata a [**IDMLOperatorInitializer:: Reset**](/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset), i due set di proprietà di associazione recuperati non sono necessariamente identici.

## <a name="describe-create-and-bind-a-descriptor-heap"></a>Descrivere, creare e associare un heap del descrittore

In termini di descrittori, la responsabilità inizia e termina con l'heap del descrittore. DirectML stesso si occupa della creazione e della gestione dei descrittori all'interno dell'heap fornito.

Quindi, usare una struttura di [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) per descrivere un heap sufficientemente grande per il numero di descrittori necessari per l'invio. Quindi crearlo con [**ID3D12Device:: CreateDescriptorHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap). Infine, chiamare [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) per associare l'heap del descrittore alla pipeline.

```cppwinrt
winrt::com_ptr<::ID3D12DescriptorHeap> d3D12DescriptorHeap;

D3D12_DESCRIPTOR_HEAP_DESC descriptorHeapDescription{};
descriptorHeapDescription.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
descriptorHeapDescription.NumDescriptors = descriptorCount;
descriptorHeapDescription.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;

winrt::check_hresult(
    d3D12Device->CreateDescriptorHeap(
        &descriptorHeapDescription,
        _uuidof(d3D12DescriptorHeap),
        d3D12DescriptorHeap.put_void()
    )
);

std::array<ID3D12DescriptorHeap*, 1> d3D12DescriptorHeaps{ d3D12DescriptorHeap.get() };
d3D12GraphicsCommandList->SetDescriptorHeaps(
    static_cast<UINT>(d3D12DescriptorHeaps.size()),
    d3D12DescriptorHeaps.data()
);
```

## <a name="describe-and-create-a-binding-table"></a>Descrivere e creare una tabella di associazione

Una tabella di binding DirectML rappresenta le risorse che si associano alla pipeline per un oggetto inviabile da usare. Tali risorse possono essere i tensori di input e di output (o altri parametri) per un operatore oppure possono essere diverse risorse permanenti e temporanee con cui può essere distribuito un oggetto inviabile.

Utilizzare la struttura [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) per descrivere la tabella di associazione, incluso il dispatcher per il quale la tabella di associazione rappresenterà le associazioni e l'intervallo di descrittori (dall'heap descrittore appena creato) a cui si desidera che la tabella di associazione faccia riferimento (e in cui DirectML può scrivere descrittori). Il `descriptorCount` valore (una delle proprietà di associazione recuperate nel primo passaggio) indica le dimensioni minime, nei descrittori, della tabella di associazione necessaria per l'oggetto inviabile. Questo valore viene usato per indicare il numero massimo di descrittori che DirectML è autorizzato a scrivere nell'heap, dall'inizio degli handle di descrittore della CPU e della GPU forniti.

Chiamare quindi [**IDMLDevice:: CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) per creare la tabella di associazione DirectML. Nei passaggi successivi, dopo aver creato ulteriori risorse per il dispatcher, le risorse verranno aggiunte alla tabella di binding.

Anziché passare un **DML_BINDING_TABLE_DESC** a questa chiamata, è possibile passare `nullptr` , che indica una tabella di binding vuota.

```cppwinrt
DML_BINDING_TABLE_DESC dmlBindingTableDesc{};
dmlBindingTableDesc.Dispatchable = dmlOperatorInitializer.get();
dmlBindingTableDesc.CPUDescriptorHandle = d3D12DescriptorHeap->GetCPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.GPUDescriptorHandle = d3D12DescriptorHeap->GetGPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.SizeInDescriptors = descriptorCount;

winrt::com_ptr<::IDMLBindingTable> dmlBindingTable;
winrt::check_hresult(
    dmlDevice->CreateBindingTable(
        &dmlBindingTableDesc,
        __uuidof(dmlBindingTable),
        dmlBindingTable.put_void()
    )
);
```

L'ordine in cui DirectML scrive i descrittori nell'heap non è specificato, pertanto l'applicazione deve prestare attenzione a non sovrascrivere i descrittori inclusi nella tabella di associazione. Gli handle di descrittore CPU e GPU forniti possono provenire da heap diversi, tuttavia è responsabilità dell'applicazione garantire che l'intero intervallo di descrittori a cui fa riferimento l'handle del descrittore della CPU venga copiato nell'intervallo a cui fa riferimento l'handle del descrittore della GPU prima dell'esecuzione utilizzando questa tabella di associazione. L'heap del descrittore da cui vengono forniti gli handle deve avere il tipo **D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV**. Inoltre, l'heap a cui fa riferimento `GPUDescriptorHandle` deve essere un heap del descrittore visibile allo shader.

È possibile reimpostare una tabella di binding per rimuovere tutte le risorse aggiunte, modificando allo stesso tempo qualsiasi proprietà impostata sul **DML_BINDING_TABLE_DESC** iniziale (per eseguire il wrapping di un nuovo intervallo di descrittori o per riutilizzarlo per un altro Dispatcher). È sufficiente apportare le modifiche alla struttura di descrizione e chiamare [**IDMLBindingTable:: Reset**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-reset).

```cppwinrt
dmlBindingTableDesc.Dispatchable = pIDMLCompiledOperator.get();

winrt::check_hresult(
    pIDMLBindingTable->Reset(
        &dmlBindingTableDesc
    )
);
```

## <a name="describe-and-bind-any-temporarypersistent-resources"></a>Descrivere e associare eventuali risorse temporanee/permanenti

La struttura di **DML_BINDING_PROPERTIES** popolata quando [sono state recuperate le proprietà di binding](#retrieve-the-binding-properties-of-a-dispatchable) dell'oggetto inviabile contiene la dimensione in byte di qualsiasi risorsa temporanea e/o persistente richiesta dal dispatcher. Se una di queste dimensioni è diversa da zero, creare una risorsa buffer Direct3D 12 e aggiungerla alla tabella di associazione.

Nell'esempio di codice riportato di seguito viene creata una risorsa temporanea, ovvero `temporaryResourceSize` byte, per l'oggetto inviabile. Viene descritto come si vuole associare la risorsa e quindi si aggiunge tale associazione alla tabella di associazione.

Poiché si sta associando una risorsa di buffer singola, viene descritta l'associazione con una struttura [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) . In tale struttura viene specificata la risorsa buffer Direct3D 12 (la risorsa deve avere [**D3D12_RESOURCE_DIMENSION_BUFFER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)di dimensione), nonché un offset e dimensioni nel buffer. È anche possibile descrivere un'associazione per una matrice di buffer (anziché per un singolo buffer) e la struttura [**DML_BUFFER_ARRAY_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding) esiste a tale scopo.

Per astrarre la distinzione tra un'associazione di buffer e un'associazione di matrici di buffer, viene usata la struttura  [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) . È possibile impostare il `Type` membro del **DML_BINDING_DESC** su [**DML_BINDING_TYPE_BUFFER**](/windows/desktop/api/directml/ne-directml-dml_binding_type) o **DML_BINDING_TYPE_BUFFER_ARRAY**. È quindi possibile impostare il `Desc` membro in modo che punti a un **DML_BUFFER_BINDING** o a un **DML_BUFFER_ARRAY_BINDING**, a seconda di `Type` .

In questo esempio si sta trattando della risorsa temporanea, quindi la si aggiunge alla tabella di binding con una chiamata a [**IDMLBindingTable:: BindTemporaryResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource).

```cppwinrt
D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
winrt::com_ptr<::ID3D12Resource> temporaryBuffer;

D3D12_RESOURCE_DESC temporaryBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(temporaryResourceSize) };
winrt::check_hresult(
    d3D12Device->CreateCommittedResource(
        &defaultHeapProperties,
        D3D12_HEAP_FLAG_NONE,
        &temporaryBufferDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        __uuidof(temporaryBuffer),
        temporaryBuffer.put_void()
    )
);

DML_BUFFER_BINDING bufferBinding{ temporaryBuffer.get(), 0, temporaryResourceSize };
DML_BINDING_DESC bindingDesc{ DML_BINDING_TYPE_BUFFER, &bufferBinding };
dmlBindingTable->BindTemporaryResource(&bindingDesc);
```

Una risorsa temporanea, se necessaria, è una memoria Scratch utilizzata internamente durante l'esecuzione dell'operatore, pertanto non è necessario preoccuparsi del suo contenuto. Non è quindi necessario mantenerla dopo che la chiamata a [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) è stata completata sulla GPU. Ciò significa che l'applicazione può rilasciare o sovrascrivere la risorsa temporanea tra gli invii dell'operatore compilato. L'intervallo di buffer specificato da associare come risorsa temporanea deve avere l'offset iniziale allineato a [**DML_TEMPORARY_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). Il tipo dell'heap sottostante al buffer deve essere **D3D12_HEAP_TYPE_DEFAULT**.

Se l'oggetto inviabile segnala una dimensione diversa da zero per la risorsa persistente più longeva, tuttavia, la procedura è leggermente diversa. È necessario creare un buffer e descrivere un'associazione che segue lo stesso modello illustrato in precedenza. Ma aggiungerlo alla tabella di associazione dell'inizializzatore di operatore con una chiamata a [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs), perché è il processo dell'inizializzatore di operatore a inizializzare la risorsa persistente. Quindi aggiungerlo alla tabella di binding dell'operatore compilato con una chiamata a [**IDMLBindingTable:: BindPersistentResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindpersistentresource). Vedere l'esempio di codice [dell'applicazione DirectML minimo](dml-min-app.md) per vedere il flusso di lavoro in azione. Il contenuto e la durata della risorsa persistente devono essere mantenuti fino a quando l'operatore compilato lo esegue. Ovvero, se un operatore richiede una risorsa persistente, l'applicazione deve fornirla durante l'inizializzazione e successivamente fornirla anche a tutte le esecuzioni future dell'operatore senza modificarne il contenuto. La risorsa persistente viene in genere utilizzata da DirectML per archiviare le tabelle di ricerca o altri dati di lunga durata calcolati durante l'inizializzazione di un operatore e riutilizzati nelle esecuzioni future dell'operatore. L'intervallo di buffer specificato da associare come buffer permanente deve avere l'offset iniziale allineato a [**DML_PERSISTENT_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). Il tipo dell'heap sottostante al buffer deve essere **D3D12_HEAP_TYPE_DEFAULT**.

## <a name="describe-and-bind-any-tensors"></a>Descrivere e associare tutti i tensori

Se si ha a che fare con un operatore compilato, anziché con un inizializzatore di operatore, è necessario associare le risorse di input e di output (per i tasti di scelta e altri parametri) alla tabella di binding dell'operatore. Il numero di binding deve corrispondere esattamente al numero di input dell'operatore, inclusi i Tenser facoltativi. I specifici tensori di input e di output e altri parametri accettati da un operatore sono documentati nell'argomento relativo a tale operatore (ad esempio, [**DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_identity_operator_desc)).

Una risorsa tensore è un buffer che contiene i singoli valori degli elementi del tensore. È possibile caricare e leggere tale buffer da e verso la GPU usando le normali tecniche di Direct3D 12 ([caricare le risorse](/windows/desktop/direct3d12/uploading-resources) e [leggere i dati tramite un buffer](/windows/desktop/direct3d12/readback-data-using-heaps)). Vedere l'esempio di codice [dell'applicazione DirectML minimo](dml-min-app.md) per vedere le tecniche in azione.

Infine, descrivere le associazioni di risorse di input e output con le strutture **DML_BUFFER_BINDING** e **DML_BINDING_DESC** , quindi aggiungerle alla tabella di binding dell'operatore compilato con le chiamate a [**IDMLBindingTable:: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) e [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs). Quando si chiama un metodo **IDMLBindingTable:: \* Bind* _, DirectML scrive uno o più descrittori nell'intervallo di descrittori della CPU.

```cppwinrt
DML_BUFFER_BINDING inputBufferBinding{ inputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC inputBindingDesc{ DML_BINDING_TYPE_BUFFER, &inputBufferBinding };
dmlBindingTable->BindInputs(1, &inputBindingDesc);

DML_BUFFER_BINDING outputBufferBinding{ outputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC outputBindingDesc{ DML_BINDING_TYPE_BUFFER, &outputBufferBinding };
dmlBindingTable->BindOutputs(1, &outputBindingDesc);
```

Uno dei passaggi per la creazione di un operatore DirectML (vedere [_ *IDMLDevice:: CreateOperator* *](/windows/desktop/api/directml/nf-directml-idmldevice-createoperator)) consiste nel dichiarare una o più strutture [**DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) per descrivere i buffer di dati del tensore che l'operatore accetta e restituisce. Nonché il tipo e le dimensioni del buffer di tensore, è possibile specificare facoltativamente il flag di [**DML_TENSOR_FLAG_OWNED_BY_DML**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags) .

**DML_TENSOR_FLAG_OWNED_BY_DML** indica che i dati del tensore devono essere di proprietà e gestiti da DirectML. DirectML crea una copia dei dati di tensore durante l'inizializzazione dell'operatore e la archivia nella risorsa persistente. Questo consente a DirectML di eseguire la riformattazione dei dati del tensore in altri moduli più efficienti. L'impostazione di questo flag può migliorare le prestazioni, ma è in genere utile solo per i tensori i cui dati non cambiano per la durata dell'operatore (ad esempio, i tensori di peso). E il flag può essere usato solo nei tensori di input. Quando il flag viene impostato su una particolare descrizione del tensore, il tensore corrispondente deve essere associato alla tabella di associazione durante l'inizializzazione dell'operatore e non durante l'esecuzione (che comporterà un errore). Si tratta dell'opposto del comportamento predefinito (il comportamento senza il flag di DML_TENSOR_FLAG_OWNED_BY_DML), in cui il tensore dovrebbe essere associato durante l'esecuzione e non durante l'inizializzazione. Quando si forniscono i dati del tensore a un inizializzatore di operatore, è lecito associare un caricamento anziché un heap predefinito, perché DirectML esegue una copia dei dati. In tutti gli altri casi, tutte le risorse vincolate a DirectML devono essere risorse heap predefinite.

Per altre informazioni, vedere [**IDMLBindingTable:: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) e [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs).

## <a name="execute-the-dispatchable"></a>Eseguire il dispatcher

Passare la tabella di associazione come parametro quando si chiama [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

Quando si utilizza la tabella di associazione durante una chiamata a **IDMLCommandRecorder:: RecordDispatch**, DirectML associa i descrittori GPU corrispondenti alla pipeline. Gli handle descrittore della CPU e della GPU non devono puntare alle stesse voci in un heap dei descrittori, tuttavia è responsabilità dell'applicazione garantire che l'intero intervallo di descrittori a cui fa riferimento l'handle del descrittore della CPU venga copiato nell'intervallo a cui fa riferimento l'handle del descrittore della GPU prima dell'esecuzione utilizzando questa tabella di associazione.

```cppwinrt
winrt::com_ptr<::ID3D12GraphicsCommandList> d3D12GraphicsCommandList;
// Code to create a Direct3D 12 command list goes here.

winrt::com_ptr<::IDMLCommandRecorder> dmlCommandRecorder;
// Code to create a DirectML command recorder goes here.

dmlCommandRecorder->RecordDispatch(
    d3D12GraphicsCommandList.get(),
    dmlOperatorInitializer.get(),
    dmlBindingTable.get()
);
```

Infine, chiudere l'elenco di comandi Direct3D 12 e inviarlo per l'esecuzione come qualsiasi altro elenco di comandi.

Prima dell'esecuzione di **RecordDispatch** sulla GPU, è necessario eseguire la transizione di tutte le risorse limitate allo stato **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** o a uno stato promuovibile in modo implicito a **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, ad esempio **D3D12_RESOURCE_STATE_COMMON**. Al termine della chiamata, le risorse rimangono nello stato **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . L'unica eccezione è rappresentata dagli heap di caricamento associati durante l'esecuzione di un inizializzatore di operatore e mentre uno o più tensori hanno il flag di **DML_TENSOR_FLAG_OWNED_BY_DML** impostato. In tal caso, gli heap di caricamento associati per l'input devono trovarsi nello stato **D3D12_RESOURCE_STATE_GENERIC_READ** e rimarranno in tale stato, come richiesto da tutti gli heap di caricamento. Se **DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE** non è stato impostato durante la compilazione dell'operatore, è necessario impostare tutte le associazioni nella tabella di binding prima della chiamata a **RecordDispatch** . in caso contrario, il comportamento non è definito. In caso contrario, se un operatore supporta l' [associazione tardiva](#optionally-specify-late-bound-operator-bindings), l'associazione delle risorse può essere rinviata fino a quando l'elenco di comandi Direct3D 12 non viene inviato alla coda dei comandi per l'esecuzione.

**RecordDispatch** agisce logicamente come una chiamata a [**ID3D12GraphicsCommandList::D la patch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch). Di conseguenza, le barriere per la visualizzazione di accesso non ordinato (UAV) sono necessarie per garantire l'ordinamento corretto in caso di dipendenze dei dati tra le invii. Questo metodo non inserisce le barriere UAV sulle risorse di input e di output. L'applicazione deve assicurarsi che vengano eseguite le barriere UAV corrette su tutti gli input se il contenuto dipende da un dispatch upstream e da eventuali output se sono presenti invii a valle che dipendono da tali output.

## <a name="lifetime-and-synchronization-of-descriptors-and-binding-table"></a>Durata e sincronizzazione dei descrittori e della tabella di associazione

Un modello mentale efficace di associazione in DirectML è che dietro le quinte la tabella di binding DirectML sta creando e gestendo descrittori UAV (unordered Access View) nell'heap del descrittore fornito. Quindi, tutte le normali regole Direct3D 12 riguardano la sincronizzazione dell'accesso a tale heap e ai relativi descrittori. È responsabilità dell'applicazione eseguire una sincronizzazione corretta tra il lavoro di CPU e GPU che usa una tabella di associazione.

Una tabella di associazione non può sovrascrivere un descrittore mentre il descrittore è in uso (ad esempio, da un frame precedente). Se quindi si vuole riusare un heap del descrittore già associato, ad esempio richiamando Bind * su una tabella di associazione che vi fa riferimento oppure sovrascrivendo manualmente l'heap del descrittore, è necessario attendere che il dispatcher stia usando l'heap del descrittore per completare l'esecuzione nella GPU. Una tabella di associazione non mantiene un riferimento sicuro nell'heap del descrittore in cui viene scritto, quindi non è necessario rilasciare l'heap del descrittore visibile dello shader, fino a quando tutto il lavoro che utilizza tale tabella di associazione non ha completato l'esecuzione nella GPU.

D'altra parte, mentre una tabella di associazione specifica e gestisce un heap del descrittore, la tabella non *contiene* alcuna memoria. È quindi possibile rilasciare o reimpostare una tabella di associazione in qualsiasi momento dopo aver chiamato [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) (non è necessario attendere il completamento di tale chiamata sulla GPU, purché i descrittori sottostanti rimangano validi).

La tabella di associazione non mantiene i riferimenti sicuri su tutte le risorse associate con esso &mdash; . l'applicazione deve assicurarsi che le risorse non vengano eliminate mentre sono ancora in uso dalla GPU. Inoltre, una tabella di binding non è thread-safe &mdash; . l'applicazione non deve chiamare metodi su una tabella di associazione simultaneamente da thread diversi senza sincronizzazione.

Si tenga presente che, in ogni caso, la riassociazione è necessaria solo quando si modificano le risorse associate. Se non è necessario modificare le risorse associate, è possibile eseguire il binding una volta all'avvio e passare la stessa tabella di associazione ogni volta che si chiama **RecordDispatch**.

Per l'interfoliazione dei carichi di lavoro di machine learning e di rendering, è sufficiente assicurarsi che le tabelle di binding di ogni frame puntino agli intervalli dell'heap del descrittore che non sono già in uso nella GPU.

## <a name="optionally-specify-late-bound-operator-bindings"></a>Facoltativamente, specificare associazioni di operatori ad associazione tardiva

Se si ha a che fare con un operatore compilato (anziché con un inizializzatore di operatore), è possibile specificare l'associazione tardiva per l'operatore. Senza associazione tardiva, è necessario impostare tutte le associazioni nella tabella di binding prima di registrare un operatore in un elenco di comandi. Con l'associazione tardiva, è possibile impostare o modificare le associazioni sugli operatori già registrati in un elenco di comandi, prima di essere inviati alla coda dei comandi.

Per specificare l'associazione tardiva, chiamare [**IDMLDevice:: CompileOperator**](/windows/win32/api/directml/nf-directml-idmldevice-compileoperator) con un `flags` argomento di [**DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE**](/windows/desktop/api/directml/ne-directml-dml_execution_flags).