---
title: Registro temporaneo (riferimenti per HLSL PS)
description: I registri temporanei di input pixel shader vengono usati per mantenere i risultati intermedi.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857830"
---
# <a name="temporary-register-hlsl-ps-reference"></a><span data-ttu-id="b41f1-103">Registro temporaneo (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="b41f1-103">Temporary register (HLSL PS reference)</span></span>

<span data-ttu-id="b41f1-104">I registri temporanei di input pixel shader vengono usati per mantenere i risultati intermedi.</span><span class="sxs-lookup"><span data-stu-id="b41f1-104">Pixel shader input temporary registers are used to hold intermediate results.</span></span>

<span data-ttu-id="b41f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b41f1-105">Syntax</span></span>


```
no declaration is required
```





| <span data-ttu-id="b41f1-106">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="b41f1-106">Pixel shader versions</span></span> | <span data-ttu-id="b41f1-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="b41f1-107">1\_1</span></span> | <span data-ttu-id="b41f1-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="b41f1-108">1\_2</span></span> | <span data-ttu-id="b41f1-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b41f1-109">1\_3</span></span> | <span data-ttu-id="b41f1-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="b41f1-110">1\_4</span></span> | <span data-ttu-id="b41f1-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b41f1-111">2\_0</span></span> | <span data-ttu-id="b41f1-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b41f1-112">2\_sw</span></span> | <span data-ttu-id="b41f1-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b41f1-113">2\_x</span></span> | <span data-ttu-id="b41f1-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b41f1-114">3\_0</span></span> | <span data-ttu-id="b41f1-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b41f1-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="b41f1-116">Registro temporaneo</span><span class="sxs-lookup"><span data-stu-id="b41f1-116">Temporary Register</span></span>    |      |      |      |      | <span data-ttu-id="b41f1-117">x</span><span class="sxs-lookup"><span data-stu-id="b41f1-117">x</span></span>    | <span data-ttu-id="b41f1-118">x</span><span class="sxs-lookup"><span data-stu-id="b41f1-118">x</span></span>     | <span data-ttu-id="b41f1-119">x</span><span class="sxs-lookup"><span data-stu-id="b41f1-119">x</span></span>    | <span data-ttu-id="b41f1-120">x</span><span class="sxs-lookup"><span data-stu-id="b41f1-120">x</span></span>    | <span data-ttu-id="b41f1-121">x</span><span class="sxs-lookup"><span data-stu-id="b41f1-121">x</span></span>     |



 

-   <span data-ttu-id="b41f1-122">Sono presenti 12 registri temporanei di pixel shader: da R0 a R11.</span><span class="sxs-lookup"><span data-stu-id="b41f1-122">There are 12 pixel-shader temporary registers: r0 to r11.</span></span>
-   <span data-ttu-id="b41f1-123">Questi registri vengono usati per archiviare i risultati intermedi durante i calcoli.</span><span class="sxs-lookup"><span data-stu-id="b41f1-123">These registers are used for storing intermediate results during computations.</span></span>
-   <span data-ttu-id="b41f1-124">Se un registro temporaneo usa componenti non definiti nel codice precedente, la convalida dello shader avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b41f1-124">If a temporary register uses components that are not defined in previous code, shader validation will fail.</span></span>
-   <span data-ttu-id="b41f1-125">Si tratta almeno di precisione a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b41f1-125">These are at least floating-point precision.</span></span>
-   <span data-ttu-id="b41f1-126">In una singola istruzione è possibile utilizzare un massimo di tre.</span><span class="sxs-lookup"><span data-stu-id="b41f1-126">A maximum of three can be used in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b41f1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b41f1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b41f1-128">Registri</span><span class="sxs-lookup"><span data-stu-id="b41f1-128">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




