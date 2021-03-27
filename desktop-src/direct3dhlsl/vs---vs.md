---
title: vs
description: Questa istruzione specifica il numero di versione dello shader. Questa istruzione funziona in tutte le versioni dello shader.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398292"
---
# <a name="vs"></a><span data-ttu-id="7eb61-104">vs</span><span class="sxs-lookup"><span data-stu-id="7eb61-104">vs</span></span>

<span data-ttu-id="7eb61-105">Questa istruzione specifica il numero di versione dello shader.</span><span class="sxs-lookup"><span data-stu-id="7eb61-105">This instruction specifies the shader version number.</span></span> <span data-ttu-id="7eb61-106">Questa istruzione funziona in tutte le versioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="7eb61-106">This instruction works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb61-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7eb61-107">Syntax</span></span>


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="7eb61-108">Argomenti di input</span><span class="sxs-lookup"><span data-stu-id="7eb61-108">Input Arguments</span></span>

<span data-ttu-id="7eb61-109">Gli argomenti di input contengono un singolo numero di versione principale con un numero di versione secondario singolo.</span><span class="sxs-lookup"><span data-stu-id="7eb61-109">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="7eb61-110">Le combinazioni consentite sono elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7eb61-110">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="7eb61-111">Versioni principali</span><span class="sxs-lookup"><span data-stu-id="7eb61-111">Main versions</span></span> | <span data-ttu-id="7eb61-112">Versioni secondarie</span><span class="sxs-lookup"><span data-stu-id="7eb61-112">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="7eb61-113">1</span><span class="sxs-lookup"><span data-stu-id="7eb61-113">1</span></span>             | <span data-ttu-id="7eb61-114">1</span><span class="sxs-lookup"><span data-stu-id="7eb61-114">1</span></span>                              |
| <span data-ttu-id="7eb61-115">2</span><span class="sxs-lookup"><span data-stu-id="7eb61-115">2</span></span>             | <span data-ttu-id="7eb61-116">0, SW (software), x (esteso)</span><span class="sxs-lookup"><span data-stu-id="7eb61-116">0, sw (software), x (extended)</span></span> |
| <span data-ttu-id="7eb61-117">3</span><span class="sxs-lookup"><span data-stu-id="7eb61-117">3</span></span>             | <span data-ttu-id="7eb61-118">0, SW (software)</span><span class="sxs-lookup"><span data-stu-id="7eb61-118">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="7eb61-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7eb61-119">Remarks</span></span>



| <span data-ttu-id="7eb61-120">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="7eb61-120">Vertex shader versions</span></span> | <span data-ttu-id="7eb61-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="7eb61-121">1\_1</span></span> | <span data-ttu-id="7eb61-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7eb61-122">2\_0</span></span> | <span data-ttu-id="7eb61-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7eb61-123">2\_x</span></span> | <span data-ttu-id="7eb61-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7eb61-124">2\_sw</span></span> | <span data-ttu-id="7eb61-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7eb61-125">3\_0</span></span> | <span data-ttu-id="7eb61-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7eb61-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="7eb61-127">vs</span><span class="sxs-lookup"><span data-stu-id="7eb61-127">vs</span></span>                     | <span data-ttu-id="7eb61-128">x</span><span class="sxs-lookup"><span data-stu-id="7eb61-128">x</span></span>    | <span data-ttu-id="7eb61-129">x</span><span class="sxs-lookup"><span data-stu-id="7eb61-129">x</span></span>    | <span data-ttu-id="7eb61-130">x</span><span class="sxs-lookup"><span data-stu-id="7eb61-130">x</span></span>    | <span data-ttu-id="7eb61-131">x</span><span class="sxs-lookup"><span data-stu-id="7eb61-131">x</span></span>     | <span data-ttu-id="7eb61-132">x</span><span class="sxs-lookup"><span data-stu-id="7eb61-132">x</span></span>    | <span data-ttu-id="7eb61-133">x</span><span class="sxs-lookup"><span data-stu-id="7eb61-133">x</span></span>     |



 

<span data-ttu-id="7eb61-134">Questa istruzione deve essere la prima istruzione non di commento in un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="7eb61-134">This instruction must be the first non-comment instruction in a vertex shader.</span></span>

<span data-ttu-id="7eb61-135">Questa istruzione è supportata in tutte le versioni di vertex shader.</span><span class="sxs-lookup"><span data-stu-id="7eb61-135">This instruction is supported in all vertex shader versions.</span></span>

<span data-ttu-id="7eb61-136">Le versioni con accelerazione hardware del software (versioni senza \_ SW nel numero di versione) possono elaborare i vertici con accelearation hardware o usare l'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="7eb61-136">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="7eb61-137">Le versioni del software (versioni con \_ SW nel numero di versione) elaborano i vertici solo con il software.</span><span class="sxs-lookup"><span data-stu-id="7eb61-137">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="7eb61-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="7eb61-138">Examples</span></span>

<span data-ttu-id="7eb61-139">Questo esempio parziale dichiara un vertex shader della versione 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="7eb61-139">This partial example declares a version 1\_1 vertex shader.</span></span>


```
vs_1_1
```



<span data-ttu-id="7eb61-140">Questo esempio parziale dichiara un vertex shader software della versione 2.</span><span class="sxs-lookup"><span data-stu-id="7eb61-140">This partial example declares a version 2 software vertex shader.</span></span>


```
vs_2_sw
```



## <a name="related-topics"></a><span data-ttu-id="7eb61-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7eb61-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eb61-142">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="7eb61-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




