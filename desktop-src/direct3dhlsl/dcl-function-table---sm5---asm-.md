---
title: dcl_function_table (SM5-ASM)
description: Dichiarare una tabella di funzioni.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993253"
---
# <a name="dcl_function_table-sm5---asm"></a><span data-ttu-id="cf7b7-103">\_tabella delle funzioni DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cf7b7-103">dcl\_function\_table (sm5 - asm)</span></span>

<span data-ttu-id="cf7b7-104">Dichiarare una tabella di funzioni.</span><span class="sxs-lookup"><span data-stu-id="cf7b7-104">Declare a function table.</span></span>



| <span data-ttu-id="cf7b7-105">\_tabella della funzione DCL \_ ft \# = {FB \# , FB \# ,...}</span><span class="sxs-lookup"><span data-stu-id="cf7b7-105">dcl\_function\_table ft\# = {fb\#, fb\#, ...}</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="cf7b7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf7b7-106">Item</span></span>                                                      | <span data-ttu-id="cf7b7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf7b7-107">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="cf7b7-108"><span id="ft"></span><span id="FT"></span>*ft*</span><span class="sxs-lookup"><span data-stu-id="cf7b7-108"><span id="ft"></span><span id="FT"></span>*ft*</span></span><br/> | <span data-ttu-id="cf7b7-109">\[nelle \] voci della tabella di funzioni.</span><span class="sxs-lookup"><span data-stu-id="cf7b7-109">\[in\] The function table entries.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf7b7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf7b7-110">Remarks</span></span>

<span data-ttu-id="cf7b7-111">Questa funzione dichiara una tabella di funzioni come un set di corpi di funzione dichiarati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="cf7b7-111">This function declares a function table as a set of function bodies that have been declared earlier.</span></span>

<span data-ttu-id="cf7b7-112">Si tratta di un vtable C++, ad eccezione del fatto che è presente una voce per ogni sito di chiamata per un'interfaccia anziché per ogni metodo.</span><span class="sxs-lookup"><span data-stu-id="cf7b7-112">This is like a C++ vtable except there is an entry per call site for an interface instead of per method.</span></span>

<span data-ttu-id="cf7b7-113">Non esiste alcun limite al numero di corpi delle funzioni che possono essere elencati in una tabella di funzioni.</span><span class="sxs-lookup"><span data-stu-id="cf7b7-113">There is no limit to how many function bodies can be listed in a function table.</span></span>

<span data-ttu-id="cf7b7-114">È possibile fare riferimento più volte a una determinata funzione del corpo della funzione \# in una o più tabelle di funzioni, come modalità di condivisione del codice comune.</span><span class="sxs-lookup"><span data-stu-id="cf7b7-114">It is valid for a given function body fb\# to be referenced multiple times in one or more function tables, as a way of sharing common code.</span></span>

<span data-ttu-id="cf7b7-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf7b7-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cf7b7-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="cf7b7-116">Vertex</span></span> | <span data-ttu-id="cf7b7-117">Hull</span><span class="sxs-lookup"><span data-stu-id="cf7b7-117">Hull</span></span> | <span data-ttu-id="cf7b7-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="cf7b7-118">Domain</span></span> | <span data-ttu-id="cf7b7-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="cf7b7-119">Geometry</span></span> | <span data-ttu-id="cf7b7-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="cf7b7-120">Pixel</span></span> | <span data-ttu-id="cf7b7-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="cf7b7-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cf7b7-122">X</span><span class="sxs-lookup"><span data-stu-id="cf7b7-122">X</span></span>      | <span data-ttu-id="cf7b7-123">X</span><span class="sxs-lookup"><span data-stu-id="cf7b7-123">X</span></span>    | <span data-ttu-id="cf7b7-124">X</span><span class="sxs-lookup"><span data-stu-id="cf7b7-124">X</span></span>      | <span data-ttu-id="cf7b7-125">X</span><span class="sxs-lookup"><span data-stu-id="cf7b7-125">X</span></span>        | <span data-ttu-id="cf7b7-126">X</span><span class="sxs-lookup"><span data-stu-id="cf7b7-126">X</span></span>     | <span data-ttu-id="cf7b7-127">X</span><span class="sxs-lookup"><span data-stu-id="cf7b7-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cf7b7-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="cf7b7-128">Minimum Shader Model</span></span>

<span data-ttu-id="cf7b7-129">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf7b7-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cf7b7-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="cf7b7-130">Shader Model</span></span>                                              | <span data-ttu-id="cf7b7-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="cf7b7-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cf7b7-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="cf7b7-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cf7b7-133">sì</span><span class="sxs-lookup"><span data-stu-id="cf7b7-133">yes</span></span>       |
| [<span data-ttu-id="cf7b7-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="cf7b7-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cf7b7-135">no</span><span class="sxs-lookup"><span data-stu-id="cf7b7-135">no</span></span>        |
| [<span data-ttu-id="cf7b7-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="cf7b7-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cf7b7-137">no</span><span class="sxs-lookup"><span data-stu-id="cf7b7-137">no</span></span>        |
| [<span data-ttu-id="cf7b7-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf7b7-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cf7b7-139">no</span><span class="sxs-lookup"><span data-stu-id="cf7b7-139">no</span></span>        |
| [<span data-ttu-id="cf7b7-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf7b7-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cf7b7-141">no</span><span class="sxs-lookup"><span data-stu-id="cf7b7-141">no</span></span>        |
| [<span data-ttu-id="cf7b7-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf7b7-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cf7b7-143">no</span><span class="sxs-lookup"><span data-stu-id="cf7b7-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cf7b7-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf7b7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf7b7-145">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf7b7-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





