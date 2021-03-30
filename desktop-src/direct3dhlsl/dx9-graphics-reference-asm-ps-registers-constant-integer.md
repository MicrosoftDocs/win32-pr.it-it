---
title: Registro Integer costante (riferimenti per HLSL PS)
description: I registri di tipo integer costanti vengono usati solo da loop-PS e Rep-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976754"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a><span data-ttu-id="69c8d-103">Registro Integer costante (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="69c8d-103">Constant integer register (HLSL PS reference)</span></span>

<span data-ttu-id="69c8d-104">I registri di tipo integer costanti vengono usati solo da [loop-PS](loop---ps.md) e [Rep-PS](rep---ps.md).</span><span class="sxs-lookup"><span data-stu-id="69c8d-104">Constant integer registers are used only by [loop - ps](loop---ps.md) and [rep - ps](rep---ps.md).</span></span>

<span data-ttu-id="69c8d-105">Possono essere impostate tramite [defi-PS](defi---ps.md) o [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="69c8d-105">They can be set using [defi - ps](defi---ps.md) or [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span></span>

<span data-ttu-id="69c8d-106">Quando viene usato come argomento dell'istruzione [loop-PS](loop---ps.md) :</span><span class="sxs-lookup"><span data-stu-id="69c8d-106">When used as an argument to the [loop - ps](loop---ps.md) instruction:</span></span>

-   <span data-ttu-id="69c8d-107">. x è il numero di iterazioni.</span><span class="sxs-lookup"><span data-stu-id="69c8d-107">.x is the iteration count.</span></span> <span data-ttu-id="69c8d-108">([Rep-PS](rep---ps.md) usa solo questo componente).</span><span class="sxs-lookup"><span data-stu-id="69c8d-108">([rep - ps](rep---ps.md) uses only this component).</span></span>
-   <span data-ttu-id="69c8d-109">. y è il valore iniziale del contatore di cicli.</span><span class="sxs-lookup"><span data-stu-id="69c8d-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="69c8d-110">. z è il passaggio di incremento per il contatore del ciclo.</span><span class="sxs-lookup"><span data-stu-id="69c8d-110">.z is the increment step for the loop counter.</span></span>



| <span data-ttu-id="69c8d-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="69c8d-111">Pixel shader versions</span></span>     | <span data-ttu-id="69c8d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="69c8d-112">1\_1</span></span> | <span data-ttu-id="69c8d-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="69c8d-113">1\_2</span></span> | <span data-ttu-id="69c8d-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="69c8d-114">1\_3</span></span> | <span data-ttu-id="69c8d-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="69c8d-115">1\_4</span></span> | <span data-ttu-id="69c8d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69c8d-116">2\_0</span></span> | <span data-ttu-id="69c8d-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="69c8d-117">2\_sw</span></span> | <span data-ttu-id="69c8d-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="69c8d-118">2\_x</span></span> | <span data-ttu-id="69c8d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69c8d-119">3\_0</span></span> | <span data-ttu-id="69c8d-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="69c8d-120">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="69c8d-121">Registro Integer costante</span><span class="sxs-lookup"><span data-stu-id="69c8d-121">Constant Integer Register</span></span> |      |      |      |      |      |       | <span data-ttu-id="69c8d-122">x</span><span class="sxs-lookup"><span data-stu-id="69c8d-122">x</span></span>    | <span data-ttu-id="69c8d-123">x</span><span class="sxs-lookup"><span data-stu-id="69c8d-123">x</span></span>    | <span data-ttu-id="69c8d-124">x</span><span class="sxs-lookup"><span data-stu-id="69c8d-124">x</span></span>     |



 

<span data-ttu-id="69c8d-125">Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="69c8d-125">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="69c8d-126">Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="69c8d-126">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="69c8d-127">Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader.</span><span class="sxs-lookup"><span data-stu-id="69c8d-127">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="69c8d-128">Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="69c8d-128">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="69c8d-129">Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="69c8d-129">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="69c8d-130">Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="69c8d-130">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="69c8d-131">Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.</span><span class="sxs-lookup"><span data-stu-id="69c8d-131">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69c8d-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69c8d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69c8d-133">Registri</span><span class="sxs-lookup"><span data-stu-id="69c8d-133">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 