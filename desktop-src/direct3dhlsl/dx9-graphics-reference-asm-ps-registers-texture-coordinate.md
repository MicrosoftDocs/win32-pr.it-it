---
title: Registro delle coordinate di trama (riferimenti per HLSL PS)
description: Registro di input del pixel shader contenente coordinate di trama.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104976511"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a><span data-ttu-id="2280f-103">Registro delle coordinate di trama (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="2280f-103">Texture coordinate register (HLSL PS reference)</span></span>

<span data-ttu-id="2280f-104">Registro di input del pixel shader contenente coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2280f-104">Pixel shader input register containing texture coordinates.</span></span>



| <span data-ttu-id="2280f-105">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="2280f-105">Pixel shader versions</span></span>       | <span data-ttu-id="2280f-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="2280f-106">1\_1</span></span> | <span data-ttu-id="2280f-107">1\_2</span><span class="sxs-lookup"><span data-stu-id="2280f-107">1\_2</span></span> | <span data-ttu-id="2280f-108">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2280f-108">1\_3</span></span> | <span data-ttu-id="2280f-109">1\_4</span><span class="sxs-lookup"><span data-stu-id="2280f-109">1\_4</span></span> | <span data-ttu-id="2280f-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2280f-110">2\_0</span></span> | <span data-ttu-id="2280f-111">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2280f-111">2\_sw</span></span> | <span data-ttu-id="2280f-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2280f-112">2\_x</span></span> | <span data-ttu-id="2280f-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2280f-113">3\_0</span></span> | <span data-ttu-id="2280f-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2280f-114">3\_sw</span></span> |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="2280f-115">Registro coordinate trama</span><span class="sxs-lookup"><span data-stu-id="2280f-115">Texture Coordinate Register</span></span> |      |      |      |      | <span data-ttu-id="2280f-116">x</span><span class="sxs-lookup"><span data-stu-id="2280f-116">x</span></span>    | <span data-ttu-id="2280f-117">x</span><span class="sxs-lookup"><span data-stu-id="2280f-117">x</span></span>     | <span data-ttu-id="2280f-118">x</span><span class="sxs-lookup"><span data-stu-id="2280f-118">x</span></span>    | <span data-ttu-id="2280f-119">x</span><span class="sxs-lookup"><span data-stu-id="2280f-119">x</span></span>    | <span data-ttu-id="2280f-120">x</span><span class="sxs-lookup"><span data-stu-id="2280f-120">x</span></span>     |



 

<span data-ttu-id="2280f-121">Un registro delle coordinate di trama contiene dati delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2280f-121">A texture coordinate register contains texture coordinate data.</span></span> <span data-ttu-id="2280f-122">Prima di utilizzare un registro delle coordinate di trama, è necessario dichiararlo tramite una dichiarazione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="2280f-122">Before a texture coordinate register is used, it must be declared by a pixel shader declaration.</span></span> <span data-ttu-id="2280f-123">Per informazioni dettagliate su come dichiarare un registro di trama, vedere [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="2280f-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span></span>

<span data-ttu-id="2280f-124">Inoltre, di seguito sono riportate alcune altre proprietà dei registri delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2280f-124">In addition, here are some other properties of texture coordinate registers.</span></span>

-   <span data-ttu-id="2280f-125">Sono presenti otto registri delle coordinate di trama di pixel shader, da T0 a T7.</span><span class="sxs-lookup"><span data-stu-id="2280f-125">There are eight pixel-shader texture coordinate registers, t0 to t7.</span></span>
-   <span data-ttu-id="2280f-126">Si tratta di registri di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2280f-126">These are read-only registers.</span></span>
-   <span data-ttu-id="2280f-127">Contengono valori RGBA a quattro componenti iterati dai vertici di input.</span><span class="sxs-lookup"><span data-stu-id="2280f-127">They contain four-component RGBA values iterated from input vertices.</span></span>
-   <span data-ttu-id="2280f-128">Contengono valori di dati ad alta precisione e di intervallo dinamico elevati interpolati dai dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2280f-128">They contain high precision, high dynamic range data values interpolated from the vertex data.</span></span> <span data-ttu-id="2280f-129">I valori vengono generati con l'interpolazione corretta della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="2280f-129">Values are generated with perspective-correct interpolation.</span></span> <span data-ttu-id="2280f-130">I dati sono di precisione a virgola mobile e sono firmati.</span><span class="sxs-lookup"><span data-stu-id="2280f-130">Data is floating-point precision, and is signed.</span></span>
-   <span data-ttu-id="2280f-131">È presente un massimo di uno in un'unica istruzione.</span><span class="sxs-lookup"><span data-stu-id="2280f-131">There is a maximum of one in a single instruction.</span></span>
-   <span data-ttu-id="2280f-132">Più letture di un registro delle coordinate di trama in uno shader devono usare una [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)identica.</span><span class="sxs-lookup"><span data-stu-id="2280f-132">Multiple reads of a texture coordinate register within a shader must use identical [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="2280f-133">Il modificatore di precisione parziale facoltativo \[ \_ PP \] si applica alle letture dipendenti.</span><span class="sxs-lookup"><span data-stu-id="2280f-133">The optional partial precision modifier \[\_pp\] applies to dependent reads.</span></span> <span data-ttu-id="2280f-134">Questo perché la precisione parziale influiscono sulle operazioni aritmetiche che coinvolgono il registro delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2280f-134">This is because partial precision affects arithmetic operations involving the texture coordinate register.</span></span> <span data-ttu-id="2280f-135">Non influirà sulla precisione delle istruzioni per gli indirizzi di trama perché non influisce sugli iteratori delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2280f-135">It will not affect the precision of texture address instructions because it does not affect the texture coordinate iterators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2280f-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2280f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2280f-137">Registri</span><span class="sxs-lookup"><span data-stu-id="2280f-137">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




