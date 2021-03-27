---
title: Modello HLSL shader 6,4
description: Descrive gli intrinseci di Machine Learning aggiunti al modello HLSL shader 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886050"
---
# <a name="hlsl-shader-model-64"></a><span data-ttu-id="c0bda-103">Modello HLSL shader 6,4</span><span class="sxs-lookup"><span data-stu-id="c0bda-103">HLSL Shader Model 6.4</span></span>

<span data-ttu-id="c0bda-104">Descrive gli intrinseci di Machine Learning aggiunti al modello HLSL shader 6,4.</span><span class="sxs-lookup"><span data-stu-id="c0bda-104">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span>

## <a name="shader-model-64"></a><span data-ttu-id="c0bda-105">Modello shader 6,4</span><span class="sxs-lookup"><span data-stu-id="c0bda-105">Shader Model 6.4</span></span>
<span data-ttu-id="c0bda-106">Queste funzioni intrinseche sono una funzionalità obbligatoria/supportata del modello shader 6,4.</span><span class="sxs-lookup"><span data-stu-id="c0bda-106">These intrinsics are a required/supported feature of Shader model 6.4.</span></span> <span data-ttu-id="c0bda-107">Di conseguenza, non è necessario alcun controllo del bit di funzionalità separato, oltre a garantire l'uso del modello di shader 6,4.</span><span class="sxs-lookup"><span data-stu-id="c0bda-107">Consequently, no separate capability bit check is required, beyond assuring the use of Shader Model 6.4.</span></span> <span data-ttu-id="c0bda-108">Il client minimo supportato per queste routine è Windows 10, versione 1903.</span><span class="sxs-lookup"><span data-stu-id="c0bda-108">The minimum supported client for these routines is Windows 10, version 1903.</span></span>

## <a name="shading-language-intrinsics"></a><span data-ttu-id="c0bda-109">Funzioni intrinseche di linguaggio ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="c0bda-109">Shading language intrinsics</span></span>

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="c0bda-110">Intero senza segno Dot-Product di 4 elementi e accumulo</span><span class="sxs-lookup"><span data-stu-id="c0bda-110">Unsigned Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
<span data-ttu-id="c0bda-111">Un prodotto Unsigned Integer a 4 dimensioni con aggiunta.</span><span class="sxs-lookup"><span data-stu-id="c0bda-111">A 4-dimensional unsigned integer dot-product with add.</span></span> <span data-ttu-id="c0bda-112">Moltiplica insieme ogni coppia corrispondente di byte int a 8 bit senza segno nei due DWORD di input e somma i risultati nell'accumulatore Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-112">Multiplies together each corresponding pair of unsigned 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit unsigned integer accumulator.</span></span> <span data-ttu-id="c0bda-113">Questa istruzione funziona all'interno di una singola SIMD Lane a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-113">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c0bda-114">Si presuppone che gli input siano anche di quantità a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-114">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="c0bda-115">Intero con segno Dot-Product di 4 elementi e accumulo</span><span class="sxs-lookup"><span data-stu-id="c0bda-115">Signed Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

<span data-ttu-id="c0bda-116">Intero con segno a 4 dimensioni-prodotto con aggiunta.</span><span class="sxs-lookup"><span data-stu-id="c0bda-116">A 4-dimensional signed integer dot-product with add.</span></span> <span data-ttu-id="c0bda-117">Moltiplica insieme ogni coppia corrispondente di byte int a 8 bit con segno nei due valori DWORD di input e somma i risultati nell'accumulatore di interi con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-117">Multiplies together each corresponding pair of signed 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit signed integer accumulator.</span></span> <span data-ttu-id="c0bda-118">Questa istruzione funziona all'interno di una singola SIMD Lane a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-118">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c0bda-119">Si presuppone che gli input siano anche di quantità a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-119">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a><span data-ttu-id="c0bda-120">Dot-Product e accumulo a virgola mobile a precisione singola a 2 elementi</span><span class="sxs-lookup"><span data-stu-id="c0bda-120">Single Precision Floating Point 2-Element Dot-Product and Accumulate</span></span>
```syntax
float dot2add( half2 a, half2 b, float acc );
```

<span data-ttu-id="c0bda-121">Prodotto a virgola mobile a virgola mobile bidimensionale di vettori Half2 con Add.</span><span class="sxs-lookup"><span data-stu-id="c0bda-121">A 2-dimensional floating point dot-product of half2 vectors with add.</span></span> <span data-ttu-id="c0bda-122">Moltiplica gli elementi dei due vettori di input float a metà precisione insieme e somma i risultati nell'accumulatore float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-122">Multiplies the elements of the two half-precision float input vectors together and sums the results into the 32-bit float accumulator.</span></span> <span data-ttu-id="c0bda-123">Queste istruzioni operano all'interno di una singola SIMD Lane a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c0bda-123">This instructions operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c0bda-124">Gli input sono quantità a 16 bit compressi nella stessa corsia.</span><span class="sxs-lookup"><span data-stu-id="c0bda-124">The inputs are 16-bit quantities packed into the same lane.</span></span>

<span data-ttu-id="c0bda-125">Questa operazione viene illustrata sotto il bit di funzionalità a bassa precisione, che indica che sono presenti la metà nativa e il supporto breve.</span><span class="sxs-lookup"><span data-stu-id="c0bda-125">This is covered under the low-precision feature bit (indicating that native half and short support are present).</span></span>

### <a name="sv_shadingrate"></a><span data-ttu-id="c0bda-126">SV_ShadingRate</span><span class="sxs-lookup"><span data-stu-id="c0bda-126">SV_ShadingRate</span></span>
```syntax
uint shadingRate : SV_ShadingRate
```

<span data-ttu-id="c0bda-127">Unsigned Integer che rappresenta il numero di pixel di destinazione scritti da ogni chiamata del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c0bda-127">An unsigned integer representing how many target pixels are written by each invocation of the pixel shader.</span></span> <span data-ttu-id="c0bda-128">I valori validi appartengono al set di valori di enumerazione [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span><span class="sxs-lookup"><span data-stu-id="c0bda-128">Valid values belong to set of enumeration values [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span></span>

<span data-ttu-id="c0bda-129">Questo valore di sistema è disponibile sulle piattaforme [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c0bda-129">This system value is available on platforms that are [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) or higher.</span></span> <span data-ttu-id="c0bda-130">Può essere scritta al massimo da una delle fasi vertex o geometry shader.</span><span class="sxs-lookup"><span data-stu-id="c0bda-130">It can be written from at most one of vertex or geometry shader stages.</span></span> <span data-ttu-id="c0bda-131">Può essere letto dalla fase pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c0bda-131">It can be read from the pixel shader stage.</span></span> <span data-ttu-id="c0bda-132">Per altre informazioni, vedere [ombreggiatura a frequenza variabile](../direct3d12/vrs.md).</span><span class="sxs-lookup"><span data-stu-id="c0bda-132">For more information, see the [Variable-rate Shading](../direct3d12/vrs.md).</span></span>