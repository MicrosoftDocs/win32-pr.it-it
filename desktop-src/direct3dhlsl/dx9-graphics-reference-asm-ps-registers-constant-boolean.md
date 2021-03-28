---
title: Registro booleano costante (riferimenti per HLSL PS)
description: Questo registro è una raccolta di bit usati nelle istruzioni per il controllo di flusso statico (ad esempio, se bool-PS-else-PS-endif-PS).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729151"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a><span data-ttu-id="7d533-103">Registro booleano costante (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="7d533-103">Constant Boolean register (HLSL PS reference)</span></span>

<span data-ttu-id="7d533-104">Questo registro è una raccolta di bit usati nelle istruzioni per il controllo di flusso statico (ad esempio, [se bool-PS](if-bool---ps.md)  -  [else-PS](else---ps.md)  -  [endif-PS](endif---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="7d533-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - ps](if-bool---ps.md) - [else - ps](else---ps.md) - [endif - ps](endif---ps.md)).</span></span> <span data-ttu-id="7d533-105">Ne sono disponibili 16, pertanto uno shader può avere 16 condizioni di ramo indipendenti.</span><span class="sxs-lookup"><span data-stu-id="7d533-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="7d533-106">Possono essere impostate usando [defb-PS](defb---ps.md) o [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="7d533-106">They can be set using [defb - ps](defb---ps.md) or [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span></span>

<span data-ttu-id="7d533-107">Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="7d533-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="7d533-108">Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="7d533-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="7d533-109">Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader.</span><span class="sxs-lookup"><span data-stu-id="7d533-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="7d533-110">Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="7d533-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="7d533-111">Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="7d533-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="7d533-112">Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="7d533-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="7d533-113">Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.</span><span class="sxs-lookup"><span data-stu-id="7d533-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>



| <span data-ttu-id="7d533-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="7d533-114">Pixel shader versions</span></span>     | <span data-ttu-id="7d533-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="7d533-115">1\_1</span></span> | <span data-ttu-id="7d533-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="7d533-116">1\_2</span></span> | <span data-ttu-id="7d533-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7d533-117">1\_3</span></span> | <span data-ttu-id="7d533-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="7d533-118">1\_4</span></span> | <span data-ttu-id="7d533-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d533-119">2\_0</span></span> | <span data-ttu-id="7d533-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d533-120">2\_sw</span></span> | <span data-ttu-id="7d533-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7d533-121">2\_x</span></span> | <span data-ttu-id="7d533-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d533-122">3\_0</span></span> | <span data-ttu-id="7d533-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d533-123">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="7d533-124">Registro booleano costante</span><span class="sxs-lookup"><span data-stu-id="7d533-124">Constant Boolean register</span></span> |      |      |      |      |      |       | <span data-ttu-id="7d533-125">x</span><span class="sxs-lookup"><span data-stu-id="7d533-125">x</span></span>    | <span data-ttu-id="7d533-126">x</span><span class="sxs-lookup"><span data-stu-id="7d533-126">x</span></span>    | <span data-ttu-id="7d533-127">x</span><span class="sxs-lookup"><span data-stu-id="7d533-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="7d533-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d533-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d533-129">Registri</span><span class="sxs-lookup"><span data-stu-id="7d533-129">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 