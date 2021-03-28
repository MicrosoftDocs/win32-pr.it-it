---
title: RestartStrip (oggetto Stream-Output DirectX HLSL)
description: Termina la striscia primitiva corrente e avvia una nuova striscia. Se la striscia corrente non ha un numero sufficiente di vertici emessi per riempire la topologia primitiva, la primitiva incompleta alla fine verrà ignorata.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16b31bbd1e2f72ce6b31a0c079f7ec5739aba87a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993424"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="1e769-104">RestartStrip (oggetto Stream-Output DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e769-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="1e769-105">Termina la striscia primitiva corrente e avvia una nuova striscia.</span><span class="sxs-lookup"><span data-stu-id="1e769-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="1e769-106">Se la striscia corrente non ha un numero sufficiente di vertici emessi per riempire la topologia primitiva, la primitiva incompleta alla fine verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="1e769-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>



|                 |
|-----------------|
| <span data-ttu-id="1e769-107">RestartStrip();</span><span class="sxs-lookup"><span data-stu-id="1e769-107">RestartStrip();</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="1e769-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e769-108">Parameters</span></span>



| <span data-ttu-id="1e769-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1e769-109">Item</span></span>                                                                                     | <span data-ttu-id="1e769-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e769-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="1e769-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno**</span><span class="sxs-lookup"><span data-stu-id="1e769-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="1e769-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e769-112">Return Value</span></span>

<span data-ttu-id="1e769-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="1e769-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="1e769-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1e769-114">Remarks</span></span>

<span data-ttu-id="1e769-115">Un taglio striscia causa la fine della striscia corrente e una nuova striscia da avviare.</span><span class="sxs-lookup"><span data-stu-id="1e769-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="1e769-116">Una striscia può essere eseguita chiamando in modo esplicito questo metodo o semplicemente eseguendo il rendering fino al valore di indice massimo (1, ovvero 0xFFFFFFFF per gli indici a 32 bit o 0xFFFF per gli indici a 16 bit).</span><span class="sxs-lookup"><span data-stu-id="1e769-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="1e769-117">Ogni istanza di un oggetto di estrazione con istanza indicizzata genera automaticamente uno strip Cut.</span><span class="sxs-lookup"><span data-stu-id="1e769-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="1e769-118">Questo vale anche se la topologia non è una striscia di triangolo.</span><span class="sxs-lookup"><span data-stu-id="1e769-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="1e769-119">Il supporto per il riavvio e il valore "Magic value" per un taglio sono disponibili solo su dispositivi di [livello funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 o superiore.</span><span class="sxs-lookup"><span data-stu-id="1e769-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="1e769-120">L'output viene sempre considerato una striscia di triangolo.</span><span class="sxs-lookup"><span data-stu-id="1e769-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="1e769-121">Per rendere l'output un elenco di triangolo, è necessario chiamare RestartStrip tra ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="1e769-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="1e769-122">Le ventole del triangolo non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="1e769-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="1e769-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="1e769-123">Minimum Shader Model</span></span>

<span data-ttu-id="1e769-124">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="1e769-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1e769-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="1e769-125">Shader Model</span></span>                                              | <span data-ttu-id="1e769-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="1e769-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1e769-127">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="1e769-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1e769-128">sì</span><span class="sxs-lookup"><span data-stu-id="1e769-128">yes</span></span>       |
| [<span data-ttu-id="1e769-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e769-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1e769-130">no</span><span class="sxs-lookup"><span data-stu-id="1e769-130">no</span></span>        |
| [<span data-ttu-id="1e769-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e769-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1e769-132">no</span><span class="sxs-lookup"><span data-stu-id="1e769-132">no</span></span>        |
| [<span data-ttu-id="1e769-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e769-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1e769-134">no</span><span class="sxs-lookup"><span data-stu-id="1e769-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1e769-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e769-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e769-136">Stream-oggetto di output</span><span class="sxs-lookup"><span data-stu-id="1e769-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

