---
title: RestartStrip (oggetto Stream-Output DirectX HLSL)
description: Termina la striscia primitiva corrente e avvia una nuova striscia. Se la striscia corrente non ha un numero di vertici sufficiente per riempire la topologia primitiva, la primitiva incompleta alla fine verrà eliminata.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120196"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="0f037-104">RestartStrip (oggetto Stream-Output DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f037-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="0f037-105">Termina la striscia primitiva corrente e avvia una nuova striscia.</span><span class="sxs-lookup"><span data-stu-id="0f037-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="0f037-106">Se la striscia corrente non ha un numero di vertici sufficiente per riempire la topologia primitiva, la primitiva incompleta alla fine verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="0f037-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>

<span data-ttu-id="0f037-107">RestartStrip();</span><span class="sxs-lookup"><span data-stu-id="0f037-107">RestartStrip();</span></span>



 

## <a name="parameters"></a><span data-ttu-id="0f037-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f037-108">Parameters</span></span>



| <span data-ttu-id="0f037-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f037-109">Item</span></span>                                                                                     | <span data-ttu-id="0f037-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f037-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="0f037-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno**</span><span class="sxs-lookup"><span data-stu-id="0f037-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="0f037-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f037-112">Return Value</span></span>

<span data-ttu-id="0f037-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="0f037-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="0f037-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="0f037-114">Remarks</span></span>

<span data-ttu-id="0f037-115">Un taglio di strip determina la fine della striscia corrente e l'avvio di una nuova striscia.</span><span class="sxs-lookup"><span data-stu-id="0f037-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="0f037-116">È possibile eseguire un strip cut chiamando in modo esplicito questo metodo o semplicemente effettuando il rendering fino al valore massimo dell'indice ( 1, che è 0xffffffff per indici a 32 bit o 0xffff per indici a 16 bit).</span><span class="sxs-lookup"><span data-stu-id="0f037-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="0f037-117">Ogni istanza di un disegno con istanze indicizzate genera automaticamente un strip cut.</span><span class="sxs-lookup"><span data-stu-id="0f037-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="0f037-118">Questo vale anche se la topologia non è una striscia a triangolo.</span><span class="sxs-lookup"><span data-stu-id="0f037-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="0f037-119">Il supporto per il riavvio e l'1 [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) "valore magico" per un taglio sono disponibili solo nei dispositivi con livello di funzionalità 10.0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0f037-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="0f037-120">Si presuppone sempre che l'output sia una striscia triangolare.</span><span class="sxs-lookup"><span data-stu-id="0f037-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="0f037-121">Per rendere l'output un elenco di triangoli, è necessario chiamare RestartStrip tra ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="0f037-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="0f037-122">Le ventole a triangolo non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="0f037-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0f037-123">Modello shader minimo</span><span class="sxs-lookup"><span data-stu-id="0f037-123">Minimum Shader Model</span></span>

<span data-ttu-id="0f037-124">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0f037-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0f037-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0f037-125">Shader Model</span></span>                                              | <span data-ttu-id="0f037-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="0f037-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0f037-127">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="0f037-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f037-128">yes</span><span class="sxs-lookup"><span data-stu-id="0f037-128">yes</span></span>       |
| [<span data-ttu-id="0f037-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f037-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f037-130">No</span><span class="sxs-lookup"><span data-stu-id="0f037-130">no</span></span>        |
| [<span data-ttu-id="0f037-131">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f037-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f037-132">No</span><span class="sxs-lookup"><span data-stu-id="0f037-132">no</span></span>        |
| [<span data-ttu-id="0f037-133">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f037-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f037-134">No</span><span class="sxs-lookup"><span data-stu-id="0f037-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0f037-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f037-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f037-136">Oggetto stream-output</span><span class="sxs-lookup"><span data-stu-id="0f037-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

