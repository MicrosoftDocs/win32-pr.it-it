---
title: Registro del contatore di cicli (informazioni di riferimento su HLSL PS)
description: L'unico registro in questa banca è il registro del contatore di cicli corrente (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719540"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="10ac8-103">Registro del contatore di cicli (informazioni di riferimento su HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="10ac8-103">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="10ac8-104">L'unico registro in questa banca è il registro del contatore di cicli corrente (aL).</span><span class="sxs-lookup"><span data-stu-id="10ac8-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="10ac8-105">Viene incrementato automaticamente in ogni esecuzione del blocco [loop-PS](loop---ps.md) / [EndLoop-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="10ac8-105">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="10ac8-106">Pertanto, può essere utilizzato nel blocco per l'indirizzamento relativo, se necessario, e non è valido per utilizzarlo all'esterno del ciclo.</span><span class="sxs-lookup"><span data-stu-id="10ac8-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="10ac8-107">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="10ac8-107">Pixel shader versions</span></span> | <span data-ttu-id="10ac8-108">1\_1</span><span class="sxs-lookup"><span data-stu-id="10ac8-108">1\_1</span></span> | <span data-ttu-id="10ac8-109">1\_2</span><span class="sxs-lookup"><span data-stu-id="10ac8-109">1\_2</span></span> | <span data-ttu-id="10ac8-110">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="10ac8-110">1\_3</span></span> | <span data-ttu-id="10ac8-111">1\_4</span><span class="sxs-lookup"><span data-stu-id="10ac8-111">1\_4</span></span> | <span data-ttu-id="10ac8-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10ac8-112">2\_0</span></span> | <span data-ttu-id="10ac8-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="10ac8-113">2\_sw</span></span> | <span data-ttu-id="10ac8-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="10ac8-114">2\_x</span></span> | <span data-ttu-id="10ac8-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10ac8-115">3\_0</span></span> | <span data-ttu-id="10ac8-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="10ac8-116">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="10ac8-117">Registro contatore cicli</span><span class="sxs-lookup"><span data-stu-id="10ac8-117">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="10ac8-118">x</span><span class="sxs-lookup"><span data-stu-id="10ac8-118">x</span></span>    | <span data-ttu-id="10ac8-119">x</span><span class="sxs-lookup"><span data-stu-id="10ac8-119">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="10ac8-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10ac8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10ac8-121">Registri</span><span class="sxs-lookup"><span data-stu-id="10ac8-121">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




