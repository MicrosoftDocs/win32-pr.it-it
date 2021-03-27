---
title: defb-PS
description: Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729175"
---
# <a name="defb---ps"></a><span data-ttu-id="25c94-103">defb-PS</span><span class="sxs-lookup"><span data-stu-id="25c94-103">defb - ps</span></span>

<span data-ttu-id="25c94-104">Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25c94-104">Defines a boolean constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c94-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25c94-105">Syntax</span></span>



| <span data-ttu-id="25c94-106">defb dest, booleanValue</span><span class="sxs-lookup"><span data-stu-id="25c94-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="25c94-107">dove</span><span class="sxs-lookup"><span data-stu-id="25c94-107">where</span></span>

-   <span data-ttu-id="25c94-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="25c94-108">dst is the destination register.</span></span>
-   <span data-ttu-id="25c94-109">booleanValue è un singolo valore booleano, ovvero true o false.</span><span class="sxs-lookup"><span data-stu-id="25c94-109">booleanValue is a single boolean value, either true or false.</span></span>

## <a name="remarks"></a><span data-ttu-id="25c94-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="25c94-110">Remarks</span></span>



| <span data-ttu-id="25c94-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="25c94-111">Pixel shader versions</span></span> | <span data-ttu-id="25c94-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="25c94-112">1\_1</span></span> | <span data-ttu-id="25c94-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="25c94-113">1\_2</span></span> | <span data-ttu-id="25c94-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="25c94-114">1\_3</span></span> | <span data-ttu-id="25c94-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="25c94-115">1\_4</span></span> | <span data-ttu-id="25c94-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="25c94-116">2\_0</span></span> | <span data-ttu-id="25c94-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="25c94-117">2\_x</span></span> | <span data-ttu-id="25c94-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="25c94-118">2\_sw</span></span> | <span data-ttu-id="25c94-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="25c94-119">3\_0</span></span> | <span data-ttu-id="25c94-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="25c94-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="25c94-121">defb</span><span class="sxs-lookup"><span data-stu-id="25c94-121">defb</span></span>                  |      |      |      |      |      | <span data-ttu-id="25c94-122">x</span><span class="sxs-lookup"><span data-stu-id="25c94-122">x</span></span>    | <span data-ttu-id="25c94-123">x</span><span class="sxs-lookup"><span data-stu-id="25c94-123">x</span></span>     | <span data-ttu-id="25c94-124">x</span><span class="sxs-lookup"><span data-stu-id="25c94-124">x</span></span>    | <span data-ttu-id="25c94-125">x</span><span class="sxs-lookup"><span data-stu-id="25c94-125">x</span></span>     |



 

<span data-ttu-id="25c94-126">L'istruzione defb definisce una costante dello shader booleano il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25c94-126">The defb instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="25c94-127">Sono denominate costanti immediate.</span><span class="sxs-lookup"><span data-stu-id="25c94-127">These are called immediate constants.</span></span> <span data-ttu-id="25c94-128">Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="25c94-128">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="25c94-129">Esistono due modi per impostare un booleanconstant in uno shader.</span><span class="sxs-lookup"><span data-stu-id="25c94-129">There are two ways to set a booleanconstant in a shader.</span></span>

1.  <span data-ttu-id="25c94-130">Usare defb per definire la costante direttamente all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="25c94-130">Use defb to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="25c94-131">Usare i metodi API per impostare una costante.</span><span class="sxs-lookup"><span data-stu-id="25c94-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="25c94-132">Usare [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) per impostare una costante booleana.</span><span class="sxs-lookup"><span data-stu-id="25c94-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25c94-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25c94-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25c94-134">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="25c94-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="25c94-135">def-PS</span><span class="sxs-lookup"><span data-stu-id="25c94-135">def - ps</span></span>](def---ps.md)
</dt> <dt>

[<span data-ttu-id="25c94-136">defi-PS</span><span class="sxs-lookup"><span data-stu-id="25c94-136">defi - ps</span></span>](defi---ps.md)
</dt> </dl>

 

 