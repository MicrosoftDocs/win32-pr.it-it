---
title: Creazione di una firma radice
description: Le firme radice sono una struttura di dati complessa contenente strutture annidate.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87209dfc324b950a74d2b31e5f1a1f6326792b9f
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826437"
---
# <a name="creating-a-root-signature"></a>Creazione di una firma radice

Le firme radice sono una struttura di dati complessa contenente strutture annidate. Questi elementi possono essere definiti a livello di codice usando la definizione della struttura dei dati riportata di seguito , che include metodi che consentono di inizializzare i membri. In alternativa, possono essere creati in HLSL (High Level Shading Language), offrendo il vantaggio che il compilatore convaliderà in anticipo che il layout è compatibile con lo shader.

L'API per la creazione di una firma radice accetta una versione serializzata (indipendente, senza puntatore) della descrizione del layout descritta di seguito. Viene fornito un metodo per generare questa versione serializzata dalla struttura di dati C++, ma un altro modo per ottenere una definizione di firma radice serializzata è recuperarla da uno shader compilato con una firma radice.

Per sfruttare le ottimizzazioni dei driver per i descrittori di firma radice e i dati, vedere Root Signature Version 1.1 (Versione della firma [radice 1.1)](root-signature-version-1-1.md)

-   [Tipi di associazione tabella descrittore](#descriptor-table-bind-types)
-   [Intervallo descrittore](#descriptor-range)
-   [Layout tabella descrittore](#descriptor-table-layout)
-   [Costanti radice](#root-constants)
-   [Descrittore radice](#root-descriptor)
-   [Visibilità dello shader](#shader-visibility)
-   [Definizione della firma radice](#root-signature-definition)
-   [Serializzazione/deserializzazione della struttura dei dati della firma radice](/windows)
-   [API di creazione della firma radice](#root-signature-creation-api)
-   [Firma radice negli oggetti di stato della pipeline](#root-signature-in-pipeline-state-objects)
-   [Codice per la definizione di una firma radice della versione 1.1](#code-for-defining-a-version-11-root-signature)
-   [Argomenti correlati](#related-topics)

## <a name="descriptor-table-bind-types"></a>Tipi di associazione tabella descrittore

L'enumerazione [**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) definisce i tipi di descrittori a cui è possibile fare riferimento come parte di una definizione di layout di tabella del descrittore.

Si tratta di un intervallo in modo che, ad esempio, se una parte di una tabella di descrittori ha 100 SRV, tale intervallo può essere dichiarato in una voce anziché in 100. Una definizione di tabella descrittore è quindi una raccolta di intervalli.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>Intervallo descrittore

La [**struttura D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definisce un intervallo di descrittori di un determinato tipo (ad esempio SRV) all'interno di una tabella di descrittori.

La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro può in genere essere usata per il parametro di `OffsetInDescriptorsFromTableStart` [**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Ciò significa aggiungere l'intervallo di descrittori definito dopo quello precedente nella tabella del descrittore. Se l'applicazione vuole creare l'alias dei descrittori o per qualche motivo vuole ignorare gli slot, può impostare `OffsetInDescriptorsFromTableStart` l'offset desiderato. La definizione di intervalli sovrapposti di tipi diversi non è valida.

Il set di registri shader specificato dalla combinazione di , , e non può essere in conflitto o sovrapporsi tra le dichiarazioni in una firma radice con visibilità `RangeType` `NumDescriptors` `BaseShaderRegister` `RegisterSpace` [**D3D12 \_ SHADER \_ comune**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (vedere la sezione relativa alla visibilità dello shader riportata di seguito).

## <a name="descriptor-table-layout"></a>Layout tabella descrittore

La [**struttura D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) dichiara il layout di una tabella descrittore come raccolta di intervalli di descrittori che vengono visualizzati uno dopo l'altro in un heap dei descrittori. I campionatori non sono consentiti nella stessa tabella descrittore di CBV/UAV/SRV.

Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Per impostare una tabella descrittore grafica (CBV, SRV, UAV, Sampler), usare [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Per impostare una tabella del descrittore di calcolo, usare [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Costanti radice

La [**struttura D3D12 \_ ROOT \_ CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) dichiara le costanti inline nella firma radice visualizzate negli shader come un unico buffer costante.

Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Descrittore radice

La [**struttura D3D12 \_ ROOT \_ DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) dichiara i descrittori (visualizzati negli shader) inline nella firma radice.

Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_CBV` `D3D12_ROOT_PARAMETER_TYPE_SRV` o `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Visibilità dello shader

Il membro dell'enumerazione [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) impostato nel parametro di visibilità dello shader [**di D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina quali shader visualizzano il contenuto di un determinato slot di firma radice. Il calcolo usa \_ sempre ALL (poiché è presente una sola fase attiva). La grafica può scegliere, ma se usa ALL, tutte le fasi dello shader vedono tutto ciò \_ che è associato allo slot della firma radice.

Un uso della visibilità dello shader è aiutare gli shader creati a aspettarsi associazioni diverse per ogni fase dello shader usando uno spazio dei nomi sovrapposto. Ad esempio, un vertex shader può dichiarare:

```hlsl
Texture2D foo : register(t0);
```

e il pixel shader può anche dichiarare:

```hlsl
Texture2D bar : register(t0);
```

Se l'applicazione crea un'associazione di firma radice a t0 VISIBILITY ALL, entrambi gli \_ shader visualizzano la stessa trama. Se lo shader definisce in realtà vuole che ogni shader veda trame diverse, può definire 2 slot di firma radice con VISIBILITY \_ VERTEX e \_ PIXEL. Indipendentemente dalla visibilità di uno slot di firma radice, ha sempre lo stesso costo (solo a seconda di SlotType) verso una dimensione massima fissa della firma radice.

Nell'hardware D3D11 di fascia bassa, anche SHADER VISIBILITY viene preso in considerazione quando si convalidano le dimensioni delle tabelle descrittore in un layout radice, poiché alcuni componenti hardware D3D11 possono supportare solo una quantità massima di \_ associazioni per fase. Queste restrizioni vengono imposte solo quando vengono eseguite su hardware di basso livello e non limitano affatto l'hardware più moderno.

Se in una firma radice sono definite più tabelle descrittori che si sovrappongono tra loro nello spazio dei nomi (le associazioni di registro allo shader) e una di esse specifica ALL per la visibilità, il layout non è valido (la creazione avrà esito \_ negativo).

## <a name="root-signature-definition"></a>Definizione della firma radice

La struttura [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) può contenere tabelle descrittori e costanti inline, ogni tipo di slot definito dalla struttura [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) e dall'enumerazione [**D3D12 \_ ROOT PARAMETER \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).

Per avviare uno slot di firma radice, vedere i **metodi SetComputeRoot \* \* \*** e **\* \* \* SetGraphicsRoot** di [**ID3D12GraphicsCommandList.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)

I campionatori statici sono descritti nella firma radice usando la [**struttura D3D12 \_ STATIC \_ SAMPLER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)

Alcuni flag limitano l'accesso di determinati shader alla firma radice, fare riferimento a [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Serializzazione/deserializzazione della struttura dei dati della firma radice

I metodi descritti in questa sezione vengono esportati da D3D12Core.dll e forniscono metodi per la serializzazione e la deserializzazione di una struttura di dati della firma radice.

Il formato serializzato è ciò che viene passato all'API durante la creazione di una firma radice. Se uno shader è stato creato con una firma radice (quando tale funzionalità viene aggiunta), lo shader compilato conterrà già una firma radice serializzata.

Se un'applicazione genera in modo procedurale una struttura di dati [**\_ \_ \_ DESC D3D12 ROOT SIGNATURE,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deve eseguire il modulo serializzato usando [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature). Output di che può essere passato in [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).

Se un'applicazione ha già una firma radice serializzata o ha uno shader compilato che contiene una firma radice e vuole individuare a livello di codice la definizione di layout (nota come "reflection"), è possibile chiamare [**D3D12CreateRootSignatureDeserializer.**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) Viene generata [**un'interfaccia ID3D12RootSignatureDeserializer,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) che contiene un metodo per restituire la struttura di dati [**DESC D3D12 \_ ROOT SIGNATURE \_ \_ deserializzata.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) L'interfaccia è proprietaria della durata della struttura dei dati deserializzata.

## <a name="root-signature-creation-api"></a>API di creazione della firma radice

[**L'API ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) accetta una versione serializzata di una firma radice.

## <a name="root-signature-in-pipeline-state-objects"></a>Firma radice negli oggetti di stato della pipeline

I metodi per creare lo stato della pipeline ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) accettano un'interfaccia [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) facoltativa come parametro di input (archiviato in una struttura [**DESC D3D12 \_ GRAPHICS PIPELINE \_ \_ STATE). \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) Verrà eseguito l'override di qualsiasi firma radice già presente negli shader.

Se una firma radice viene passata in uno dei metodi di creazione dello stato della pipeline, questa firma radice viene convalidata in base a tutti gli shader nell'oggetto PSO per la compatibilità e viene data al driver da usare con tutti gli shader. Se uno degli shader ha una firma radice diversa, viene sostituito dalla firma radice passata all'API. Se non viene passata una firma radice, tutti gli shader passati devono avere una firma radice e devono corrispondere. Questo verrà assegnato al driver. L'impostazione di un oggetto PSO in un elenco di comandi o in un bundle non modifica la firma radice. Questa operazione viene eseguita dai metodi [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) [**e SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature). Quando viene richiamato time draw(graphics)/dispatch(compute), l'applicazione deve assicurarsi che l'oggetto PSO corrente corrisponda alla firma radice corrente. In caso contrario, il comportamento non è definito.

## <a name="code-for-defining-a-version-11-root-signature"></a>Codice per la definizione di una firma radice della versione 1.1

L'esempio seguente illustra come creare una firma radice con il formato seguente:



| RootParameterIndex                       | Contenuto                                               | Valori                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| \[0\]                  | Costanti radice: { b2 }                         | (1 CBV)                                      |
| \[1\]                  | Tabella del descrittore: { t2-t7, u0-u3 }             | (6 SRV + 4 UAV)                            |
| \[2\]                  | CBV radice: { b0 }                               | (1 CBV, dati statici)                         |
| \[3\]                  | Tabella del descrittore: { s0-s1 }                    | (2 campionatori)                                 |
| \[4\]                  | Tabella dei descrittori: { t8 - unbounded }           | (senza associazione \# di SRV, descrittori volatili) |
| \[5\]                  | Tabella dei descrittori: { (t0, space1) - unbounded } | (senza associazione \# di SRV, descrittori volatili) |
| \[6\]                  | Tabella dei descrittori: { b1 }                       | (1 CBV, dati statici)                         |



 

Se la maggior parte delle parti della firma radice viene usata nella maggior parte dei casi, può essere meglio che cambiare la firma radice troppo frequentemente. Le applicazioni devono ordinare le voci nella firma radice dalla più frequente alla meno frequente. Quando un'app modifica le associazioni in una parte qualsiasi della firma radice, il driver potrebbe avere la funzione di creare una copia di uno o tutti gli stati della firma radice, che possono diventare un costo non aggiuntivo se moltiplicato tra molte modifiche di stato.

Inoltre, la firma radice definirà un campionatore statico che esegue il filtro della trama anisotropo nel registro shader s3.

Dopo l'associazione di questa firma radice, le tabelle dei descrittori, la radice CBV e le costanti possono essere assegnate allo spazio dei parametri \[ 0..6. \] Ad esempio, le tabelle dei descrittori (intervalli in un heap descrittore) possono essere associate a ognuno dei parametri radice \[ 1 \] e \[ 3..6. \]

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

Il codice seguente illustra come usare la firma radice precedente in un elenco di comandi grafici.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(2,pHeaps);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Firme radice](root-signatures.md)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[Uso di una firma radice](using-a-root-signature.md)
</dt> </dl>

 

 
