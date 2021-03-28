---
title: defb-vs
description: Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963108"
---
# <a name="defb---vs"></a><span data-ttu-id="9773e-103">defb-vs</span><span class="sxs-lookup"><span data-stu-id="9773e-103">defb - vs</span></span>

<span data-ttu-id="9773e-104">Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9773e-104">Defines a Boolean constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9773e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9773e-105">Syntax</span></span>



| <span data-ttu-id="9773e-106">defb dest, booleanValue</span><span class="sxs-lookup"><span data-stu-id="9773e-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="9773e-107">dove</span><span class="sxs-lookup"><span data-stu-id="9773e-107">where</span></span>

-   <span data-ttu-id="9773e-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9773e-108">dst is the destination register.</span></span>
-   <span data-ttu-id="9773e-109">booleanValue è un valore booleano, ovvero true o false.</span><span class="sxs-lookup"><span data-stu-id="9773e-109">booleanValue is a boolean value, either True or False.</span></span>

## <a name="remarks"></a><span data-ttu-id="9773e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9773e-110">Remarks</span></span>



| <span data-ttu-id="9773e-111">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="9773e-111">Vertex shader versions</span></span> | <span data-ttu-id="9773e-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="9773e-112">1\_1</span></span> | <span data-ttu-id="9773e-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9773e-113">2\_0</span></span> | <span data-ttu-id="9773e-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9773e-114">2\_x</span></span> | <span data-ttu-id="9773e-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9773e-115">2\_sw</span></span> | <span data-ttu-id="9773e-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9773e-116">3\_0</span></span> | <span data-ttu-id="9773e-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9773e-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9773e-118">defb</span><span class="sxs-lookup"><span data-stu-id="9773e-118">defb</span></span>                   |      | <span data-ttu-id="9773e-119">x</span><span class="sxs-lookup"><span data-stu-id="9773e-119">x</span></span>    | <span data-ttu-id="9773e-120">x</span><span class="sxs-lookup"><span data-stu-id="9773e-120">x</span></span>    | <span data-ttu-id="9773e-121">x</span><span class="sxs-lookup"><span data-stu-id="9773e-121">x</span></span>     | <span data-ttu-id="9773e-122">x</span><span class="sxs-lookup"><span data-stu-id="9773e-122">x</span></span>    | <span data-ttu-id="9773e-123">x</span><span class="sxs-lookup"><span data-stu-id="9773e-123">x</span></span>     |



 

<span data-ttu-id="9773e-124">L'istruzione defb-vs definisce una costante dello shader booleano il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9773e-124">The defb - vs instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="9773e-125">Sono denominate costanti immediate.</span><span class="sxs-lookup"><span data-stu-id="9773e-125">These are called immediate constants.</span></span> <span data-ttu-id="9773e-126">Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetVertexShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="9773e-126">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantB.</span></span>

<span data-ttu-id="9773e-127">Esistono due modi per impostare una costante booleana in uno shader.</span><span class="sxs-lookup"><span data-stu-id="9773e-127">There are two ways to set a boolean constant in a shader.</span></span>

1.  <span data-ttu-id="9773e-128">Usare defb-vs per definire la costante direttamente all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="9773e-128">Use defb - vs to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="9773e-129">Usare i metodi API per impostare una costante.</span><span class="sxs-lookup"><span data-stu-id="9773e-129">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="9773e-130">Usare [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) per impostare una costante booleana.</span><span class="sxs-lookup"><span data-stu-id="9773e-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9773e-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9773e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9773e-132">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="9773e-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="9773e-133">def-vs</span><span class="sxs-lookup"><span data-stu-id="9773e-133">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="9773e-134">defi-vs</span><span class="sxs-lookup"><span data-stu-id="9773e-134">defi - vs</span></span>](defi---vs.md)
</dt> </dl>

 

 