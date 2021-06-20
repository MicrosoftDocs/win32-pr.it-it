---
title: Registro contatori del ciclo (informazioni di riferimento su HLSL PS)
description: Informazioni sul registro dei contatori del ciclo per i pixel shader. L'unico registro in questa banca è il registro corrente del contatore del ciclo (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405514"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="4184d-104">Registro contatori del ciclo (informazioni di riferimento su HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="4184d-104">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="4184d-105">L'unico registro in questa banca è il registro corrente del contatore del ciclo (aL).</span><span class="sxs-lookup"><span data-stu-id="4184d-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="4184d-106">Viene incrementato automaticamente in ogni esecuzione del [ciclo ps](loop---ps.md) / [endloop - blocco ps.](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4184d-106">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="4184d-107">Può quindi essere usato nel blocco per l'indirizzamento relativo, se necessario, e non è valido per usarlo all'esterno del ciclo.</span><span class="sxs-lookup"><span data-stu-id="4184d-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="4184d-108">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="4184d-108">Pixel shader versions</span></span> | <span data-ttu-id="4184d-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="4184d-109">1\_1</span></span> | <span data-ttu-id="4184d-110">1\_2</span><span class="sxs-lookup"><span data-stu-id="4184d-110">1\_2</span></span> | <span data-ttu-id="4184d-111">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4184d-111">1\_3</span></span> | <span data-ttu-id="4184d-112">1\_4</span><span class="sxs-lookup"><span data-stu-id="4184d-112">1\_4</span></span> | <span data-ttu-id="4184d-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4184d-113">2\_0</span></span> | <span data-ttu-id="4184d-114">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4184d-114">2\_sw</span></span> | <span data-ttu-id="4184d-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4184d-115">2\_x</span></span> | <span data-ttu-id="4184d-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4184d-116">3\_0</span></span> | <span data-ttu-id="4184d-117">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4184d-117">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="4184d-118">Registro contatori cicli</span><span class="sxs-lookup"><span data-stu-id="4184d-118">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="4184d-119">x</span><span class="sxs-lookup"><span data-stu-id="4184d-119">x</span></span>    | <span data-ttu-id="4184d-120">x</span><span class="sxs-lookup"><span data-stu-id="4184d-120">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4184d-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4184d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4184d-122">Registri</span><span class="sxs-lookup"><span data-stu-id="4184d-122">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




