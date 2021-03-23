---
title: Creazione di una firma radice
description: Le firme radice sono una struttura di dati complessa contenente strutture annidate.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9660f35c349342d147a61a6b4ce9c02a4a1abab
ms.sourcegitcommit: 65af948af39d1a31885a1b688f5dbfe955d7eba1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/18/2020
ms.locfileid: "104548802"
---
# <a name="creating-a-root-signature"></a>Creazione di una firma radice

Le firme radice sono una struttura di dati complessa contenente strutture annidate. Questi possono essere definiti a livello di codice usando la definizione della struttura di dati riportata di seguito, che include i metodi per inizializzare i membri. In alternativa, possono essere creati in HLSL (High Level Shading Language), offrendo il vantaggio che il compilatore convaliderà in anticipo che il layout è compatibile con lo shader.

L'API per la creazione di una firma radice accetta una versione serializzata (autonoma, senza puntatore) della descrizione del layout descritta di seguito. Viene fornito un metodo per generare la versione serializzata dalla struttura dei dati C++, ma un altro modo per ottenere una definizione della firma radice serializzata consiste nel recuperarla da uno shader compilato con una firma radice.

Per sfruttare i vantaggi delle ottimizzazioni dei driver per i descrittori e i dati della firma radice, vedere la pagina relativa alla [firma radice versione 1,1](root-signature-version-1-1.md)

-   [Tipi di binding tabella descrittore](#descriptor-table-bind-types)
-   [Intervallo descrittori](#descriptor-range)
-   [Layout tabella descrittore](#descriptor-table-layout)
-   [Costanti radice](#root-constants)
-   [Descrittore radice](#root-descriptor)
-   [Visibilità shader](#shader-visibility)
-   [Definizione della firma radice](#root-signature-definition)
-   [Serializzazione/deserializzazione della struttura dei dati della firma radice](/windows)
-   [API di creazione della firma radice](#root-signature-creation-api)
-   [Firma radice negli oggetti stato della pipeline](#root-signature-in-pipeline-state-objects)
-   [Codice per la definizione di una firma radice della versione 1,1](#code-for-defining-a-version-11-root-signature)
-   [Argomenti correlati](#related-topics)

## <a name="descriptor-table-bind-types"></a>Tipi di binding tabella descrittore

Il [**tipo di \_ \_ intervallo \_ descrittore D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) enum definisce i tipi di descrittori a cui è possibile fare riferimento come parte di una definizione del layout della tabella del descrittore.

Si tratta di un intervallo in modo che, ad esempio, se parte di una tabella descrittore presenta 100 SRVs, tale intervallo può essere dichiarato in una voce anziché 100. Una definizione di tabella del descrittore è quindi una raccolta di intervalli.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>Intervallo descrittori

La struttura dell' [**\_ \_ intervallo di descrittori D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definisce un intervallo di descrittori di un determinato tipo (ad esempio SRVs) all'interno di una tabella del descrittore.

La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro può essere utilizzata in genere per il `OffsetInDescriptorsFromTableStart` parametro [**dell' \_ \_ intervallo di descrittori D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Questo significa accodare l'intervallo del descrittore che viene definito dopo quello precedente nella tabella del descrittore. Se l'applicazione vuole descrittori di alias o per qualche motivo vuole ignorare gli slot, può impostare `OffsetInDescriptorsFromTableStart` su qualsiasi offset desiderato. La definizione di intervalli sovrapposti di tipi diversi non è valida.

Il set di registri dello shader specificato dalla combinazione di `RangeType` , `NumDescriptors` , `BaseShaderRegister` e `RegisterSpace` non può essere in conflitto o sovrapposto a qualsiasi dichiarazione in una firma radice con [**\_ \_ visibilità D3D12 shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) comune. vedere la sezione relativa alla visibilità dello shader riportata di seguito.

## <a name="descriptor-table-layout"></a>Layout tabella descrittore

La struttura della [**\_ \_ \_ tabella descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) dichiara il layout di una tabella dei descrittori come una raccolta di intervalli di descrittori che vengono visualizzati uno dopo l'altro in un heap del descrittore. I sampler non sono consentiti nella stessa tabella dei descrittori di CBV/UAV/SRVs.

Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Per impostare una tabella del descrittore Graphics (CBV, SRV, UAV, Sampler), usare [**ID3D12GraphicsCommandList:: SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Per impostare una tabella del descrittore di calcolo, utilizzare [**ID3D12GraphicsCommandList:: SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Costanti radice

La struttura delle [**\_ \_ costanti radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) dichiara le costanti inline nella firma radice che vengono visualizzate in shader come un buffer costante.

Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Descrittore radice

La struttura del [**\_ \_ descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) dichiara i descrittori (visualizzati in shader) inline nella firma radice.

Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` o `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Visibilità shader

Il membro dell'enumerazione di [**\_ \_ visibilità dello shader D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) impostato nel parametro di visibilità dello shader [**del \_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina gli shader che visualizzano il contenuto di uno slot di firma radice specificato. Il calcolo usa sempre \_ tutti (poiché esiste una sola fase attiva). La grafica può scegliere, ma se usa \_ tutto, tutte le fasi dello shader visualizzano qualsiasi elemento associato allo slot della firma radice.

Un uso della visibilità dello shader è aiutare gli shader creati in attesa di associazioni diverse per ogni fase dello shader usando uno spazio dei nomi sovrapposto. Un vertex shader, ad esempio, può dichiarare:

 

Texture2D foo: Register (T0); "

 

il pixel shader Inoltre può dichiarare:

 

Barra Texture2D: Register (T0);

Se l'applicazione crea un binding della firma radice a T0 VISIBILITY \_ All, entrambi gli shader visualizzano la stessa trama. Se lo shader definisce in realtà che ogni shader può visualizzare trame diverse, può definire due slot di firma radice con il \_ vertice e il \_ pixel di visibilità. Indipendentemente dalla visibilità in uno slot di firma radice, ha sempre lo stesso costo (costo solo a seconda del valore di SlotType) verso una dimensione massima della firma radice fissa.

Nell'hardware D3D11 di fascia bassa, \_ viene presa in considerazione anche la visibilità dello shader usato per la convalida delle dimensioni delle tabelle dei descrittori in un layout radice, poiché alcuni componenti hardware d3d11 possono supportare solo una quantità massima di binding per fase. Queste restrizioni vengono imposte solo quando si esegue l'hardware a basso livello e non si limitano l'hardware più moderno.

Se per una firma radice sono state definite più tabelle dei descrittori che si sovrappongono tra loro nello spazio dei nomi (i binding Register allo shader) e in uno di essi \_ viene specificato all per Visibility, il layout non è valido (la creazione avrà esito negativo).

## <a name="root-signature-definition"></a>Definizione della firma radice

La [**struttura \_ \_ \_ desc della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) può contenere tabelle descrittore e costanti inline, ogni tipo di slot definito dalla struttura del [**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) e dal [**\_ \_ \_ tipo di parametro radice enum D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).

Per avviare uno slot di firma radice, fare riferimento ai **metodi \* \* \* SetComputeRoot** e **SetGraphicsRoot \* \* \*** di [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

I sampler statici sono descritti nella firma radice usando la struttura del [**\_ \_ campionatore statico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

Un numero di flag che limitano l'accesso di determinati shader alla firma radice, fanno riferimento [**ai \_ \_ \_ flag della firma radice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Serializzazione/deserializzazione della struttura dei dati della firma radice

I metodi descritti in questa sezione sono esportati da D3D12Core.dll e forniscono metodi per la serializzazione e la deserializzazione di una struttura di dati della firma radice.

Il modulo serializzato è quello che viene passato all'API quando si crea una firma radice. Se uno shader è stato creato con una firma radice (quando tale funzionalità viene aggiunta), lo shader compilato conterrà già una firma radice serializzata.

Se un'applicazione genera in modo procedurale una struttura dei dati [**\_ \_ \_ desc della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , deve creare il modulo serializzato usando [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature). L'output di che può essere passato in [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).

Se un'applicazione ha già una firma radice serializzata o ha uno shader compilato che contiene una firma radice e desidera individuare a livello di codice la definizione del layout (nota come "Reflection"), è possibile chiamare [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) . Viene generata un'interfaccia [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , che contiene un metodo per restituire la struttura dei dati [**della \_ \_ firma radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserializzata. L'interfaccia possiede la durata della struttura dei dati deserializzati.

## <a name="root-signature-creation-api"></a>API di creazione della firma radice

L'API [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) accetta una versione serializzata di una firma radice.

## <a name="root-signature-in-pipeline-state-objects"></a>Firma radice negli oggetti stato della pipeline

I metodi per creare lo stato della pipeline ([**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) accettano un'interfaccia [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) facoltativa come parametro di input (archiviato in una struttura di [**\_ \_ \_ \_ Descrizione dello stato della pipeline grafica D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ). Verrà eseguito l'override di qualsiasi firma radice già presente negli shader.

Se una firma radice viene passata in uno dei metodi di stato di creazione della pipeline, la firma radice viene convalidata rispetto a tutti gli shader nell'oggetto PSO per la compatibilità e viene fornita al driver da usare con tutti gli shader. Se uno qualsiasi degli shader presenta una firma radice diversa, viene sostituito dalla firma radice passata all'API. Se non viene passata una firma radice, tutti gli shader passati devono avere una firma radice e devono corrispondere, che verrà assegnato al driver. L'impostazione di un oggetto PSO in un elenco di comandi o in un bundle non comporta la modifica della firma radice. Questa operazione viene eseguita dai metodi [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) e [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature). Quando viene richiamato/dispatch (Compute), l'applicazione deve verificare che il PSO corrente corrisponda alla firma radice corrente. in caso contrario, il comportamento non è definito.

## <a name="code-for-defining-a-version-11-root-signature"></a>Codice per la definizione di una firma radice della versione 1,1

Nell'esempio seguente viene illustrato come creare una firma radice con il formato seguente:



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| **RootParameterIndex** | **Contents**                                   |                                              |
| \[0\]                  | Costanti radice: {B2}                         | (1 CBV)                                      |
| \[1\]                  | Tabella descrittore: {T2-T7, U0-U3}             | (6 SRVs + 4 UAV)                            |
| \[2\]                  | CBV radice: {B0}                               | (1 CBV, dati statici)                         |
| \[3\]                  | Tabella descrittore: {S0-S1}                    | (2 Samplers)                                 |
| \[4\]                  | Tabella descrittore: {T8-unbounded}           | (non associato \# a SRVs, descrittori volatili) |
| \[5\]                  | Tabella descrittore: {(T0, space1)-unbounded} | (non associato \# a SRVs, descrittori volatili) |
| \[6\]                  | Tabella descrittore: {B1}                       | (1 CBV, dati statici)                         |



 

Se la maggior parte delle parti della firma radice viene utilizzata la maggior parte del tempo, può essere preferibile rispetto alla necessità di cambiare troppo spesso la firma radice. Le applicazioni devono ordinare le voci della firma radice dal passaggio più frequente al minore. Quando un'applicazione modifica i binding in qualsiasi parte della firma radice, il driver potrebbe dover creare una copia di alcuni o tutti gli Stati della firma radice, il che può diventare un costo non semplice quando viene moltiplicato per molte modifiche di stato.

Inoltre, la firma radice definirà un campionatore statico che esegue il filtro di trama anisotropico al registro shader S3.

Una volta associata la firma radice, le tabelle di descrittore, CBV radice e costanti possono essere assegnate allo \[ spazio dei parametri 0.. 6 \] . ad esempio, le tabelle dei descrittori (intervalli in un heap del descrittore) possono essere associati a ogni parametro radice \[ 1 \] e \[ 3.. 6 \] .

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

Il codice seguente illustra come può essere usata la firma radice precedente in un elenco di comandi di grafica.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
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

 

 
