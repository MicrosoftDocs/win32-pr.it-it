---
title: ps
description: Questa istruzione specifica il numero di versione dello shader e funziona in tutte le versioni dello shader.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993192"
---
# <a name="ps"></a><span data-ttu-id="c62cd-103">ps</span><span class="sxs-lookup"><span data-stu-id="c62cd-103">ps</span></span>

<span data-ttu-id="c62cd-104">Questa istruzione specifica il numero di versione dello shader e funziona in tutte le versioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="c62cd-104">This instruction specifies the shader version number and works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c62cd-105">Syntax</span></span>


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="c62cd-106">Argomenti di input</span><span class="sxs-lookup"><span data-stu-id="c62cd-106">Input Arguments</span></span>

<span data-ttu-id="c62cd-107">Gli argomenti di input contengono un singolo numero di versione principale con un numero di versione secondario singolo.</span><span class="sxs-lookup"><span data-stu-id="c62cd-107">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="c62cd-108">Le combinazioni consentite sono elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c62cd-108">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="c62cd-109">Versioni principali</span><span class="sxs-lookup"><span data-stu-id="c62cd-109">Main versions</span></span> | <span data-ttu-id="c62cd-110">Versioni secondarie</span><span class="sxs-lookup"><span data-stu-id="c62cd-110">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="c62cd-111">1</span><span class="sxs-lookup"><span data-stu-id="c62cd-111">1</span></span>             | <span data-ttu-id="c62cd-112">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="c62cd-112">1, 2, 3, 4</span></span>                     |
| <span data-ttu-id="c62cd-113">2</span><span class="sxs-lookup"><span data-stu-id="c62cd-113">2</span></span>             | <span data-ttu-id="c62cd-114">0, x (esteso), SW (software)</span><span class="sxs-lookup"><span data-stu-id="c62cd-114">0, x (extended), sw (software)</span></span> |
| <span data-ttu-id="c62cd-115">3</span><span class="sxs-lookup"><span data-stu-id="c62cd-115">3</span></span>             | <span data-ttu-id="c62cd-116">0, SW (software)</span><span class="sxs-lookup"><span data-stu-id="c62cd-116">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="c62cd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c62cd-117">Remarks</span></span>



| <span data-ttu-id="c62cd-118">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="c62cd-118">Pixel shader versions</span></span> | <span data-ttu-id="c62cd-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="c62cd-119">1\_1</span></span> | <span data-ttu-id="c62cd-120">1\_2</span><span class="sxs-lookup"><span data-stu-id="c62cd-120">1\_2</span></span> | <span data-ttu-id="c62cd-121">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c62cd-121">1\_3</span></span> | <span data-ttu-id="c62cd-122">1\_4</span><span class="sxs-lookup"><span data-stu-id="c62cd-122">1\_4</span></span> | <span data-ttu-id="c62cd-123">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c62cd-123">2\_0</span></span> | <span data-ttu-id="c62cd-124">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c62cd-124">2\_x</span></span> | <span data-ttu-id="c62cd-125">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c62cd-125">2\_sw</span></span> | <span data-ttu-id="c62cd-126">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c62cd-126">3\_0</span></span> | <span data-ttu-id="c62cd-127">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c62cd-127">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c62cd-128">ps</span><span class="sxs-lookup"><span data-stu-id="c62cd-128">ps</span></span>                    | <span data-ttu-id="c62cd-129">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-129">x</span></span>    | <span data-ttu-id="c62cd-130">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-130">x</span></span>    | <span data-ttu-id="c62cd-131">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-131">x</span></span>    | <span data-ttu-id="c62cd-132">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-132">x</span></span>    | <span data-ttu-id="c62cd-133">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-133">x</span></span>    | <span data-ttu-id="c62cd-134">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-134">x</span></span>    | <span data-ttu-id="c62cd-135">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-135">x</span></span>     | <span data-ttu-id="c62cd-136">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-136">x</span></span>    | <span data-ttu-id="c62cd-137">x</span><span class="sxs-lookup"><span data-stu-id="c62cd-137">x</span></span>     |



 

<span data-ttu-id="c62cd-138">Questa istruzione deve essere la prima istruzione non di commento in una pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c62cd-138">This instruction must be the first non-comment instruction in a pixel shader.</span></span>

<span data-ttu-id="c62cd-139">Le versioni con accelerazione hardware del software (versioni senza \_ SW nel numero di versione) possono elaborare i vertici con accelearation hardware o usare l'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="c62cd-139">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="c62cd-140">Le versioni del software (versioni con \_ SW nel numero di versione) elaborano i vertici solo con il software.</span><span class="sxs-lookup"><span data-stu-id="c62cd-140">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="c62cd-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="c62cd-141">Examples</span></span>

<span data-ttu-id="c62cd-142">In questo esempio parziale viene dichiarata una versione 1 \_ 1 pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c62cd-142">This partial example declares a version 1\_1 pixel shader.</span></span>


```
ps_1_1
```



<span data-ttu-id="c62cd-143">Questo esempio parziale dichiara una versione 1 \_ 4 pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c62cd-143">This partial example declares a version 1\_4 pixel shader.</span></span>


```
ps_1_4
```



## <a name="related-topics"></a><span data-ttu-id="c62cd-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c62cd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c62cd-145">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="c62cd-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




