---
title: Nuovi tipi di risorse
description: In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Buffer degli indirizzi byte (panoramica)
- Buffer di lettura/scrittura (panoramica)
- Buffer strutturato (panoramica)
- Buffer di accesso non ordinato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399360"
---
# <a name="new-resource-types"></a><span data-ttu-id="824d9-107">Nuovi tipi di risorse</span><span class="sxs-lookup"><span data-stu-id="824d9-107">New Resource Types</span></span>

<span data-ttu-id="824d9-108">In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.</span><span class="sxs-lookup"><span data-stu-id="824d9-108">Several new resource types have been added in Direct3D 11.</span></span>

-   [<span data-ttu-id="824d9-109">Buffer e trame di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="824d9-109">Read/Write Buffers and Textures</span></span>](#readwrite-buffers-and-textures)
-   [<span data-ttu-id="824d9-110">Buffer strutturato</span><span class="sxs-lookup"><span data-stu-id="824d9-110">Structured Buffer</span></span>](#structured-buffer)
-   [<span data-ttu-id="824d9-111">Buffer degli indirizzi byte</span><span class="sxs-lookup"><span data-stu-id="824d9-111">Byte Address Buffer</span></span>](#byte-address-buffer)
-   [<span data-ttu-id="824d9-112">Buffer o trama di accesso non ordinato</span><span class="sxs-lookup"><span data-stu-id="824d9-112">Unordered Access Buffer or Texture</span></span>](#unordered-access-buffer-or-texture)
    -   [<span data-ttu-id="824d9-113">Accoda e utilizza buffer</span><span class="sxs-lookup"><span data-stu-id="824d9-113">Append and Consume Buffer</span></span>](#append-and-consume-buffer)
-   [<span data-ttu-id="824d9-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="824d9-114">Related topics</span></span>](#related-topics)

## <a name="readwrite-buffers-and-textures"></a><span data-ttu-id="824d9-115">Buffer e trame di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="824d9-115">Read/Write Buffers and Textures</span></span>

<span data-ttu-id="824d9-116">Le risorse del modello Shader 4 sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="824d9-116">Shader model 4 resources are read only.</span></span> <span data-ttu-id="824d9-117">Shader Model 5 implementa un nuovo set corrispondente di risorse di lettura/scrittura:</span><span class="sxs-lookup"><span data-stu-id="824d9-117">Shader model 5 implements a new corresponding set of read/write resources:</span></span>

-   [<span data-ttu-id="824d9-118">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="824d9-118">RWBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   <span data-ttu-id="824d9-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span><span class="sxs-lookup"><span data-stu-id="824d9-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span></span>
-   <span data-ttu-id="824d9-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span><span class="sxs-lookup"><span data-stu-id="824d9-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span></span>
-   [<span data-ttu-id="824d9-121">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="824d9-121">RWTexture3D</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

<span data-ttu-id="824d9-122">Queste risorse richiedono una variabile di risorsa per accedere alla memoria (tramite l'indicizzazione) perché non sono disponibili metodi per accedere direttamente alla memoria.</span><span class="sxs-lookup"><span data-stu-id="824d9-122">These resources require a resource variable to access memory (through indexing) as there are no methods for accessing memory directly.</span></span> <span data-ttu-id="824d9-123">Una variabile di risorsa può essere usata a destra e a sinistra di un'equazione. Se usato sul lato destro, il tipo di modello deve essere un singolo componente (float, int o uint).</span><span class="sxs-lookup"><span data-stu-id="824d9-123">A resource variable can be used on the left and right sides of an equation; if used on the right side, the template type must be single component (float, int, or uint).</span></span>

## <a name="structured-buffer"></a><span data-ttu-id="824d9-124">Buffer strutturato</span><span class="sxs-lookup"><span data-stu-id="824d9-124">Structured Buffer</span></span>

<span data-ttu-id="824d9-125">Un buffer strutturato è un buffer che contiene elementi di dimensioni uguali.</span><span class="sxs-lookup"><span data-stu-id="824d9-125">A structured buffer is a buffer that contains elements of equal sizes.</span></span> <span data-ttu-id="824d9-126">Usare una struttura con uno o più tipi di membro per definire un elemento.</span><span class="sxs-lookup"><span data-stu-id="824d9-126">Use a structure with one or more member types to define an element.</span></span> <span data-ttu-id="824d9-127">Ecco una struttura con tre membri.</span><span class="sxs-lookup"><span data-stu-id="824d9-127">Here is a structure with three members.</span></span>


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



<span data-ttu-id="824d9-128">Usare questa struttura per dichiarare un buffer strutturato come il seguente:</span><span class="sxs-lookup"><span data-stu-id="824d9-128">Use this structure to declare a structured buffer like this:</span></span>


```
StructuredBuffer<MyStruct> mySB;
```



<span data-ttu-id="824d9-129">Oltre all'indicizzazione, un buffer strutturato supporta l'accesso a un singolo membro come il seguente:</span><span class="sxs-lookup"><span data-stu-id="824d9-129">In addition to indexing, a structured buffer supports accessing a single member like this:</span></span>


```
float4 myColor = mySb[27].Color;
```



<span data-ttu-id="824d9-130">Usare i tipi di oggetti seguenti per accedere a un buffer strutturato:</span><span class="sxs-lookup"><span data-stu-id="824d9-130">Use the following object types to access a structured buffer:</span></span>

-   <span data-ttu-id="824d9-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) è un buffer strutturato di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="824d9-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) is a read only structured buffer.</span></span>
-   <span data-ttu-id="824d9-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) è un buffer strutturato di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="824d9-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) is a read/write structured buffer.</span></span>

<span data-ttu-id="824d9-133">Le [funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md) che implementano operazioni interlocked sono consentite su elementi int e uint in un **RWStructuredBuffer**.</span><span class="sxs-lookup"><span data-stu-id="824d9-133">[Atomic functions](direct3d-11-advanced-stages-cs-atomic-functions.md) which implement interlocked operations are allowed on int and uint elements in an **RWStructuredBuffer**.</span></span>

## <a name="byte-address-buffer"></a><span data-ttu-id="824d9-134">Buffer degli indirizzi byte</span><span class="sxs-lookup"><span data-stu-id="824d9-134">Byte Address Buffer</span></span>

<span data-ttu-id="824d9-135">Un buffer di indirizzi byte è un buffer il cui contenuto è indirizzabile da un offset di byte.</span><span class="sxs-lookup"><span data-stu-id="824d9-135">A byte address buffer is a buffer whose contents are addressable by a byte offset.</span></span> <span data-ttu-id="824d9-136">In genere, il contenuto di un [buffer](overviews-direct3d-11-resources-buffers-intro.md) viene indicizzato per ogni elemento usando uno stride per ogni elemento e il numero di elemento (N) come specificato da S \* N.</span><span class="sxs-lookup"><span data-stu-id="824d9-136">Normally, the contents of a [buffer](overviews-direct3d-11-resources-buffers-intro.md) are indexed per element using a stride for each element (S) and the element number (N) as given by S\*N.</span></span> <span data-ttu-id="824d9-137">Un buffer di indirizzi byte, che può essere chiamato anche buffer non elaborato, usa un offset di valore byte dall'inizio del buffer per accedere ai dati.</span><span class="sxs-lookup"><span data-stu-id="824d9-137">A byte address buffer, which can also be called a raw buffer, uses a byte value offset from the beginning of the buffer to access data.</span></span> <span data-ttu-id="824d9-138">Il valore byte deve essere un multiplo di quattro in modo che sia DWORD allineato.</span><span class="sxs-lookup"><span data-stu-id="824d9-138">The byte value must be a multiple of four so that it is DWORD aligned.</span></span> <span data-ttu-id="824d9-139">Se viene specificato un altro valore, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="824d9-139">If any other value is provided, behavior is undefined.</span></span>

<span data-ttu-id="824d9-140">Shader Model 5 introduce gli oggetti per l'accesso a un [buffer di indirizzi byte](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) di sola lettura, oltre a un [buffer di indirizzi byte di lettura e scrittura](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span><span class="sxs-lookup"><span data-stu-id="824d9-140">Shader model 5 introduces objects for accessing a [read-only byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) as well as a [read-write byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span></span> <span data-ttu-id="824d9-141">Il contenuto di un buffer di indirizzi byte è progettato per essere un Unsigned Integer a 32 bit; Se il valore nel buffer non è effettivamente un Unsigned Integer, usare una funzione come [**AsFloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) per leggerlo.</span><span class="sxs-lookup"><span data-stu-id="824d9-141">The contents of a byte address buffer is designed to be a 32-bit unsigned integer; if the value in the buffer is not really an unsigned integer, use a function such as [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) to read it.</span></span>

## <a name="unordered-access-buffer-or-texture"></a><span data-ttu-id="824d9-142">Buffer o trama di accesso non ordinato</span><span class="sxs-lookup"><span data-stu-id="824d9-142">Unordered Access Buffer or Texture</span></span>

<span data-ttu-id="824d9-143">Una risorsa di accesso non ordinato, che include buffer, trame e matrici di trama, senza campionamento multiplo, consente un accesso in lettura/scrittura non ordinato da più thread.</span><span class="sxs-lookup"><span data-stu-id="824d9-143">An unordered access resource (which includes buffers, textures, and texture arrays - without multisampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="824d9-144">Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria tramite l'utilizzo di [funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="824d9-144">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts through the use of [Atomic Functions](direct3d-11-advanced-stages-cs-atomic-functions.md).</span></span>

<span data-ttu-id="824d9-145">Creare una trama o un buffer di accesso non ordinato chiamando una funzione, ad esempio [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) o [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) , e passando il flag di **accesso non \_ \_ ordinato \_ di binding d3d11** dall'enumerazione del [**\_ \_ flag di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="824d9-145">Create an unordered access buffer or texture by calling a function such as [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) or [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and passing in the **D3D11\_BIND\_UNORDERED\_ACCESS** flag from the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumeration.</span></span>

<span data-ttu-id="824d9-146">Le risorse di accesso non ordinato possono essere limitate solo a pixel shader e compute shader.</span><span class="sxs-lookup"><span data-stu-id="824d9-146">Unordered access resources can only be bound to pixel shaders and compute shaders.</span></span> <span data-ttu-id="824d9-147">Durante l'esecuzione, i pixel shader o i compute shader eseguiti in parallelo hanno le stesse risorse di accesso non ordinato associato.</span><span class="sxs-lookup"><span data-stu-id="824d9-147">During execution, pixel shaders or compute shaders running in parallel have the same unordered access resources bound.</span></span>

### <a name="append-and-consume-buffer"></a><span data-ttu-id="824d9-148">Accoda e utilizza buffer</span><span class="sxs-lookup"><span data-stu-id="824d9-148">Append and Consume Buffer</span></span>

<span data-ttu-id="824d9-149">Un buffer di Accodamento e utilizzo è un tipo speciale di risorsa non ordinata che supporta l'aggiunta e la rimozione di valori dalla fine di un buffer in modo analogo al funzionamento di uno stack.</span><span class="sxs-lookup"><span data-stu-id="824d9-149">An append and consume buffer is a special type of an unordered resource that supports adding and removing values from the end of a buffer similar to the way a stack works.</span></span>

<span data-ttu-id="824d9-150">Un buffer di Accodamento e di utilizzo deve essere un buffer strutturato:</span><span class="sxs-lookup"><span data-stu-id="824d9-150">An append and consume buffer must be a structured buffer:</span></span>

-   [<span data-ttu-id="824d9-151">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="824d9-151">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="824d9-152">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="824d9-152">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

<span data-ttu-id="824d9-153">Usare queste risorse tramite i relativi metodi, che non usano variabili di risorsa.</span><span class="sxs-lookup"><span data-stu-id="824d9-153">Use these resources through their methods, these resources do not use resource variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="824d9-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="824d9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="824d9-155">Panoramica di Compute Shader</span><span class="sxs-lookup"><span data-stu-id="824d9-155">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 