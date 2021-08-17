---
title: Oggetti di stato
description: Usare HLSL per definire gli oggetti di stato.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70ff3ca1fb2509cd5f788cc1965920c46af5791bec10bb833df19f4b4f9be533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119935"
---
# <a name="state-objects"></a>Oggetti di stato

Con i modelli di shader 6.3 e versioni successive, le applicazioni hanno la praticità e la flessibilità di poter definire oggetti di stato DXR direttamente nel codice dello shader HLSL oltre a usare le API Direct3D 12.

In HLSL gli oggetti di stato vengono dichiarati con questa sintassi:

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**digitare**<br/>     | Identifica il tipo di oggetto secondario. Deve essere uno dei tipi di oggetto secondario HLSL supportati.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**<br/> | Campi del sottooggetto. I campi specifici per ogni tipo di oggetto secondario sono descritti di seguito.<br/> |




Elenco di tipi di oggetti secondari:
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

Il tipo di oggetto secondario StateObjectConfig corrisponde a una [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) struttura .

Ha un campo, un flag bit per bit, che è uno o entrambi

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

oppure zero per nessuno di essi.

Esempio:

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>GlobalRootSignature
GlobalRootSignature corrisponde a una [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) struttura .

I campi sono costituiti da alcune stringhe che descrivono le parti della firma radice. Per informazioni di riferimento, vedere [Specifica delle firme radice in HLSL.](../direct3d12/specifying-root-signatures-in-hlsl.md)

Esempio:
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a>LocalRootSignature
LocalRootSignature corrisponde a una [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) struttura .

Proprio come il sottooggetto di firma radice globale, i campi sono costituiti da alcune stringhe che descrivono le parti della firma radice. Per informazioni di riferimento, vedere [Specifica delle firme radice in HLSL.](../direct3d12/specifying-root-signatures-in-hlsl.md)

Esempio:
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
Per impostazione predefinita, un oggetto secondario semplicemente dichiarato nella stessa libreria di un'esportazione può essere applicato a tale esportazione. Tuttavia, le applicazioni hanno la possibilità di eseguire l'override e ottenere informazioni specifiche sull'oggetto secondario associato all'esportazione. In HLSL questa "associazione esplicita" viene eseguita usando SubobjectToExportsAssocation.

SubobjectToExportsAssocation corrisponde a una [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) struttura .

Questo oggetto secondario viene dichiarato con la sintassi

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**<br/>     | Stringa che identifica un oggetto secondario esportato.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Esportazioni**<br/> | Stringa contenente un elenco delimitato da punto e virgola di esportazioni.<br/> |


Esempio:
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Si noti che entrambi i campi *usano nomi esportati.* Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione dell'esportazione.

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

RaytracingShaderConfig corrisponde a una [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) struttura .

Questo oggetto secondario viene dichiarato con la sintassi

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | Valore numerico per lo spazio di archiviazione massimo per i valori scalari (con conteggio di 4 byte ciascuno) nei payload di raggio per gli shader di raytracing associati.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | Valore numerico per il numero massimo di scalari (conteggiati come 4 byte ciascuno) che possono essere usati per gli attributi negli shader di raytracing associati. Il valore non può superare [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).<br/> |


Esempio:
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

RaytracingPipelineConfig corrisponde a una [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) struttura .

Questo oggetto secondario viene dichiarato con la sintassi

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Limite numerico da usare per la ricorsione di raggi nella pipeline di raytracing. È un numero compreso tra 0 e 31 inclusi. <br/> |


Esempio:
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Poiché la ricorsione di raytracing comporta un costo in termini di prestazioni, le applicazioni devono usare la profondità di ricorsione più bassa necessaria per i risultati desiderati.

Se le chiamate dello shader non hanno ancora raggiunto la profondità massima della ricorsione, possono chiamare [TraceRay](../direct3d12/traceray-function.md) un numero qualsiasi di volte. Tuttavia, se raggiungono o superano la profondità massima della ricorsione, chiamando TraceRay il dispositivo viene rimosso. Pertanto, gli shader di raytracing devono smettere di chiamare TraceRay se hanno raggiunto o superato la profondità massima della ricorsione.

## <a name="trianglehitgroup"></a>TriangleHitGroup

TriangleHitGroup corrisponde a una [struttura D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) il cui campo Type è impostato [su D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Questo oggetto secondario viene dichiarato con la sintassi

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nome della stringa dello shader anyhit per il gruppo di hit o una stringa vuota.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nome della stringa dell'hit shader più vicino per il gruppo di hit o una stringa vuota.<br/> |


Esempio:
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Si noti che entrambi i campi *usano nomi esportati.* Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione dell'esportazione.

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

Un elemento ProcedurelPrimitiveHitGroup corrisponde a una [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) il cui campo Type è impostato [su D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Questo oggetto secondario viene dichiarato con la sintassi

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nome della stringa dello shader anyhit per il gruppo di hit o una stringa vuota.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nome della stringa dell'hit shader più vicino per il gruppo di hit o una stringa vuota.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | Nome di stringa dello shader di intersezione per il gruppo di hit o una stringa vuota.<br/> |


Esempio:
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Si noti che i tre campi usano *nomi esportati.* Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione dell'esportazione.

## <a name="remarks"></a>Commenti

I sottooggetti hanno il concetto di "associazione" o "oggetto secondario con cui esportare".

Quando si specificano oggetti secondari tramite il codice dello shader, la scelta di "quale oggetto secondario viene associato all'esportazione" segue le regole descritte nella [specifica DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior). In particolare, si supponga che un'applicazione abbia un'esportazione. Se un'applicazione associa l'esportazione alla firma radice A tramite il codice shader e la firma radice B tramite il codice dell'applicazione, B è quella che viene usata. La progettazione di "usare B" invece di "generare un errore" offre alle applicazioni la possibilità di eseguire l'override pratico delle associazioni DXIL usando il codice dell'applicazione, anziché essere obbligate a ricompilare gli shader per risolvere gli elementi non corrispondenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Post di blog per sviluppatori DirectX "Novità di D3D12 - DirectX Raytracing (DXR) supporta ora oggetti secondari della libreria"](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Specifica funzionale di DirectX Raytracing (DXR)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Esempio: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>