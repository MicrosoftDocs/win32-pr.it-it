---
title: defi-PS
description: Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118187"
---
# <a name="defi---ps"></a><span data-ttu-id="6ddb3-103">defi-PS</span><span class="sxs-lookup"><span data-stu-id="6ddb3-103">defi - ps</span></span>

<span data-ttu-id="6ddb3-104">Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-104">Defines an integer constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ddb3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ddb3-105">Syntax</span></span>



| <span data-ttu-id="6ddb3-106">defi DST, integerValue</span><span class="sxs-lookup"><span data-stu-id="6ddb3-106">defi dst, integerValue</span></span> |
|------------------------|



 

-   <span data-ttu-id="6ddb3-107">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-107">dst is the destination register.</span></span>
-   <span data-ttu-id="6ddb3-108">integerValue è un valore intero costante.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-108">integerValue is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ddb3-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ddb3-109">Remarks</span></span>



| <span data-ttu-id="6ddb3-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6ddb3-110">Pixel shader versions</span></span> | <span data-ttu-id="6ddb3-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="6ddb3-111">1\_1</span></span> | <span data-ttu-id="6ddb3-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="6ddb3-112">1\_2</span></span> | <span data-ttu-id="6ddb3-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6ddb3-113">1\_3</span></span> | <span data-ttu-id="6ddb3-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="6ddb3-114">1\_4</span></span> | <span data-ttu-id="6ddb3-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ddb3-115">2\_0</span></span> | <span data-ttu-id="6ddb3-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6ddb3-116">2\_x</span></span> | <span data-ttu-id="6ddb3-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ddb3-117">2\_sw</span></span> | <span data-ttu-id="6ddb3-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ddb3-118">3\_0</span></span> | <span data-ttu-id="6ddb3-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ddb3-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6ddb3-120">defi</span><span class="sxs-lookup"><span data-stu-id="6ddb3-120">defi</span></span>                  |      |      |      |      |      | <span data-ttu-id="6ddb3-121">x</span><span class="sxs-lookup"><span data-stu-id="6ddb3-121">x</span></span>    | <span data-ttu-id="6ddb3-122">x</span><span class="sxs-lookup"><span data-stu-id="6ddb3-122">x</span></span>     | <span data-ttu-id="6ddb3-123">x</span><span class="sxs-lookup"><span data-stu-id="6ddb3-123">x</span></span>    | <span data-ttu-id="6ddb3-124">x</span><span class="sxs-lookup"><span data-stu-id="6ddb3-124">x</span></span>     |



 

<span data-ttu-id="6ddb3-125">L'istruzione defi definisce una costante dello shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-125">The defi instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="6ddb3-126">Sono denominate costanti immediate.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-126">These are called immediate constants.</span></span> <span data-ttu-id="6ddb3-127">Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-127">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="6ddb3-128">Esistono due modi per impostare una costante in uno shader.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="6ddb3-129">Usare defi per definire la costante direttamente all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-129">Use defi to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="6ddb3-130">Usare i metodi API per impostare una costante.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-130">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="6ddb3-131">Usare [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) per impostare una costante booleana.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>
    -   <span data-ttu-id="6ddb3-132">Usare [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) per impostare una costante a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) to set a floating-point constant.</span></span>
    -   <span data-ttu-id="6ddb3-133">Usare [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) per impostare una costante Integer.</span><span class="sxs-lookup"><span data-stu-id="6ddb3-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ddb3-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ddb3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ddb3-135">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6ddb3-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 