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
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995285"
---
# <a name="state-objects"></a>Oggetti di stato

Con i modelli shader 6,3 e versioni successive, le applicazioni offrono la convenienza e la flessibilità di poter definire gli oggetti di stato DXR direttamente nel codice dello shader HLSL, oltre a usare le API Direct3D 12.

In HLSL, gli oggetti di stato vengono dichiarati con la sintassi seguente:

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
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**<br/>     | Identifica il tipo di oggetto SubObject. Deve essere uno dei tipi di sottooggetto HLSL supportati.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Campo [1, 2,...]**<br/> | Campi dell'oggetto SubObject. Di seguito sono descritti i campi specifici per ogni tipo di oggetto.<br/> |




Elenco di tipi di oggetti SubObject:
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

Il tipo di sottooggetto StateObjectConfig corrisponde a una struttura [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .

Include un campo, un flag bit per bit, che è uno o entrambi

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

oppure, zero per nessuno di essi.

Esempio:

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>GlobalRootSignature
Un GlobalRootSignature corrisponde a una struttura [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .

I campi sono costituiti da un certo numero di stringhe che descrivono le parti della firma radice. Per riferimento, vedere Specifica delle [firme radice in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

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
Un LocalRootSignature corrisponde a una struttura [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .

Analogamente al sottooggetto della firma radice globale, i campi sono costituiti da un certo numero di stringhe che descrivono le parti della firma radice. Per riferimento, vedere Specifica delle [firme radice in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Esempio:
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
Per impostazione predefinita, un sottooggetto dichiarato semplicemente nella stessa libreria di un'esportazione è in grado di applicare a tale esportazione. Tuttavia, le applicazioni hanno la possibilità di eseguire l'override di tale oggetto e di ottenere informazioni specifiche su quale elemento SubObject viene utilizzato per l'esportazione. In HLSL questa "associazione esplicita" viene eseguita tramite SubobjectToExportsAssocation.

Un SubobjectToExportsAssocation corrisponde a una struttura [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .

Questo sottooggetto viene dichiarato con la sintassi

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
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**Subobjectname**<br/>     | Stringa che identifica un sottooggetto esportato.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Esporta**<br/> | Stringa contenente un elenco delimitato da punti e virgola delle esportazioni.<br/> |


Esempio:
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Si noti che entrambi i campi utilizzano nomi *esportati* . Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione delle esportazioni.

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

Un RaytracingShaderConfig corrisponde a una struttura [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .

Questo sottooggetto viene dichiarato con la sintassi

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
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | Valore numerico per lo spazio di archiviazione massimo per i valori scalari (conteggiati come 4 byte ciascuno) nei payload del raggio per gli shader raytracing associati.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | Valore numerico per il numero massimo di scalari (conteggiato come 4 byte ciascuno) che può essere usato per gli attributi negli shader raytracing associati. Il valore non può superare [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).<br/> |


Esempio:
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

Un RaytracingPipelineConfig corrisponde a una struttura [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .

Questo sottooggetto viene dichiarato con la sintassi

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Limite numerico da usare per la ricorsione dei raggi nella pipeline raytracing. Si tratta di un numero compreso tra 0 e 31, inclusi. <br/> |


Esempio:
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Poiché la ricorsione raytracing comporta un costo in termini di prestazioni, le applicazioni devono utilizzare la profondità di ricorsione più bassa necessaria per i risultati desiderati.

Se le chiamate dello shader non hanno ancora raggiunto la profondità massima di ricorsione, possono chiamare [TraceRay](../direct3d12/traceray-function.md) per un numero qualsiasi di volte. Tuttavia, se raggiungono o superano la profondità massima di ricorsione, la chiamata di TraceRay comporta lo stato rimosso del dispositivo. Di conseguenza, gli shader raytracing devono interrompere la chiamata a TraceRay se hanno raggiunto o superato la profondità massima di ricorsione.

## <a name="trianglehitgroup"></a>TriangleHitGroup

Un TriangleHitGroup corrisponde a una struttura [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) il cui campo di tipo è impostato su [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Questo sottooggetto viene dichiarato con la sintassi

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
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nome di stringa dello shader anyhit per il gruppo di hit o una stringa vuota.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nome di stringa dell'hit shader più vicino per il gruppo di hit o una stringa vuota.<br/> |


Esempio:
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Si noti che entrambi i campi utilizzano nomi *esportati* . Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione delle esportazioni.

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

Un ProceduralPrimitiveHitGroup corrisponde a una struttura [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) il cui campo di tipo è impostato su [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Questo sottooggetto viene dichiarato con la sintassi

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
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nome di stringa dello shader anyhit per il gruppo di hit o una stringa vuota.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nome di stringa dell'hit shader più vicino per il gruppo di hit o una stringa vuota.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | Nome di stringa dell'intersezione shader per il gruppo di hit o una stringa vuota.<br/> |


Esempio:
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Si noti che i tre campi utilizzano i nomi *esportati* . Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione delle esportazioni.

## <a name="remarks"></a>Commenti

Gli oggetti subobjects hanno la nozione di "Association" o "quale SubObject passa con quale esportazione".

Quando si specificano sottooggetti tramite il codice dello shader, la scelta di "quale oggetto SubObject passa con l'esportazione" segue le regole descritte nella [specifica DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior). In particolare, si supponga che un'applicazione abbia alcune esportazioni. Se un'applicazione associa l'esportazione con la firma radice A tramite shader-code e la firma radice B tramite il codice dell'applicazione, B è quello che viene usato. La progettazione di "use B" invece di "generate an error" offre alle applicazioni la possibilità di eseguire facilmente l'override delle associazioni DXIL usando il codice dell'applicazione, anziché forzare la ricompilazione degli shader per risolvere gli elementi non corrispondenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Post di Blog per sviluppatori DirectX "Novità in D3D12-DirectX raytracing (DXR) supporta ora gli oggetti sottooggetti della libreria"](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Specifiche funzionali DirectX raytracing (DXR)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Esempio: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>