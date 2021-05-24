---
title: Creazione di una firma radice
description: Le firme radice sono una struttura di dati complessa contenente strutture annidate.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed993618e021656dbc9377882e2961f7f0d62263
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335645"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="ba64b-103">Creazione di una firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-103">Creating a Root Signature</span></span>

<span data-ttu-id="ba64b-104">Le firme radice sono una struttura di dati complessa contenente strutture annidate.</span><span class="sxs-lookup"><span data-stu-id="ba64b-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="ba64b-105">Questi elementi possono essere definiti a livello di codice usando la definizione della struttura dei dati riportata di seguito , che include metodi che consentono di inizializzare i membri.</span><span class="sxs-lookup"><span data-stu-id="ba64b-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="ba64b-106">In alternativa, possono essere creati in HLSL (High Level Shading Language), offrendo il vantaggio che il compilatore convaliderà in anticipo che il layout è compatibile con lo shader.</span><span class="sxs-lookup"><span data-stu-id="ba64b-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="ba64b-107">L'API per la creazione di una firma radice accetta una versione serializzata (indipendente, senza puntatore) della descrizione del layout descritta di seguito.</span><span class="sxs-lookup"><span data-stu-id="ba64b-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="ba64b-108">Viene fornito un metodo per generare questa versione serializzata dalla struttura di dati C++, ma un altro modo per ottenere una definizione di firma radice serializzata è recuperarla da uno shader compilato con una firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="ba64b-109">Se si vogliono sfruttare le ottimizzazioni dei driver per i descrittori di firma radice e i dati, vedere Root Signature Version 1.1 (Firma radice [versione 1.1)](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="ba64b-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="ba64b-110">Tipi di associazione tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="ba64b-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="ba64b-111">Intervallo descrittore</span><span class="sxs-lookup"><span data-stu-id="ba64b-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="ba64b-112">Layout tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="ba64b-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="ba64b-113">Costanti radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="ba64b-114">Descrittore radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="ba64b-115">Visibilità dello shader</span><span class="sxs-lookup"><span data-stu-id="ba64b-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="ba64b-116">Definizione della firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="ba64b-117">Serializzazione/deserializzazione della struttura dei dati della firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="ba64b-118">API di creazione della firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="ba64b-119">Firma radice negli oggetti di stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="ba64b-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="ba64b-120">Codice per la definizione di una firma radice della versione 1.1</span><span class="sxs-lookup"><span data-stu-id="ba64b-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="ba64b-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba64b-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="ba64b-122">Tipi di associazione tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="ba64b-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="ba64b-123">L'enumerazione [**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) definisce i tipi di descrittori a cui è possibile fare riferimento come parte di una definizione di layout della tabella descrittore.</span><span class="sxs-lookup"><span data-stu-id="ba64b-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="ba64b-124">Si tratta di un intervallo in modo che, ad esempio, se una parte di una tabella di descrittori ha 100 SRV, tale intervallo può essere dichiarato in una voce anziché in 100.</span><span class="sxs-lookup"><span data-stu-id="ba64b-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="ba64b-125">Una definizione di tabella descrittore è quindi una raccolta di intervalli.</span><span class="sxs-lookup"><span data-stu-id="ba64b-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="ba64b-126">Intervallo descrittore</span><span class="sxs-lookup"><span data-stu-id="ba64b-126">Descriptor Range</span></span>

<span data-ttu-id="ba64b-127">La [**struttura D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definisce un intervallo di descrittori di un determinato tipo (ad esempio SRV) all'interno di una tabella di descrittori.</span><span class="sxs-lookup"><span data-stu-id="ba64b-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="ba64b-128">La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro può in genere essere usata per il parametro di `OffsetInDescriptorsFromTableStart` [**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span><span class="sxs-lookup"><span data-stu-id="ba64b-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="ba64b-129">Ciò significa aggiungere l'intervallo di descrittori definito dopo quello precedente nella tabella del descrittore.</span><span class="sxs-lookup"><span data-stu-id="ba64b-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="ba64b-130">Se l'applicazione vuole creare l'alias dei descrittori o per qualche motivo vuole ignorare gli slot, può impostare `OffsetInDescriptorsFromTableStart` l'offset desiderato.</span><span class="sxs-lookup"><span data-stu-id="ba64b-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="ba64b-131">La definizione di intervalli sovrapposti di tipi diversi non è valida.</span><span class="sxs-lookup"><span data-stu-id="ba64b-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="ba64b-132">Il set di registri shader specificato dalla combinazione di , , e non può essere in conflitto o sovrapporsi tra le dichiarazioni in una firma radice con visibilità `RangeType` `NumDescriptors` `BaseShaderRegister` `RegisterSpace` [**D3D12 \_ SHADER \_ comune**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (vedere la sezione relativa alla visibilità dello shader riportata di seguito).</span><span class="sxs-lookup"><span data-stu-id="ba64b-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="ba64b-133">Layout tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="ba64b-133">Descriptor Table Layout</span></span>

<span data-ttu-id="ba64b-134">La [**struttura D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) dichiara il layout di una tabella descrittore come raccolta di intervalli di descrittori che vengono visualizzati uno dopo l'altro in un heap dei descrittori.</span><span class="sxs-lookup"><span data-stu-id="ba64b-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="ba64b-135">I campionatori non sono consentiti nella stessa tabella descrittore di CBV/UAV/SRV.</span><span class="sxs-lookup"><span data-stu-id="ba64b-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="ba64b-136">Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="ba64b-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="ba64b-137">Per impostare una tabella descrittore grafica (CBV, SRV, UAV, Sampler), usare [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="ba64b-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="ba64b-138">Per impostare una tabella del descrittore di calcolo, usare [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="ba64b-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="ba64b-139">Costanti radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-139">Root Constants</span></span>

<span data-ttu-id="ba64b-140">La [**struttura D3D12 \_ ROOT \_ CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) dichiara le costanti inline nella firma radice visualizzate negli shader come un unico buffer costante.</span><span class="sxs-lookup"><span data-stu-id="ba64b-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="ba64b-141">Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="ba64b-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="ba64b-142">Descrittore radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-142">Root Descriptor</span></span>

<span data-ttu-id="ba64b-143">La [**struttura D3D12 \_ ROOT \_ DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) dichiara i descrittori (visualizzati negli shader) inline nella firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="ba64b-144">Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_CBV` o `D3D12_ROOT_PARAMETER_TYPE_SRV` `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="ba64b-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="ba64b-145">Visibilità shader</span><span class="sxs-lookup"><span data-stu-id="ba64b-145">Shader Visibility</span></span>

<span data-ttu-id="ba64b-146">Il membro dell'enumerazione [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) impostato nel parametro di visibilità dello shader [**di D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina quali shader visualizzano il contenuto di uno slot di firma radice specificato.</span><span class="sxs-lookup"><span data-stu-id="ba64b-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="ba64b-147">Il calcolo usa \_ sempre ALL (poiché è presente una sola fase attiva).</span><span class="sxs-lookup"><span data-stu-id="ba64b-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="ba64b-148">La grafica può scegliere, ma se usa ALL, tutte le fasi dello shader vedono tutto ciò \_ che è associato allo slot di firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="ba64b-149">Uno degli usi della visibilità dello shader è aiutare gli shader creati a aspettarsi associazioni diverse per ogni fase dello shader usando uno spazio dei nomi sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="ba64b-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="ba64b-150">Ad esempio, un vertex shader può dichiarare:</span><span class="sxs-lookup"><span data-stu-id="ba64b-150">For example, a vertex shader may declare:</span></span>

```hlsl
Texture2D foo : register(t0);
```

<span data-ttu-id="ba64b-151">e il pixel shader possono anche dichiarare:</span><span class="sxs-lookup"><span data-stu-id="ba64b-151">and the pixel shader may also declare:</span></span>

```hlsl
Texture2D bar : register(t0);
```

<span data-ttu-id="ba64b-152">Se l'applicazione esegue un binding della firma radice a t0 VISIBILITY \_ ALL, entrambi gli shader vedono la stessa trama.</span><span class="sxs-lookup"><span data-stu-id="ba64b-152">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="ba64b-153">Se lo shader definisce in realtà vuole che ogni shader veda trame diverse, può definire 2 slot di firma radice con VISIBILITY \_ VERTEX e \_ PIXEL.</span><span class="sxs-lookup"><span data-stu-id="ba64b-153">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="ba64b-154">Indipendentemente dalla visibilità in uno slot di firma radice, ha sempre lo stesso costo (solo a seconda di SlotType) verso una dimensione massima fissa della firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-154">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="ba64b-155">Nell'hardware D3D11 di fascia bassa, shader VISIBILITY viene anche preso in considerazione durante la convalida delle dimensioni delle tabelle dei descrittori in un layout radice, poiché alcuni componenti hardware D3D11 possono supportare solo una quantità massima di \_ associazioni per fase.</span><span class="sxs-lookup"><span data-stu-id="ba64b-155">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="ba64b-156">Queste restrizioni vengono imposte solo quando vengono eseguite su hardware di basso livello e non limitano affatto l'hardware più moderno.</span><span class="sxs-lookup"><span data-stu-id="ba64b-156">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="ba64b-157">Se per una firma radice sono definite più tabelle di descrittori che si sovrappongono tra loro nello spazio dei nomi (le associazioni del registro allo shader) e una di esse specifica ALL per la visibilità, il layout non è valido (la creazione avrà esito \_ negativo).</span><span class="sxs-lookup"><span data-stu-id="ba64b-157">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="ba64b-158">Definizione della firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-158">Root Signature Definition</span></span>

<span data-ttu-id="ba64b-159">La [**struttura D3D12 \_ ROOT SIGNATURE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) può contenere tabelle di descrittori e costanti inline, ogni tipo di slot definito dalla struttura [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) e dall'enumerazione [**D3D12 \_ ROOT PARAMETER \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span><span class="sxs-lookup"><span data-stu-id="ba64b-159">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="ba64b-160">Per avviare uno slot di firma radice, fare riferimento ai **metodi \* \* \* SetComputeRoot** e **\* \* \* SetGraphicsRoot** di [**ID3D12GraphicsCommandList.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)</span><span class="sxs-lookup"><span data-stu-id="ba64b-160">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="ba64b-161">I campionatori statici sono descritti nella firma radice usando la [**struttura D3D12 \_ STATIC \_ SAMPLER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="ba64b-161">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="ba64b-162">Alcuni flag limitano l'accesso di determinati shader alla firma radice. Vedere [**D3D12 ROOT SIGNATURE FLAGS ( FLAG \_ DI \_ FIRMA \_ RADICE D3D12).**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)</span><span class="sxs-lookup"><span data-stu-id="ba64b-162">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="ba64b-163">Serializzazione/deserializzazione della struttura dei dati della firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-163">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="ba64b-164">I metodi descritti in questa sezione vengono esportati da D3D12Core.dll e forniscono metodi per la serializzazione e la deserializzazione di una struttura di dati della firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-164">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="ba64b-165">Il formato serializzato è ciò che viene passato all'API quando si crea una firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-165">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="ba64b-166">Se uno shader è stato creato con una firma radice (quando viene aggiunta tale funzionalità), lo shader compilato conterrà già una firma radice serializzata.</span><span class="sxs-lookup"><span data-stu-id="ba64b-166">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="ba64b-167">Se un'applicazione genera una struttura di dati [**\_ \_ \_ DESC D3D12 ROOT SIGNATURE,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deve creare il form serializzato [**usando D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span><span class="sxs-lookup"><span data-stu-id="ba64b-167">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="ba64b-168">Output di che può essere passato in [**ID3D12Device::CreateRootSignature.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)</span><span class="sxs-lookup"><span data-stu-id="ba64b-168">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="ba64b-169">Se un'applicazione ha già una firma radice serializzata o ha uno shader compilato che contiene una firma radice e vuole individuare a livello di codice la definizione del layout (nota come "reflection"), è possibile chiamare [**D3D12CreateRootSignatureDeserializer.**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer)</span><span class="sxs-lookup"><span data-stu-id="ba64b-169">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="ba64b-170">Viene generata [**un'interfaccia ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) che contiene un metodo per restituire la struttura dei dati [**DESC D3D12 \_ ROOT SIGNATURE \_ deserializzata. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)</span><span class="sxs-lookup"><span data-stu-id="ba64b-170">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="ba64b-171">L'interfaccia è proprietaria della durata della struttura dei dati deserializzati.</span><span class="sxs-lookup"><span data-stu-id="ba64b-171">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="ba64b-172">API di creazione della firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-172">Root Signature Creation API</span></span>

<span data-ttu-id="ba64b-173">[**L'API ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) accetta una versione serializzata di una firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-173">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="ba64b-174">Firma radice negli oggetti di stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="ba64b-174">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="ba64b-175">I metodi per creare lo stato della pipeline ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) accettano un'interfaccia [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) facoltativa come parametro di input (archiviato in una struttura [**DESC D3D12 \_ GRAPHICS PIPELINE \_ \_ STATE). \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)</span><span class="sxs-lookup"><span data-stu-id="ba64b-175">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="ba64b-176">Verrà eseguito l'override di qualsiasi firma radice già presente negli shader.</span><span class="sxs-lookup"><span data-stu-id="ba64b-176">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="ba64b-177">Se una firma radice viene passata in uno dei metodi di creazione dello stato della pipeline, questa firma radice viene convalidata rispetto a tutti gli shader nel pso per la compatibilità e viene data al driver per l'uso con tutti gli shader.</span><span class="sxs-lookup"><span data-stu-id="ba64b-177">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="ba64b-178">Se uno degli shader contiene una firma radice diversa, viene sostituito dalla firma radice passata all'API.</span><span class="sxs-lookup"><span data-stu-id="ba64b-178">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="ba64b-179">Se non viene passata una firma radice, tutti gli shader passati devono avere una firma radice e devono corrispondere. Questa firma verrà data al driver.</span><span class="sxs-lookup"><span data-stu-id="ba64b-179">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="ba64b-180">L'impostazione di un pso in un elenco di comandi o in un bundle non modifica la firma radice.</span><span class="sxs-lookup"><span data-stu-id="ba64b-180">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="ba64b-181">Questa operazione viene eseguita dai metodi [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) [**e SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span><span class="sxs-lookup"><span data-stu-id="ba64b-181">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="ba64b-182">Quando viene richiamata la funzione time draw(graphics)/dispatch(compute), l'applicazione deve assicurarsi che l'oggetto PsO corrente corrisponda alla firma radice corrente. In caso contrario, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="ba64b-182">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="ba64b-183">Codice per la definizione di una firma radice della versione 1.1</span><span class="sxs-lookup"><span data-stu-id="ba64b-183">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="ba64b-184">L'esempio seguente illustra come creare una firma radice con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="ba64b-184">The example below shows how to create a root signature with the following format:</span></span>



| <span data-ttu-id="ba64b-185">RootParameterIndex</span><span class="sxs-lookup"><span data-stu-id="ba64b-185">RootParameterIndex</span></span>                       | <span data-ttu-id="ba64b-186">Contenuto</span><span class="sxs-lookup"><span data-stu-id="ba64b-186">Contents</span></span>                                               | <span data-ttu-id="ba64b-187">Valori</span><span class="sxs-lookup"><span data-stu-id="ba64b-187">Values</span></span>                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| <span data-ttu-id="ba64b-188">\[0\]</span><span class="sxs-lookup"><span data-stu-id="ba64b-188">\[0\]</span></span>                  | <span data-ttu-id="ba64b-189">Costanti radice: { b2 }</span><span class="sxs-lookup"><span data-stu-id="ba64b-189">Root constants: { b2 }</span></span>                         | <span data-ttu-id="ba64b-190">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="ba64b-190">(1 CBV)</span></span>                                      |
| <span data-ttu-id="ba64b-191">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ba64b-191">\[1\]</span></span>                  | <span data-ttu-id="ba64b-192">Tabella dei descrittori: { t2-t7, u0-u3 }</span><span class="sxs-lookup"><span data-stu-id="ba64b-192">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="ba64b-193">(6 SRV + 4 UAV)</span><span class="sxs-lookup"><span data-stu-id="ba64b-193">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="ba64b-194">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ba64b-194">\[2\]</span></span>                  | <span data-ttu-id="ba64b-195">Root CBV: { b0 }</span><span class="sxs-lookup"><span data-stu-id="ba64b-195">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="ba64b-196">(1 CBV, dati statici)</span><span class="sxs-lookup"><span data-stu-id="ba64b-196">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="ba64b-197">\[3\]</span><span class="sxs-lookup"><span data-stu-id="ba64b-197">\[3\]</span></span>                  | <span data-ttu-id="ba64b-198">Tabella dei descrittori: { s0-s1 }</span><span class="sxs-lookup"><span data-stu-id="ba64b-198">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="ba64b-199">(2 campionatori)</span><span class="sxs-lookup"><span data-stu-id="ba64b-199">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="ba64b-200">\[4\]</span><span class="sxs-lookup"><span data-stu-id="ba64b-200">\[4\]</span></span>                  | <span data-ttu-id="ba64b-201">Tabella dei descrittori: { t8 - unbounded }</span><span class="sxs-lookup"><span data-stu-id="ba64b-201">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="ba64b-202">(senza associazione \# di SRV, descrittori volatili)</span><span class="sxs-lookup"><span data-stu-id="ba64b-202">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="ba64b-203">\[5\]</span><span class="sxs-lookup"><span data-stu-id="ba64b-203">\[5\]</span></span>                  | <span data-ttu-id="ba64b-204">Tabella dei descrittori: { (t0, space1) - unbounded }</span><span class="sxs-lookup"><span data-stu-id="ba64b-204">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="ba64b-205">(senza associazione \# di SRV, descrittori volatili)</span><span class="sxs-lookup"><span data-stu-id="ba64b-205">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="ba64b-206">\[6\]</span><span class="sxs-lookup"><span data-stu-id="ba64b-206">\[6\]</span></span>                  | <span data-ttu-id="ba64b-207">Tabella dei descrittori: { b1 }</span><span class="sxs-lookup"><span data-stu-id="ba64b-207">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="ba64b-208">(1 CBV, dati statici)</span><span class="sxs-lookup"><span data-stu-id="ba64b-208">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="ba64b-209">Se la maggior parte delle parti della firma radice viene usata nella maggior parte dei casi, può essere meglio che cambiare la firma radice troppo frequentemente.</span><span class="sxs-lookup"><span data-stu-id="ba64b-209">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="ba64b-210">Le applicazioni devono ordinare le voci nella firma radice dalla più frequente alla meno frequente.</span><span class="sxs-lookup"><span data-stu-id="ba64b-210">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="ba64b-211">Quando un'app modifica le associazioni in qualsiasi parte della firma radice, il driver potrebbe essere necessario creare una copia di uno o tutti gli stati della firma radice, che possono diventare un costo non aggiuntivo se moltiplicato tra molte modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="ba64b-211">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="ba64b-212">Inoltre, la firma radice definirà un campionatore statico che esegue il filtro delle trame anisotropo nel registro shader s3.</span><span class="sxs-lookup"><span data-stu-id="ba64b-212">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="ba64b-213">Dopo l'associazione di questa firma radice, allo spazio dei parametri \[ 0..6 è possibile assegnare tabelle di descrittori, CBV radice e \] costanti.</span><span class="sxs-lookup"><span data-stu-id="ba64b-213">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="ba64b-214">Ad esempio, le tabelle dei descrittori (intervalli in un heap descrittore) possono essere associate a ognuno dei parametri radice 1 e \[ \] \[ 3..6. \]</span><span class="sxs-lookup"><span data-stu-id="ba64b-214">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

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

<span data-ttu-id="ba64b-215">Il codice seguente illustra come usare la firma radice precedente in un elenco di comandi grafici.</span><span class="sxs-lookup"><span data-stu-id="ba64b-215">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ba64b-216">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba64b-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba64b-217">Firme radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-217">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="ba64b-218">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="ba64b-218">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="ba64b-219">Uso di una firma radice</span><span class="sxs-lookup"><span data-stu-id="ba64b-219">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
