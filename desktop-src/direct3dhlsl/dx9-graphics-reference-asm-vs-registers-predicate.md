---
title: Registro predicato (HLSL VS Reference)
description: Questo registro di output del vertex shader contiene un valore booleano per canale.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104046136"
---
# <a name="predicate-register-hlsl-vs-reference"></a><span data-ttu-id="ff28d-103">Registro predicato (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="ff28d-103">Predicate Register (HLSL VS reference)</span></span>

<span data-ttu-id="ff28d-104">Questo registro di output del vertex shader contiene un valore booleano per canale.</span><span class="sxs-lookup"><span data-stu-id="ff28d-104">This vertex shader output register contains a per-channel Boolean value.</span></span>

<span data-ttu-id="ff28d-105">Un registro predicato è supportato dalle versioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ff28d-105">A predicate register is supported by the following versions.</span></span>



| <span data-ttu-id="ff28d-106">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="ff28d-106">Vertex shader versions</span></span> | <span data-ttu-id="ff28d-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="ff28d-107">1\_1</span></span> | <span data-ttu-id="ff28d-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff28d-108">2\_0</span></span> | <span data-ttu-id="ff28d-109">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ff28d-109">2\_sw</span></span> | <span data-ttu-id="ff28d-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ff28d-110">2\_x</span></span> | <span data-ttu-id="ff28d-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff28d-111">3\_0</span></span> | <span data-ttu-id="ff28d-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ff28d-112">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="ff28d-113">registro predicato</span><span class="sxs-lookup"><span data-stu-id="ff28d-113">predicate register</span></span>     |      |      |       | <span data-ttu-id="ff28d-114">x</span><span class="sxs-lookup"><span data-stu-id="ff28d-114">x</span></span>    | <span data-ttu-id="ff28d-115">x</span><span class="sxs-lookup"><span data-stu-id="ff28d-115">x</span></span>    | <span data-ttu-id="ff28d-116">x</span><span class="sxs-lookup"><span data-stu-id="ff28d-116">x</span></span>     |



 

<span data-ttu-id="ff28d-117">Di seguito sono riportate le proprietà Register.</span><span class="sxs-lookup"><span data-stu-id="ff28d-117">Here are the register properties.</span></span>



| <span data-ttu-id="ff28d-118">Tipo di registro</span><span class="sxs-lookup"><span data-stu-id="ff28d-118">Register type</span></span> | <span data-ttu-id="ff28d-119">Conteggio</span><span class="sxs-lookup"><span data-stu-id="ff28d-119">Count</span></span> | <span data-ttu-id="ff28d-120">L/S</span><span class="sxs-lookup"><span data-stu-id="ff28d-120">R/W</span></span> | <span data-ttu-id="ff28d-121">\# Leggere le porte</span><span class="sxs-lookup"><span data-stu-id="ff28d-121">\# Read ports</span></span> | <span data-ttu-id="ff28d-122">\# Letture/Inst</span><span class="sxs-lookup"><span data-stu-id="ff28d-122">\# Reads/inst</span></span> | <span data-ttu-id="ff28d-123">Dimension</span><span class="sxs-lookup"><span data-stu-id="ff28d-123">Dimension</span></span> | <span data-ttu-id="ff28d-124">Relannr</span><span class="sxs-lookup"><span data-stu-id="ff28d-124">RelAddr</span></span> | <span data-ttu-id="ff28d-125">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="ff28d-125">Defaults</span></span> | <span data-ttu-id="ff28d-126">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="ff28d-126">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="ff28d-127">Predicato (p)</span><span class="sxs-lookup"><span data-stu-id="ff28d-127">Predicate(p)</span></span>  | <span data-ttu-id="ff28d-128">1</span><span class="sxs-lookup"><span data-stu-id="ff28d-128">1</span></span>     | <span data-ttu-id="ff28d-129">L/S</span><span class="sxs-lookup"><span data-stu-id="ff28d-129">R/W</span></span> | <span data-ttu-id="ff28d-130">1</span><span class="sxs-lookup"><span data-stu-id="ff28d-130">1</span></span>             | <span data-ttu-id="ff28d-131">1</span><span class="sxs-lookup"><span data-stu-id="ff28d-131">1</span></span>             | <span data-ttu-id="ff28d-132">4</span><span class="sxs-lookup"><span data-stu-id="ff28d-132">4</span></span>         | <span data-ttu-id="ff28d-133">N/D</span><span class="sxs-lookup"><span data-stu-id="ff28d-133">N/A</span></span>     | <span data-ttu-id="ff28d-134">nessuno</span><span class="sxs-lookup"><span data-stu-id="ff28d-134">None</span></span>     | <span data-ttu-id="ff28d-135">N</span><span class="sxs-lookup"><span data-stu-id="ff28d-135">N</span></span>            |



 

<span data-ttu-id="ff28d-136">Il registro del predicato può essere modificato con [setp \_ comp-vs](setp-comp---vs.md). Non sono disponibili valori predefiniti per questo registro, un'applicazione deve impostare il registro prima che venga usato.</span><span class="sxs-lookup"><span data-stu-id="ff28d-136">The predicate register can be modified with [setp\_comp - vs](setp-comp---vs.md). There are no default values for this register, an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff28d-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff28d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff28d-138">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="ff28d-138">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




