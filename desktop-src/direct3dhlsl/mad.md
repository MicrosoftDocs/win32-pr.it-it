---
title: mad (funzione)
description: Esegue un'operazione di moltiplicazione/aggiunta aritmetica su tre valori.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- funzione MAD HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104472006"
---
# <a name="mad-function"></a><span data-ttu-id="617a6-104">mad (funzione)</span><span class="sxs-lookup"><span data-stu-id="617a6-104">mad function</span></span>

<span data-ttu-id="617a6-105">Esegue un'operazione di moltiplicazione/aggiunta aritmetica su tre valori.</span><span class="sxs-lookup"><span data-stu-id="617a6-105">Performs an arithmetic multiply/add operation on three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="617a6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="617a6-106">Syntax</span></span>

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a><span data-ttu-id="617a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="617a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="617a6-108">*mvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="617a6-108">*mvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="617a6-109">Tipo: **numerico**</span><span class="sxs-lookup"><span data-stu-id="617a6-109">Type: **numeric**</span></span>

<span data-ttu-id="617a6-110">Valore di moltiplicazione.</span><span class="sxs-lookup"><span data-stu-id="617a6-110">The multiplication value.</span></span>

</dd> <dt>

<span data-ttu-id="617a6-111">*avalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="617a6-111">*avalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="617a6-112">Tipo: **numerico**</span><span class="sxs-lookup"><span data-stu-id="617a6-112">Type: **numeric**</span></span>

<span data-ttu-id="617a6-113">Primo valore di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="617a6-113">The first addition value.</span></span>

</dd> <dt>

<span data-ttu-id="617a6-114">*bValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="617a6-114">*bvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="617a6-115">Tipo: **numerico**</span><span class="sxs-lookup"><span data-stu-id="617a6-115">Type: **numeric**</span></span>

<span data-ttu-id="617a6-116">Secondo valore di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="617a6-116">The second addition value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="617a6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="617a6-117">Return value</span></span>

<span data-ttu-id="617a6-118">Tipo: **numerico**</span><span class="sxs-lookup"><span data-stu-id="617a6-118">Type: **numeric**</span></span>

<span data-ttu-id="617a6-119">Risultato di *mvalue* \* *avalue*  +  *bValue*.</span><span class="sxs-lookup"><span data-stu-id="617a6-119">The result of *mvalue* \* *avalue* + *bvalue*.</span></span>

## <a name="remarks"></a><span data-ttu-id="617a6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="617a6-120">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="617a6-121">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="617a6-121">Minimum Shader Model</span></span>

<span data-ttu-id="617a6-122">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="617a6-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="617a6-123">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="617a6-123">Shader Model</span></span>                                                                | <span data-ttu-id="617a6-124">Supportato</span><span class="sxs-lookup"><span data-stu-id="617a6-124">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="617a6-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="617a6-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="617a6-126">sì</span><span class="sxs-lookup"><span data-stu-id="617a6-126">yes</span></span>       |



 

<span data-ttu-id="617a6-127">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="617a6-127">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="617a6-128">Vertice</span><span class="sxs-lookup"><span data-stu-id="617a6-128">Vertex</span></span> | <span data-ttu-id="617a6-129">Hull</span><span class="sxs-lookup"><span data-stu-id="617a6-129">Hull</span></span> | <span data-ttu-id="617a6-130">Dominio</span><span class="sxs-lookup"><span data-stu-id="617a6-130">Domain</span></span> | <span data-ttu-id="617a6-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="617a6-131">Geometry</span></span> | <span data-ttu-id="617a6-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="617a6-132">Pixel</span></span> | <span data-ttu-id="617a6-133">Calcolo</span><span class="sxs-lookup"><span data-stu-id="617a6-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="617a6-134">x</span><span class="sxs-lookup"><span data-stu-id="617a6-134">x</span></span>      | <span data-ttu-id="617a6-135">x</span><span class="sxs-lookup"><span data-stu-id="617a6-135">x</span></span>    | <span data-ttu-id="617a6-136">x</span><span class="sxs-lookup"><span data-stu-id="617a6-136">x</span></span>      | <span data-ttu-id="617a6-137">x</span><span class="sxs-lookup"><span data-stu-id="617a6-137">x</span></span>        | <span data-ttu-id="617a6-138">x</span><span class="sxs-lookup"><span data-stu-id="617a6-138">x</span></span>     | <span data-ttu-id="617a6-139">x</span><span class="sxs-lookup"><span data-stu-id="617a6-139">x</span></span>       |



 

<span data-ttu-id="617a6-140">Gli autori dello shader possono usare il intrinseche **MAD** per impostare in modo esplicito come destinazione l'istruzione hardware **MAD** nell'output dello shader compilato, che è particolarmente utile con gli shader che contrassegnano i risultati con la parola chiave [precisa](dx-graphics-hlsl-appendix-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="617a6-140">Shader authors can use the **mad** instrinsic to explicitly target the **mad** hardware instruction in the compiled shader output, which is particularly useful with shaders that mark results with the [precise](dx-graphics-hlsl-appendix-keywords.md) keyword.</span></span> <span data-ttu-id="617a6-141">L'istruzione **MAD** può essere implementata nell'hardware come "con fusione", che offre una maggiore precisione rispetto all'implementazione di un'istruzione **mul** seguita da un'istruzione **Add** o da un'operazione **mul**  +  **Add**.</span><span class="sxs-lookup"><span data-stu-id="617a6-141">The **mad** instruction can be implemented in hardware as either "fused," which offers higher precision than implementing a **mul** instruction followed by an **add** instruction, or as a **mul** + **add**.</span></span>

<span data-ttu-id="617a6-142">Se gli autori dello shader usano il intrinseche **MAD** per calcolare un risultato contrassegnato come preciso dallo shader, indicano all'hardware di usare qualsiasi implementazione valida dell'istruzione **MAD** (fusa o meno), purché l'implementazione sia coerente per tutti gli usi di tale intrinseca intrinseca in qualsiasi shader **su tale hardware** .</span><span class="sxs-lookup"><span data-stu-id="617a6-142">If shader authors use the **mad** instrinsic to calculate a result that the shader marked as precise, they indicate to the hardware to use any valid implementation of the **mad** instruction (fused or not) as long as the implementation is consistent for all uses of that **mad** intrinsic in any shader on that hardware.</span></span> <span data-ttu-id="617a6-143">Gli shader possono quindi sfruttare i vantaggi dei potenziali miglioramenti delle prestazioni usando un'istruzione **MAD** nativa (rispetto a **mul**  +  **Add**) su alcuni componenti hardware.</span><span class="sxs-lookup"><span data-stu-id="617a6-143">Shaders can then take advantage of potential performance improvements by using a native **mad** instruction (versus **mul** + **add**) on some hardware.</span></span> <span data-ttu-id="617a6-144">Il risultato dell'esecuzione di un'istruzione hardware **MAD** nativa potrebbe essere diverso rispetto all'esecuzione di un **mul** seguito da un **Add**.</span><span class="sxs-lookup"><span data-stu-id="617a6-144">The result of performing a native **mad** hardware instruction might or might not be different than performing a **mul** followed by an **add**.</span></span> <span data-ttu-id="617a6-145">Tuttavia, qualunque sia il risultato, il risultato deve essere coerente affinché la stessa operazione venga eseguita in più shader o in parti diverse di uno shader.</span><span class="sxs-lookup"><span data-stu-id="617a6-145">However, whatever the result is, the result must be consistent for the same operation to occur in multiple shaders or different parts of a shader.</span></span>

## <a name="see-also"></a><span data-ttu-id="617a6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="617a6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="617a6-147">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="617a6-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="617a6-148">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="617a6-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




