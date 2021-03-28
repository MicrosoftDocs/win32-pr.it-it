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
# <a name="state-objects"></a><span data-ttu-id="16629-103">Oggetti di stato</span><span class="sxs-lookup"><span data-stu-id="16629-103">State Objects</span></span>

<span data-ttu-id="16629-104">Con i modelli shader 6,3 e versioni successive, le applicazioni offrono la convenienza e la flessibilità di poter definire gli oggetti di stato DXR direttamente nel codice dello shader HLSL, oltre a usare le API Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="16629-104">With shader models 6.3 and later, applications have the convenience and flexibility of being able to define DXR state objects directly in HLSL shader code in addition to using Direct3D 12 APIs.</span></span>

<span data-ttu-id="16629-105">In HLSL, gli oggetti di stato vengono dichiarati con la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="16629-105">In HLSL, state objects are declared with this syntax:</span></span>

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| <span data-ttu-id="16629-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="16629-106">Item</span></span>                                                                                         | <span data-ttu-id="16629-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16629-107">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16629-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16629-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="16629-109">Identifica il tipo di oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="16629-109">Identifies the type of subobject.</span></span> <span data-ttu-id="16629-110">Deve essere uno dei tipi di sottooggetto HLSL supportati.</span><span class="sxs-lookup"><span data-stu-id="16629-110">Must be one of the supported HLSL subobject types.</span></span><br/>     |
| <span data-ttu-id="16629-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="16629-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="16629-112">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="16629-112">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="16629-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Campo [1, 2,...]**</span><span class="sxs-lookup"><span data-stu-id="16629-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**</span></span><br/> | <span data-ttu-id="16629-114">Campi dell'oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="16629-114">Fields of the subobject.</span></span> <span data-ttu-id="16629-115">Di seguito sono descritti i campi specifici per ogni tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="16629-115">Specific fields for each type of subobject are described below.</span></span><br/> |




<span data-ttu-id="16629-116">Elenco di tipi di oggetti SubObject:</span><span class="sxs-lookup"><span data-stu-id="16629-116">List of subobject types:</span></span>
-   [<span data-ttu-id="16629-117">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="16629-117">StateObjectConfig</span></span>](#stateobjectconfig)
-   [<span data-ttu-id="16629-118">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="16629-118">GlobalRootSignature</span></span>](#globalrootsignature)
-   [<span data-ttu-id="16629-119">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="16629-119">LocalRootSignature</span></span>](#localrootsignature)
-   [<span data-ttu-id="16629-120">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="16629-120">SubobjectToExportsAssocation</span></span>](#subobjecttoexportsassocation)
-   [<span data-ttu-id="16629-121">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="16629-121">RaytracingShaderConfig</span></span>](#raytracingshaderconfig)
-   [<span data-ttu-id="16629-122">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="16629-122">RaytracingPipelineConfig</span></span>](#raytracingpipelineconfig)
-   [<span data-ttu-id="16629-123">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="16629-123">TriangleHitGroup</span></span>](#trianglehitgroup)
-   [<span data-ttu-id="16629-124">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="16629-124">ProceduralPrimitiveHitGroup</span></span>](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a><span data-ttu-id="16629-125">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="16629-125">StateObjectConfig</span></span>

<span data-ttu-id="16629-126">Il tipo di sottooggetto StateObjectConfig corrisponde a una struttura [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .</span><span class="sxs-lookup"><span data-stu-id="16629-126">The StateObjectConfig subobject type corresponds to a [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) structure.</span></span>

<span data-ttu-id="16629-127">Include un campo, un flag bit per bit, che è uno o entrambi</span><span class="sxs-lookup"><span data-stu-id="16629-127">It has one field, a bitwise flag, which is one or both of</span></span>

* <span data-ttu-id="16629-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span><span class="sxs-lookup"><span data-stu-id="16629-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span></span>
* <span data-ttu-id="16629-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span><span class="sxs-lookup"><span data-stu-id="16629-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span></span>

<span data-ttu-id="16629-130">oppure, zero per nessuno di essi.</span><span class="sxs-lookup"><span data-stu-id="16629-130">or, zero for neither of them.</span></span>

<span data-ttu-id="16629-131">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-131">Example:</span></span>

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a><span data-ttu-id="16629-132">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="16629-132">GlobalRootSignature</span></span>
<span data-ttu-id="16629-133">Un GlobalRootSignature corrisponde a una struttura [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="16629-133">A GlobalRootSignature corresponds to a [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) structure.</span></span>

<span data-ttu-id="16629-134">I campi sono costituiti da un certo numero di stringhe che descrivono le parti della firma radice.</span><span class="sxs-lookup"><span data-stu-id="16629-134">The fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="16629-135">Per riferimento, vedere Specifica delle [firme radice in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="16629-135">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="16629-136">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-136">Example:</span></span>
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a><span data-ttu-id="16629-137">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="16629-137">LocalRootSignature</span></span>
<span data-ttu-id="16629-138">Un LocalRootSignature corrisponde a una struttura [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="16629-138">A LocalRootSignature corresponds to a [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) structure.</span></span>

<span data-ttu-id="16629-139">Analogamente al sottooggetto della firma radice globale, i campi sono costituiti da un certo numero di stringhe che descrivono le parti della firma radice.</span><span class="sxs-lookup"><span data-stu-id="16629-139">Just like the global root signature subobject, the fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="16629-140">Per riferimento, vedere Specifica delle [firme radice in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="16629-140">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="16629-141">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-141">Example:</span></span>
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a><span data-ttu-id="16629-142">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="16629-142">SubobjectToExportsAssocation</span></span>
<span data-ttu-id="16629-143">Per impostazione predefinita, un sottooggetto dichiarato semplicemente nella stessa libreria di un'esportazione è in grado di applicare a tale esportazione.</span><span class="sxs-lookup"><span data-stu-id="16629-143">By default, a subobject merely declared in the same library as an export is able to apply to that export.</span></span> <span data-ttu-id="16629-144">Tuttavia, le applicazioni hanno la possibilità di eseguire l'override di tale oggetto e di ottenere informazioni specifiche su quale elemento SubObject viene utilizzato per l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="16629-144">However, applications have the ability to override that and get specific about what subobject goes with which export.</span></span> <span data-ttu-id="16629-145">In HLSL questa "associazione esplicita" viene eseguita tramite SubobjectToExportsAssocation.</span><span class="sxs-lookup"><span data-stu-id="16629-145">In HLSL, this "explicit association" is done using SubobjectToExportsAssocation.</span></span>

<span data-ttu-id="16629-146">Un SubobjectToExportsAssocation corrisponde a una struttura [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .</span><span class="sxs-lookup"><span data-stu-id="16629-146">A SubobjectToExportsAssocation corresponds to a [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) structure.</span></span>

<span data-ttu-id="16629-147">Questo sottooggetto viene dichiarato con la sintassi</span><span class="sxs-lookup"><span data-stu-id="16629-147">This subobject is declared with the syntax</span></span>

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| <span data-ttu-id="16629-148">Elemento</span><span class="sxs-lookup"><span data-stu-id="16629-148">Item</span></span>                                                                                         | <span data-ttu-id="16629-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16629-149">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16629-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="16629-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="16629-151">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="16629-151">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="16629-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**Subobjectname**</span><span class="sxs-lookup"><span data-stu-id="16629-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span></span><br/>     | <span data-ttu-id="16629-153">Stringa che identifica un sottooggetto esportato.</span><span class="sxs-lookup"><span data-stu-id="16629-153">String which identifies an exported subobject.</span></span><br/> |
| <span data-ttu-id="16629-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Esporta**</span><span class="sxs-lookup"><span data-stu-id="16629-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exports**</span></span><br/> | <span data-ttu-id="16629-155">Stringa contenente un elenco delimitato da punti e virgola delle esportazioni.</span><span class="sxs-lookup"><span data-stu-id="16629-155">String containing a semicolon-delimited list of exports.</span></span><br/> |


<span data-ttu-id="16629-156">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-156">Example:</span></span>
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

<span data-ttu-id="16629-157">Si noti che entrambi i campi utilizzano nomi *esportati* .</span><span class="sxs-lookup"><span data-stu-id="16629-157">Note that both fields use *exported* names.</span></span> <span data-ttu-id="16629-158">Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione delle esportazioni.</span><span class="sxs-lookup"><span data-stu-id="16629-158">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="raytracingshaderconfig"></a><span data-ttu-id="16629-159">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="16629-159">RaytracingShaderConfig</span></span>

<span data-ttu-id="16629-160">Un RaytracingShaderConfig corrisponde a una struttura [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .</span><span class="sxs-lookup"><span data-stu-id="16629-160">A RaytracingShaderConfig corresponds to a [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) structure.</span></span>

<span data-ttu-id="16629-161">Questo sottooggetto viene dichiarato con la sintassi</span><span class="sxs-lookup"><span data-stu-id="16629-161">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| <span data-ttu-id="16629-162">Elemento</span><span class="sxs-lookup"><span data-stu-id="16629-162">Item</span></span>                                                                                         | <span data-ttu-id="16629-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16629-163">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16629-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="16629-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="16629-165">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="16629-165">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="16629-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span><span class="sxs-lookup"><span data-stu-id="16629-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span></span><br/>     | <span data-ttu-id="16629-167">Valore numerico per lo spazio di archiviazione massimo per i valori scalari (conteggiati come 4 byte ciascuno) nei payload del raggio per gli shader raytracing associati.</span><span class="sxs-lookup"><span data-stu-id="16629-167">Numerical value for the maximum storage for scalars (counted as 4 bytes each) in ray payloads for associated raytracing shaders.</span></span><br/> |
| <span data-ttu-id="16629-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="16629-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span></span><br/> | <span data-ttu-id="16629-169">Valore numerico per il numero massimo di scalari (conteggiato come 4 byte ciascuno) che può essere usato per gli attributi negli shader raytracing associati.</span><span class="sxs-lookup"><span data-stu-id="16629-169">Numerical value for the maximum number of scalars (counted as 4 bytes each) that can be used for attributes in associated raytracing shaders.</span></span> <span data-ttu-id="16629-170">Il valore non può superare [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span><span class="sxs-lookup"><span data-stu-id="16629-170">The value cannot exceed [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span></span><br/> |


<span data-ttu-id="16629-171">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-171">Example:</span></span>
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a><span data-ttu-id="16629-172">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="16629-172">RaytracingPipelineConfig</span></span>

<span data-ttu-id="16629-173">Un RaytracingPipelineConfig corrisponde a una struttura [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .</span><span class="sxs-lookup"><span data-stu-id="16629-173">A RaytracingPipelineConfig corresponds to a [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) structure.</span></span>

<span data-ttu-id="16629-174">Questo sottooggetto viene dichiarato con la sintassi</span><span class="sxs-lookup"><span data-stu-id="16629-174">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| <span data-ttu-id="16629-175">Elemento</span><span class="sxs-lookup"><span data-stu-id="16629-175">Item</span></span>                                                                                         | <span data-ttu-id="16629-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16629-176">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16629-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="16629-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="16629-178">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="16629-178">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="16629-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span><span class="sxs-lookup"><span data-stu-id="16629-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span></span><br/>     | <span data-ttu-id="16629-180">Limite numerico da usare per la ricorsione dei raggi nella pipeline raytracing.</span><span class="sxs-lookup"><span data-stu-id="16629-180">Numerical limit to use for ray recursion in the raytracing pipeline.</span></span> <span data-ttu-id="16629-181">Si tratta di un numero compreso tra 0 e 31, inclusi.</span><span class="sxs-lookup"><span data-stu-id="16629-181">It is a number between 0 and 31, inclusive.</span></span> <br/> |


<span data-ttu-id="16629-182">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-182">Example:</span></span>
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
<span data-ttu-id="16629-183">Poiché la ricorsione raytracing comporta un costo in termini di prestazioni, le applicazioni devono utilizzare la profondità di ricorsione più bassa necessaria per i risultati desiderati.</span><span class="sxs-lookup"><span data-stu-id="16629-183">Since there is a performance cost to raytracing recursion, applications should use the lowest recursion depth needed for the desired results.</span></span>

<span data-ttu-id="16629-184">Se le chiamate dello shader non hanno ancora raggiunto la profondità massima di ricorsione, possono chiamare [TraceRay](../direct3d12/traceray-function.md) per un numero qualsiasi di volte.</span><span class="sxs-lookup"><span data-stu-id="16629-184">If shader invocations haven't yet reached the maximum recursion depth, they can call [TraceRay](../direct3d12/traceray-function.md) any number of times.</span></span> <span data-ttu-id="16629-185">Tuttavia, se raggiungono o superano la profondità massima di ricorsione, la chiamata di TraceRay comporta lo stato rimosso del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16629-185">But if they reach or exceed the maximum recursion depth, calling TraceRay puts the device into removed state.</span></span> <span data-ttu-id="16629-186">Di conseguenza, gli shader raytracing devono interrompere la chiamata a TraceRay se hanno raggiunto o superato la profondità massima di ricorsione.</span><span class="sxs-lookup"><span data-stu-id="16629-186">Therefore, raytracing shaders should take care to stop calling TraceRay if they've met or exceeded the maximum recursion depth.</span></span>

## <a name="trianglehitgroup"></a><span data-ttu-id="16629-187">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="16629-187">TriangleHitGroup</span></span>

<span data-ttu-id="16629-188">Un TriangleHitGroup corrisponde a una struttura [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) il cui campo di tipo è impostato su [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="16629-188">A TriangleHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="16629-189">Questo sottooggetto viene dichiarato con la sintassi</span><span class="sxs-lookup"><span data-stu-id="16629-189">This subobject is declared with the syntax</span></span>

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| <span data-ttu-id="16629-190">Elemento</span><span class="sxs-lookup"><span data-stu-id="16629-190">Item</span></span>                                                                                         | <span data-ttu-id="16629-191">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16629-191">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16629-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="16629-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="16629-193">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="16629-193">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="16629-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="16629-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="16629-195">Nome di stringa dello shader anyhit per il gruppo di hit o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="16629-195">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="16629-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="16629-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="16629-197">Nome di stringa dell'hit shader più vicino per il gruppo di hit o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="16629-197">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="16629-198">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-198">Example:</span></span>
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

<span data-ttu-id="16629-199">Si noti che entrambi i campi utilizzano nomi *esportati* .</span><span class="sxs-lookup"><span data-stu-id="16629-199">Note that both fields use *exported* names.</span></span> <span data-ttu-id="16629-200">Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione delle esportazioni.</span><span class="sxs-lookup"><span data-stu-id="16629-200">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="proceduralprimitivehitgroup"></a><span data-ttu-id="16629-201">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="16629-201">ProceduralPrimitiveHitGroup</span></span>

<span data-ttu-id="16629-202">Un ProceduralPrimitiveHitGroup corrisponde a una struttura [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) il cui campo di tipo è impostato su [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="16629-202">A ProceduralPrimitiveHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="16629-203">Questo sottooggetto viene dichiarato con la sintassi</span><span class="sxs-lookup"><span data-stu-id="16629-203">This subobject is declared with the syntax</span></span>

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| <span data-ttu-id="16629-204">Elemento</span><span class="sxs-lookup"><span data-stu-id="16629-204">Item</span></span>                                                                                         | <span data-ttu-id="16629-205">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16629-205">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16629-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="16629-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="16629-207">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="16629-207">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="16629-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="16629-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="16629-209">Nome di stringa dello shader anyhit per il gruppo di hit o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="16629-209">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="16629-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="16629-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="16629-211">Nome di stringa dell'hit shader più vicino per il gruppo di hit o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="16629-211">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="16629-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span><span class="sxs-lookup"><span data-stu-id="16629-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span></span><br/> | <span data-ttu-id="16629-213">Nome di stringa dell'intersezione shader per il gruppo di hit o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="16629-213">String name of the intersection shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="16629-214">Esempio:</span><span class="sxs-lookup"><span data-stu-id="16629-214">Example:</span></span>
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

<span data-ttu-id="16629-215">Si noti che i tre campi utilizzano i nomi *esportati* .</span><span class="sxs-lookup"><span data-stu-id="16629-215">Note that the three fields use *exported* names.</span></span> <span data-ttu-id="16629-216">Un nome esportato può essere diverso dal nome originale in HLSL, se l'applicazione sceglie di eseguire la ridenominazione delle esportazioni.</span><span class="sxs-lookup"><span data-stu-id="16629-216">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="remarks"></a><span data-ttu-id="16629-217">Commenti</span><span class="sxs-lookup"><span data-stu-id="16629-217">Remarks</span></span>

<span data-ttu-id="16629-218">Gli oggetti subobjects hanno la nozione di "Association" o "quale SubObject passa con quale esportazione".</span><span class="sxs-lookup"><span data-stu-id="16629-218">Subobjects have the notion of "association", or "which subobject goes with which export".</span></span>

<span data-ttu-id="16629-219">Quando si specificano sottooggetti tramite il codice dello shader, la scelta di "quale oggetto SubObject passa con l'esportazione" segue le regole descritte nella [specifica DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span><span class="sxs-lookup"><span data-stu-id="16629-219">When specifying subobjects through shader code, the choice of "which subobject goes with which export" follows the rules as outlined in the [DXR specification](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span></span> <span data-ttu-id="16629-220">In particolare, si supponga che un'applicazione abbia alcune esportazioni.</span><span class="sxs-lookup"><span data-stu-id="16629-220">In particular, suppose an application has some export.</span></span> <span data-ttu-id="16629-221">Se un'applicazione associa l'esportazione con la firma radice A tramite shader-code e la firma radice B tramite il codice dell'applicazione, B è quello che viene usato.</span><span class="sxs-lookup"><span data-stu-id="16629-221">If an application associates that export with root signature A through shader-code and root signature B through application code, B is the one that gets used.</span></span> <span data-ttu-id="16629-222">La progettazione di "use B" invece di "generate an error" offre alle applicazioni la possibilità di eseguire facilmente l'override delle associazioni DXIL usando il codice dell'applicazione, anziché forzare la ricompilazione degli shader per risolvere gli elementi non corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="16629-222">The design of "use B" instead of "produce an error" gives applications the ability to conveniently override DXIL associations using application code, rather than be forced to recompile shaders to resolve mismatching things.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16629-223">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16629-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16629-224">Post di Blog per sviluppatori DirectX "Novità in D3D12-DirectX raytracing (DXR) supporta ora gli oggetti sottooggetti della libreria"</span><span class="sxs-lookup"><span data-stu-id="16629-224">DirectX Developer Blog post "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects"</span></span>](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[<span data-ttu-id="16629-225">Specifiche funzionali DirectX raytracing (DXR)</span><span class="sxs-lookup"><span data-stu-id="16629-225">DirectX Raytracing (DXR) Functional Spec</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[<span data-ttu-id="16629-226">Esempio: D3D12RaytracingLibrarySubobjects</span><span class="sxs-lookup"><span data-stu-id="16629-226">Sample: D3D12RaytracingLibrarySubobjects</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>