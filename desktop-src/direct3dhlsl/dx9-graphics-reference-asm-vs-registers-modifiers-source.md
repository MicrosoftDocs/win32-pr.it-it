---
title: Modificatori del registro di origine vertex shader
description: I modificatori di origine possono essere applicati per modificare i dati letti da un registro di origine prima che i dati vengano utilizzati dall'istruzione.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396403"
---
# <a name="vertex-shader-source-register-modifiers"></a><span data-ttu-id="8f71a-103">Modificatori del registro di origine vertex shader</span><span class="sxs-lookup"><span data-stu-id="8f71a-103">Vertex Shader Source Register Modifiers</span></span>

<span data-ttu-id="8f71a-104">I modificatori di origine possono essere applicati per modificare i dati letti da un registro di origine prima che i dati vengano utilizzati dall'istruzione.</span><span class="sxs-lookup"><span data-stu-id="8f71a-104">Source modifiers can be applied to modify the data read from a source register before the data is used by the instruction.</span></span>

## <a name="negate"></a><span data-ttu-id="8f71a-105">Negate</span><span class="sxs-lookup"><span data-stu-id="8f71a-105">Negate</span></span>

<span data-ttu-id="8f71a-106">Negare il contenuto del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="8f71a-106">Negate the contents of the source register.</span></span>



| <span data-ttu-id="8f71a-107">Modificatore Component</span><span class="sxs-lookup"><span data-stu-id="8f71a-107">Component modifier</span></span> | <span data-ttu-id="8f71a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f71a-108">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="8f71a-109">\- r</span><span class="sxs-lookup"><span data-stu-id="8f71a-109">\- r</span></span>               | <span data-ttu-id="8f71a-110">Negazione origine</span><span class="sxs-lookup"><span data-stu-id="8f71a-110">Source negation</span></span> |



 

<span data-ttu-id="8f71a-111">Non è possibile usare il modificatore negazioni nel secondo registro di origine di queste istruzioni: [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4x4-vs](m4x4---vs.md).</span><span class="sxs-lookup"><span data-stu-id="8f71a-111">The negate modifier cannot be used on second source register of these instructions: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).</span></span>



| <span data-ttu-id="8f71a-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="8f71a-112">Vertex shader versions</span></span> | <span data-ttu-id="8f71a-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="8f71a-113">1\_1</span></span> | <span data-ttu-id="8f71a-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8f71a-114">2\_0</span></span> | <span data-ttu-id="8f71a-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8f71a-115">2\_x</span></span> | <span data-ttu-id="8f71a-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8f71a-116">2\_sw</span></span> | <span data-ttu-id="8f71a-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8f71a-117">3\_0</span></span> | <span data-ttu-id="8f71a-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8f71a-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| \-                     | <span data-ttu-id="8f71a-119">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-119">x</span></span>    | <span data-ttu-id="8f71a-120">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-120">x</span></span>    | <span data-ttu-id="8f71a-121">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-121">x</span></span>    | <span data-ttu-id="8f71a-122">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-122">x</span></span>     | <span data-ttu-id="8f71a-123">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-123">x</span></span>    | <span data-ttu-id="8f71a-124">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-124">x</span></span>     |



 

## <a name="absolute-value"></a><span data-ttu-id="8f71a-125">Valore assoluto</span><span class="sxs-lookup"><span data-stu-id="8f71a-125">Absolute Value</span></span>

<span data-ttu-id="8f71a-126">Assumere il valore assoluto del registro.</span><span class="sxs-lookup"><span data-stu-id="8f71a-126">Take the absolute value of the register.</span></span>



| <span data-ttu-id="8f71a-127">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="8f71a-127">Vertex shader versions</span></span> | <span data-ttu-id="8f71a-128">1\_1</span><span class="sxs-lookup"><span data-stu-id="8f71a-128">1\_1</span></span> | <span data-ttu-id="8f71a-129">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8f71a-129">2\_0</span></span> | <span data-ttu-id="8f71a-130">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8f71a-130">2\_x</span></span> | <span data-ttu-id="8f71a-131">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8f71a-131">2\_sw</span></span> | <span data-ttu-id="8f71a-132">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8f71a-132">3\_0</span></span> | <span data-ttu-id="8f71a-133">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8f71a-133">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8f71a-134">abs</span><span class="sxs-lookup"><span data-stu-id="8f71a-134">abs</span></span>                    |      |      |      |       | <span data-ttu-id="8f71a-135">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-135">x</span></span>    | <span data-ttu-id="8f71a-136">x</span><span class="sxs-lookup"><span data-stu-id="8f71a-136">x</span></span>     |



 

<span data-ttu-id="8f71a-137">Se una versione 3 dello shader legge da uno o più registri float costanti (c \# ), uno dei seguenti deve essere true.</span><span class="sxs-lookup"><span data-stu-id="8f71a-137">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="8f71a-138">Tutti i registri a virgola mobile costanti devono usare il modificatore ABS.</span><span class="sxs-lookup"><span data-stu-id="8f71a-138">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="8f71a-139">Nessun registro a virgola mobile costante può utilizzare il modificatore ABS.</span><span class="sxs-lookup"><span data-stu-id="8f71a-139">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f71a-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f71a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f71a-141">Modificatori del registro vertex shader</span><span class="sxs-lookup"><span data-stu-id="8f71a-141">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




