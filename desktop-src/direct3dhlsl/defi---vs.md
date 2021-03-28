---
title: defi-vs
description: Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517007"
---
# <a name="defi---vs"></a><span data-ttu-id="8a8fb-103">defi-vs</span><span class="sxs-lookup"><span data-stu-id="8a8fb-103">defi - vs</span></span>

<span data-ttu-id="8a8fb-104">Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-104">Defines an integer constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a8fb-105">Syntax</span></span>



| <span data-ttu-id="8a8fb-106">defi DST, integerValue0, integerValue1, integerValue2, integerValue3</span><span class="sxs-lookup"><span data-stu-id="8a8fb-106">defi dst, integerValue0, integerValue1, integerValue2, integerValue3</span></span> |
|----------------------------------------------------------------------|



 

-   <span data-ttu-id="8a8fb-107">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-107">dst is the destination register.</span></span>
-   <span data-ttu-id="8a8fb-108">integerValue \# è un valore intero costante.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-108">integerValue\# is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a8fb-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a8fb-109">Remarks</span></span>



| <span data-ttu-id="8a8fb-110">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="8a8fb-110">Vertex shader versions</span></span> | <span data-ttu-id="8a8fb-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="8a8fb-111">1\_1</span></span> | <span data-ttu-id="8a8fb-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8a8fb-112">2\_0</span></span> | <span data-ttu-id="8a8fb-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8a8fb-113">2\_x</span></span> | <span data-ttu-id="8a8fb-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8a8fb-114">2\_sw</span></span> | <span data-ttu-id="8a8fb-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8a8fb-115">3\_0</span></span> | <span data-ttu-id="8a8fb-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8a8fb-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8a8fb-117">defi</span><span class="sxs-lookup"><span data-stu-id="8a8fb-117">defi</span></span>                   |      | <span data-ttu-id="8a8fb-118">x</span><span class="sxs-lookup"><span data-stu-id="8a8fb-118">x</span></span>    | <span data-ttu-id="8a8fb-119">x</span><span class="sxs-lookup"><span data-stu-id="8a8fb-119">x</span></span>    | <span data-ttu-id="8a8fb-120">x</span><span class="sxs-lookup"><span data-stu-id="8a8fb-120">x</span></span>     | <span data-ttu-id="8a8fb-121">x</span><span class="sxs-lookup"><span data-stu-id="8a8fb-121">x</span></span>    | <span data-ttu-id="8a8fb-122">x</span><span class="sxs-lookup"><span data-stu-id="8a8fb-122">x</span></span>     |



 

<span data-ttu-id="8a8fb-123">L'istruzione defi definisce una costante di Integer shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-123">The defi instruction defines an integer shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="8a8fb-124">Sono denominate costanti immediate.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-124">These are called immediate constants.</span></span> <span data-ttu-id="8a8fb-125">Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetVertexShaderConstantI.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-125">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantI.</span></span>

<span data-ttu-id="8a8fb-126">Esistono due modi per impostare una costante Integer in uno shader.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-126">There are two ways to set an integer constant in a shader.</span></span>

1.  <span data-ttu-id="8a8fb-127">Usare defi per definire il vettore di costanti Integer direttamente all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-127">Use defi to define the integer constant vector directly inside a shader.</span></span>
2.  <span data-ttu-id="8a8fb-128">Usare i metodi API per impostare una costante.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-128">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="8a8fb-129">Usare [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) per impostare una costante Integer.</span><span class="sxs-lookup"><span data-stu-id="8a8fb-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a8fb-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a8fb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a8fb-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="8a8fb-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="8a8fb-132">def-vs</span><span class="sxs-lookup"><span data-stu-id="8a8fb-132">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="8a8fb-133">defb-vs</span><span class="sxs-lookup"><span data-stu-id="8a8fb-133">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 