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
# <a name="creating-a-root-signature"></a><span data-ttu-id="f1be2-103">Creazione di una firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-103">Creating a Root Signature</span></span>

<span data-ttu-id="f1be2-104">Le firme radice sono una struttura di dati complessa contenente strutture annidate.</span><span class="sxs-lookup"><span data-stu-id="f1be2-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="f1be2-105">Questi possono essere definiti a livello di codice usando la definizione della struttura di dati riportata di seguito, che include i metodi per inizializzare i membri.</span><span class="sxs-lookup"><span data-stu-id="f1be2-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="f1be2-106">In alternativa, possono essere creati in HLSL (High Level Shading Language), offrendo il vantaggio che il compilatore convaliderà in anticipo che il layout è compatibile con lo shader.</span><span class="sxs-lookup"><span data-stu-id="f1be2-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="f1be2-107">L'API per la creazione di una firma radice accetta una versione serializzata (autonoma, senza puntatore) della descrizione del layout descritta di seguito.</span><span class="sxs-lookup"><span data-stu-id="f1be2-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="f1be2-108">Viene fornito un metodo per generare la versione serializzata dalla struttura dei dati C++, ma un altro modo per ottenere una definizione della firma radice serializzata consiste nel recuperarla da uno shader compilato con una firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="f1be2-109">Per sfruttare i vantaggi delle ottimizzazioni dei driver per i descrittori e i dati della firma radice, vedere la pagina relativa alla [firma radice versione 1,1](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="f1be2-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="f1be2-110">Tipi di binding tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="f1be2-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="f1be2-111">Intervallo descrittori</span><span class="sxs-lookup"><span data-stu-id="f1be2-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="f1be2-112">Layout tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="f1be2-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="f1be2-113">Costanti radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="f1be2-114">Descrittore radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="f1be2-115">Visibilità shader</span><span class="sxs-lookup"><span data-stu-id="f1be2-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="f1be2-116">Definizione della firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="f1be2-117">Serializzazione/deserializzazione della struttura dei dati della firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="f1be2-118">API di creazione della firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="f1be2-119">Firma radice negli oggetti stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="f1be2-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="f1be2-120">Codice per la definizione di una firma radice della versione 1,1</span><span class="sxs-lookup"><span data-stu-id="f1be2-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="f1be2-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1be2-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="f1be2-122">Tipi di binding tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="f1be2-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="f1be2-123">Il [**tipo di \_ \_ intervallo \_ descrittore D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) enum definisce i tipi di descrittori a cui è possibile fare riferimento come parte di una definizione del layout della tabella del descrittore.</span><span class="sxs-lookup"><span data-stu-id="f1be2-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="f1be2-124">Si tratta di un intervallo in modo che, ad esempio, se parte di una tabella descrittore presenta 100 SRVs, tale intervallo può essere dichiarato in una voce anziché 100.</span><span class="sxs-lookup"><span data-stu-id="f1be2-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="f1be2-125">Una definizione di tabella del descrittore è quindi una raccolta di intervalli.</span><span class="sxs-lookup"><span data-stu-id="f1be2-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="f1be2-126">Intervallo descrittori</span><span class="sxs-lookup"><span data-stu-id="f1be2-126">Descriptor Range</span></span>

<span data-ttu-id="f1be2-127">La struttura dell' [**\_ \_ intervallo di descrittori D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definisce un intervallo di descrittori di un determinato tipo (ad esempio SRVs) all'interno di una tabella del descrittore.</span><span class="sxs-lookup"><span data-stu-id="f1be2-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="f1be2-128">La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro può essere utilizzata in genere per il `OffsetInDescriptorsFromTableStart` parametro [**dell' \_ \_ intervallo di descrittori D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span><span class="sxs-lookup"><span data-stu-id="f1be2-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="f1be2-129">Questo significa accodare l'intervallo del descrittore che viene definito dopo quello precedente nella tabella del descrittore.</span><span class="sxs-lookup"><span data-stu-id="f1be2-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="f1be2-130">Se l'applicazione vuole descrittori di alias o per qualche motivo vuole ignorare gli slot, può impostare `OffsetInDescriptorsFromTableStart` su qualsiasi offset desiderato.</span><span class="sxs-lookup"><span data-stu-id="f1be2-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="f1be2-131">La definizione di intervalli sovrapposti di tipi diversi non è valida.</span><span class="sxs-lookup"><span data-stu-id="f1be2-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="f1be2-132">Il set di registri dello shader specificato dalla combinazione di `RangeType` , `NumDescriptors` , `BaseShaderRegister` e `RegisterSpace` non può essere in conflitto o sovrapposto a qualsiasi dichiarazione in una firma radice con [**\_ \_ visibilità D3D12 shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) comune. vedere la sezione relativa alla visibilità dello shader riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="f1be2-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="f1be2-133">Layout tabella descrittore</span><span class="sxs-lookup"><span data-stu-id="f1be2-133">Descriptor Table Layout</span></span>

<span data-ttu-id="f1be2-134">La struttura della [**\_ \_ \_ tabella descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) dichiara il layout di una tabella dei descrittori come una raccolta di intervalli di descrittori che vengono visualizzati uno dopo l'altro in un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="f1be2-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="f1be2-135">I sampler non sono consentiti nella stessa tabella dei descrittori di CBV/UAV/SRVs.</span><span class="sxs-lookup"><span data-stu-id="f1be2-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="f1be2-136">Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="f1be2-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="f1be2-137">Per impostare una tabella del descrittore Graphics (CBV, SRV, UAV, Sampler), usare [**ID3D12GraphicsCommandList:: SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="f1be2-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="f1be2-138">Per impostare una tabella del descrittore di calcolo, utilizzare [**ID3D12GraphicsCommandList:: SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="f1be2-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="f1be2-139">Costanti radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-139">Root Constants</span></span>

<span data-ttu-id="f1be2-140">La struttura delle [**\_ \_ costanti radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) dichiara le costanti inline nella firma radice che vengono visualizzate in shader come un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="f1be2-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="f1be2-141">Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="f1be2-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="f1be2-142">Descrittore radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-142">Root Descriptor</span></span>

<span data-ttu-id="f1be2-143">La struttura del [**\_ \_ descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) dichiara i descrittori (visualizzati in shader) inline nella firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="f1be2-144">Questo struct viene usato quando il tipo di slot della firma radice è impostato su `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` o `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="f1be2-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="f1be2-145">Visibilità shader</span><span class="sxs-lookup"><span data-stu-id="f1be2-145">Shader Visibility</span></span>

<span data-ttu-id="f1be2-146">Il membro dell'enumerazione di [**\_ \_ visibilità dello shader D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) impostato nel parametro di visibilità dello shader [**del \_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina gli shader che visualizzano il contenuto di uno slot di firma radice specificato.</span><span class="sxs-lookup"><span data-stu-id="f1be2-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="f1be2-147">Il calcolo usa sempre \_ tutti (poiché esiste una sola fase attiva).</span><span class="sxs-lookup"><span data-stu-id="f1be2-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="f1be2-148">La grafica può scegliere, ma se usa \_ tutto, tutte le fasi dello shader visualizzano qualsiasi elemento associato allo slot della firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="f1be2-149">Un uso della visibilità dello shader è aiutare gli shader creati in attesa di associazioni diverse per ogni fase dello shader usando uno spazio dei nomi sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="f1be2-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="f1be2-150">Un vertex shader, ad esempio, può dichiarare:</span><span class="sxs-lookup"><span data-stu-id="f1be2-150">For example, a vertex shader may declare:</span></span>

 

<span data-ttu-id="f1be2-151">Texture2D foo: Register (T0); "</span><span class="sxs-lookup"><span data-stu-id="f1be2-151">Texture2D foo : register(t0);"</span></span>

 

<span data-ttu-id="f1be2-152">il pixel shader Inoltre può dichiarare:</span><span class="sxs-lookup"><span data-stu-id="f1be2-152">and the pixel shader may also declare:</span></span>

 

<span data-ttu-id="f1be2-153">Barra Texture2D: Register (T0);</span><span class="sxs-lookup"><span data-stu-id="f1be2-153">Texture2D bar : register(t0);</span></span>

<span data-ttu-id="f1be2-154">Se l'applicazione crea un binding della firma radice a T0 VISIBILITY \_ All, entrambi gli shader visualizzano la stessa trama.</span><span class="sxs-lookup"><span data-stu-id="f1be2-154">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="f1be2-155">Se lo shader definisce in realtà che ogni shader può visualizzare trame diverse, può definire due slot di firma radice con il \_ vertice e il \_ pixel di visibilità.</span><span class="sxs-lookup"><span data-stu-id="f1be2-155">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="f1be2-156">Indipendentemente dalla visibilità in uno slot di firma radice, ha sempre lo stesso costo (costo solo a seconda del valore di SlotType) verso una dimensione massima della firma radice fissa.</span><span class="sxs-lookup"><span data-stu-id="f1be2-156">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="f1be2-157">Nell'hardware D3D11 di fascia bassa, \_ viene presa in considerazione anche la visibilità dello shader usato per la convalida delle dimensioni delle tabelle dei descrittori in un layout radice, poiché alcuni componenti hardware d3d11 possono supportare solo una quantità massima di binding per fase.</span><span class="sxs-lookup"><span data-stu-id="f1be2-157">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="f1be2-158">Queste restrizioni vengono imposte solo quando si esegue l'hardware a basso livello e non si limitano l'hardware più moderno.</span><span class="sxs-lookup"><span data-stu-id="f1be2-158">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="f1be2-159">Se per una firma radice sono state definite più tabelle dei descrittori che si sovrappongono tra loro nello spazio dei nomi (i binding Register allo shader) e in uno di essi \_ viene specificato all per Visibility, il layout non è valido (la creazione avrà esito negativo).</span><span class="sxs-lookup"><span data-stu-id="f1be2-159">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="f1be2-160">Definizione della firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-160">Root Signature Definition</span></span>

<span data-ttu-id="f1be2-161">La [**struttura \_ \_ \_ desc della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) può contenere tabelle descrittore e costanti inline, ogni tipo di slot definito dalla struttura del [**\_ \_ parametro radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) e dal [**\_ \_ \_ tipo di parametro radice enum D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span><span class="sxs-lookup"><span data-stu-id="f1be2-161">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="f1be2-162">Per avviare uno slot di firma radice, fare riferimento ai **metodi \* \* \* SetComputeRoot** e **SetGraphicsRoot \* \* \*** di [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="f1be2-162">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="f1be2-163">I sampler statici sono descritti nella firma radice usando la struttura del [**\_ \_ campionatore statico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="f1be2-163">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="f1be2-164">Un numero di flag che limitano l'accesso di determinati shader alla firma radice, fanno riferimento [**ai \_ \_ \_ flag della firma radice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="f1be2-164">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="f1be2-165">Serializzazione/deserializzazione della struttura dei dati della firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-165">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="f1be2-166">I metodi descritti in questa sezione sono esportati da D3D12Core.dll e forniscono metodi per la serializzazione e la deserializzazione di una struttura di dati della firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-166">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="f1be2-167">Il modulo serializzato è quello che viene passato all'API quando si crea una firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-167">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="f1be2-168">Se uno shader è stato creato con una firma radice (quando tale funzionalità viene aggiunta), lo shader compilato conterrà già una firma radice serializzata.</span><span class="sxs-lookup"><span data-stu-id="f1be2-168">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="f1be2-169">Se un'applicazione genera in modo procedurale una struttura dei dati [**\_ \_ \_ desc della firma radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , deve creare il modulo serializzato usando [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span><span class="sxs-lookup"><span data-stu-id="f1be2-169">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="f1be2-170">L'output di che può essere passato in [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="f1be2-170">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="f1be2-171">Se un'applicazione ha già una firma radice serializzata o ha uno shader compilato che contiene una firma radice e desidera individuare a livello di codice la definizione del layout (nota come "Reflection"), è possibile chiamare [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) .</span><span class="sxs-lookup"><span data-stu-id="f1be2-171">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="f1be2-172">Viene generata un'interfaccia [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , che contiene un metodo per restituire la struttura dei dati [**della \_ \_ firma radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserializzata.</span><span class="sxs-lookup"><span data-stu-id="f1be2-172">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="f1be2-173">L'interfaccia possiede la durata della struttura dei dati deserializzati.</span><span class="sxs-lookup"><span data-stu-id="f1be2-173">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="f1be2-174">API di creazione della firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-174">Root Signature Creation API</span></span>

<span data-ttu-id="f1be2-175">L'API [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) accetta una versione serializzata di una firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-175">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="f1be2-176">Firma radice negli oggetti stato della pipeline</span><span class="sxs-lookup"><span data-stu-id="f1be2-176">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="f1be2-177">I metodi per creare lo stato della pipeline ([**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) accettano un'interfaccia [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) facoltativa come parametro di input (archiviato in una struttura di [**\_ \_ \_ \_ Descrizione dello stato della pipeline grafica D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ).</span><span class="sxs-lookup"><span data-stu-id="f1be2-177">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="f1be2-178">Verrà eseguito l'override di qualsiasi firma radice già presente negli shader.</span><span class="sxs-lookup"><span data-stu-id="f1be2-178">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="f1be2-179">Se una firma radice viene passata in uno dei metodi di stato di creazione della pipeline, la firma radice viene convalidata rispetto a tutti gli shader nell'oggetto PSO per la compatibilità e viene fornita al driver da usare con tutti gli shader.</span><span class="sxs-lookup"><span data-stu-id="f1be2-179">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="f1be2-180">Se uno qualsiasi degli shader presenta una firma radice diversa, viene sostituito dalla firma radice passata all'API.</span><span class="sxs-lookup"><span data-stu-id="f1be2-180">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="f1be2-181">Se non viene passata una firma radice, tutti gli shader passati devono avere una firma radice e devono corrispondere, che verrà assegnato al driver.</span><span class="sxs-lookup"><span data-stu-id="f1be2-181">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="f1be2-182">L'impostazione di un oggetto PSO in un elenco di comandi o in un bundle non comporta la modifica della firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-182">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="f1be2-183">Questa operazione viene eseguita dai metodi [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) e [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span><span class="sxs-lookup"><span data-stu-id="f1be2-183">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="f1be2-184">Quando viene richiamato/dispatch (Compute), l'applicazione deve verificare che il PSO corrente corrisponda alla firma radice corrente. in caso contrario, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="f1be2-184">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="f1be2-185">Codice per la definizione di una firma radice della versione 1,1</span><span class="sxs-lookup"><span data-stu-id="f1be2-185">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="f1be2-186">Nell'esempio seguente viene illustrato come creare una firma radice con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="f1be2-186">The example below shows how to create a root signature with the following format:</span></span>



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="f1be2-187">**RootParameterIndex**</span><span class="sxs-lookup"><span data-stu-id="f1be2-187">**RootParameterIndex**</span></span> | <span data-ttu-id="f1be2-188">**Contents**</span><span class="sxs-lookup"><span data-stu-id="f1be2-188">**Contents**</span></span>                                   |                                              |
| <span data-ttu-id="f1be2-189">\[0\]</span><span class="sxs-lookup"><span data-stu-id="f1be2-189">\[0\]</span></span>                  | <span data-ttu-id="f1be2-190">Costanti radice: {B2}</span><span class="sxs-lookup"><span data-stu-id="f1be2-190">Root constants: { b2 }</span></span>                         | <span data-ttu-id="f1be2-191">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="f1be2-191">(1 CBV)</span></span>                                      |
| <span data-ttu-id="f1be2-192">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f1be2-192">\[1\]</span></span>                  | <span data-ttu-id="f1be2-193">Tabella descrittore: {T2-T7, U0-U3}</span><span class="sxs-lookup"><span data-stu-id="f1be2-193">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="f1be2-194">(6 SRVs + 4 UAV)</span><span class="sxs-lookup"><span data-stu-id="f1be2-194">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="f1be2-195">\[2\]</span><span class="sxs-lookup"><span data-stu-id="f1be2-195">\[2\]</span></span>                  | <span data-ttu-id="f1be2-196">CBV radice: {B0}</span><span class="sxs-lookup"><span data-stu-id="f1be2-196">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="f1be2-197">(1 CBV, dati statici)</span><span class="sxs-lookup"><span data-stu-id="f1be2-197">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="f1be2-198">\[3\]</span><span class="sxs-lookup"><span data-stu-id="f1be2-198">\[3\]</span></span>                  | <span data-ttu-id="f1be2-199">Tabella descrittore: {S0-S1}</span><span class="sxs-lookup"><span data-stu-id="f1be2-199">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="f1be2-200">(2 Samplers)</span><span class="sxs-lookup"><span data-stu-id="f1be2-200">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="f1be2-201">\[4\]</span><span class="sxs-lookup"><span data-stu-id="f1be2-201">\[4\]</span></span>                  | <span data-ttu-id="f1be2-202">Tabella descrittore: {T8-unbounded}</span><span class="sxs-lookup"><span data-stu-id="f1be2-202">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="f1be2-203">(non associato \# a SRVs, descrittori volatili)</span><span class="sxs-lookup"><span data-stu-id="f1be2-203">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="f1be2-204">\[5\]</span><span class="sxs-lookup"><span data-stu-id="f1be2-204">\[5\]</span></span>                  | <span data-ttu-id="f1be2-205">Tabella descrittore: {(T0, space1)-unbounded}</span><span class="sxs-lookup"><span data-stu-id="f1be2-205">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="f1be2-206">(non associato \# a SRVs, descrittori volatili)</span><span class="sxs-lookup"><span data-stu-id="f1be2-206">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="f1be2-207">\[6\]</span><span class="sxs-lookup"><span data-stu-id="f1be2-207">\[6\]</span></span>                  | <span data-ttu-id="f1be2-208">Tabella descrittore: {B1}</span><span class="sxs-lookup"><span data-stu-id="f1be2-208">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="f1be2-209">(1 CBV, dati statici)</span><span class="sxs-lookup"><span data-stu-id="f1be2-209">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="f1be2-210">Se la maggior parte delle parti della firma radice viene utilizzata la maggior parte del tempo, può essere preferibile rispetto alla necessità di cambiare troppo spesso la firma radice.</span><span class="sxs-lookup"><span data-stu-id="f1be2-210">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="f1be2-211">Le applicazioni devono ordinare le voci della firma radice dal passaggio più frequente al minore.</span><span class="sxs-lookup"><span data-stu-id="f1be2-211">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="f1be2-212">Quando un'applicazione modifica i binding in qualsiasi parte della firma radice, il driver potrebbe dover creare una copia di alcuni o tutti gli Stati della firma radice, il che può diventare un costo non semplice quando viene moltiplicato per molte modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="f1be2-212">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="f1be2-213">Inoltre, la firma radice definirà un campionatore statico che esegue il filtro di trama anisotropico al registro shader S3.</span><span class="sxs-lookup"><span data-stu-id="f1be2-213">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="f1be2-214">Una volta associata la firma radice, le tabelle di descrittore, CBV radice e costanti possono essere assegnate allo \[ spazio dei parametri 0.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="f1be2-214">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="f1be2-215">ad esempio, le tabelle dei descrittori (intervalli in un heap del descrittore) possono essere associati a ogni parametro radice \[ 1 \] e \[ 3.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="f1be2-215">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

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

<span data-ttu-id="f1be2-216">Il codice seguente illustra come può essere usata la firma radice precedente in un elenco di comandi di grafica.</span><span class="sxs-lookup"><span data-stu-id="f1be2-216">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f1be2-217">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1be2-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1be2-218">Firme radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-218">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="f1be2-219">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="f1be2-219">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="f1be2-220">Uso di una firma radice</span><span class="sxs-lookup"><span data-stu-id="f1be2-220">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
