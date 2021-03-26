---
title: def-PS
description: Definisce pixel shader costanti a virgola mobile.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047302"
---
# <a name="def---ps"></a><span data-ttu-id="3a2dd-103">def-PS</span><span class="sxs-lookup"><span data-stu-id="3a2dd-103">def - ps</span></span>

<span data-ttu-id="3a2dd-104">Definisce pixel shader costanti a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-104">Defines pixel shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a2dd-105">Syntax</span></span>



| <span data-ttu-id="3a2dd-106">def DST, fVvalue1, fValue2, fValue3, fValue4</span><span class="sxs-lookup"><span data-stu-id="3a2dd-106">def dst, fVvalue1, fValue2, fValue3, fValue4</span></span> |
|----------------------------------------------|



 

<span data-ttu-id="3a2dd-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="3a2dd-107">Where:</span></span>

-   <span data-ttu-id="3a2dd-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3a2dd-109">fValue1 a fValue4 sono valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-109">fValue1 to fValue4 are floating-point values..</span></span>

## <a name="remarks"></a><span data-ttu-id="3a2dd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a2dd-110">Remarks</span></span>



| <span data-ttu-id="3a2dd-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3a2dd-111">Pixel shader versions</span></span> | <span data-ttu-id="3a2dd-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="3a2dd-112">1\_1</span></span> | <span data-ttu-id="3a2dd-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="3a2dd-113">1\_2</span></span> | <span data-ttu-id="3a2dd-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3a2dd-114">1\_3</span></span> | <span data-ttu-id="3a2dd-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="3a2dd-115">1\_4</span></span> | <span data-ttu-id="3a2dd-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a2dd-116">2\_0</span></span> | <span data-ttu-id="3a2dd-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-117">2\_x</span></span> | <span data-ttu-id="3a2dd-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3a2dd-118">2\_sw</span></span> | <span data-ttu-id="3a2dd-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a2dd-119">3\_0</span></span> | <span data-ttu-id="3a2dd-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3a2dd-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3a2dd-121">def</span><span class="sxs-lookup"><span data-stu-id="3a2dd-121">def</span></span>                   | <span data-ttu-id="3a2dd-122">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-122">x</span></span>    | <span data-ttu-id="3a2dd-123">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-123">x</span></span>    | <span data-ttu-id="3a2dd-124">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-124">x</span></span>    | <span data-ttu-id="3a2dd-125">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-125">x</span></span>    | <span data-ttu-id="3a2dd-126">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-126">x</span></span>    | <span data-ttu-id="3a2dd-127">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-127">x</span></span>    | <span data-ttu-id="3a2dd-128">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-128">x</span></span>     | <span data-ttu-id="3a2dd-129">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-129">x</span></span>    | <span data-ttu-id="3a2dd-130">x</span><span class="sxs-lookup"><span data-stu-id="3a2dd-130">x</span></span>     |



 

<span data-ttu-id="3a2dd-131">Esistono due modi per impostare una costante a virgola mobile in una pixel shader.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-131">There are two ways to set a floating-point constant in a pixel shader.</span></span>

1.  <span data-ttu-id="3a2dd-132">Usare def per definire la costante direttamente all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-132">Use def to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="3a2dd-133">Usare l'API per impostare una costante con [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="3a2dd-133">Use the API to set a constant with [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="3a2dd-134">def definisce una costante dello shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-134">def defines a shader constant whose value is loaded any time a shader is set to a device.</span></span> <span data-ttu-id="3a2dd-135">Sono denominate costanti immediate.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-135">These are called immediate constants.</span></span> <span data-ttu-id="3a2dd-136">Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-136">Immediate constants take precedence over constants set by the API method.</span></span>

-   <span data-ttu-id="3a2dd-137">Deve comparire prima della prima istruzione aritmetica o di indirizzamento nello shader.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-137">Must appear before the first arithmetic or addressing instruction in shader.</span></span>
-   <span data-ttu-id="3a2dd-138">È possibile combinare le istruzioni [DCL-(SM2, SM3-PS ASM),](dcl---ps.md) ovvero l'altro tipo di istruzione che risiede all'inizio di uno shader.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-138">Can be intermixed with [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) instructions (which are the other type of instruction that resides at the beginning of a shader).</span></span>
-   <span data-ttu-id="3a2dd-139">il registro DST deve essere un [registro costante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="3a2dd-139">dst register must be a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>
-   <span data-ttu-id="3a2dd-140">La maschera di scrittura deve essere piena (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="3a2dd-140">Write mask must be full (default).</span></span>
-   <span data-ttu-id="3a2dd-141">Se un [registro costante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) viene definito più volte in uno shader, l'ultimo viene reso permanente.</span><span class="sxs-lookup"><span data-stu-id="3a2dd-141">If a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) is defined multiple times in a shader, the last one persists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a2dd-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a2dd-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a2dd-143">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3a2dd-143">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 