---
title: hs_decls (SM5-ASM)
description: Avviare la fase delle dichiarazioni in uno scafo dello shader.
ms.assetid: 1C8552B1-F649-4B73-A365-D449A9121DAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e57207e35aab507a1404efaf90131a9648918ae7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117217"
---
# <a name="hs_decls-sm5---asm"></a><span data-ttu-id="231fb-103">HS \_ decls (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="231fb-103">hs\_decls (sm5 - asm)</span></span>

<span data-ttu-id="231fb-104">Avviare la fase delle dichiarazioni in uno scafo dello shader.</span><span class="sxs-lookup"><span data-stu-id="231fb-104">Start the declarations phase in a hull shader.</span></span>



| <span data-ttu-id="231fb-105">\_decls HS</span><span class="sxs-lookup"><span data-stu-id="231fb-105">hs\_decls</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="231fb-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="231fb-106">Remarks</span></span>

<span data-ttu-id="231fb-107">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="231fb-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="231fb-108">Vertice</span><span class="sxs-lookup"><span data-stu-id="231fb-108">Vertex</span></span> | <span data-ttu-id="231fb-109">Hull</span><span class="sxs-lookup"><span data-stu-id="231fb-109">Hull</span></span> | <span data-ttu-id="231fb-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="231fb-110">Domain</span></span> | <span data-ttu-id="231fb-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="231fb-111">Geometry</span></span> | <span data-ttu-id="231fb-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="231fb-112">Pixel</span></span> | <span data-ttu-id="231fb-113">Calcolo</span><span class="sxs-lookup"><span data-stu-id="231fb-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="231fb-114">X</span><span class="sxs-lookup"><span data-stu-id="231fb-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="231fb-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="231fb-115">Minimum Shader Model</span></span>

<span data-ttu-id="231fb-116">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="231fb-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="231fb-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="231fb-117">Shader Model</span></span>                                              | <span data-ttu-id="231fb-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="231fb-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="231fb-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="231fb-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="231fb-120">sì</span><span class="sxs-lookup"><span data-stu-id="231fb-120">yes</span></span>       |
| [<span data-ttu-id="231fb-121">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="231fb-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="231fb-122">no</span><span class="sxs-lookup"><span data-stu-id="231fb-122">no</span></span>        |
| [<span data-ttu-id="231fb-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="231fb-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="231fb-124">no</span><span class="sxs-lookup"><span data-stu-id="231fb-124">no</span></span>        |
| [<span data-ttu-id="231fb-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="231fb-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="231fb-126">no</span><span class="sxs-lookup"><span data-stu-id="231fb-126">no</span></span>        |
| [<span data-ttu-id="231fb-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="231fb-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="231fb-128">no</span><span class="sxs-lookup"><span data-stu-id="231fb-128">no</span></span>        |
| [<span data-ttu-id="231fb-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="231fb-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="231fb-130">no</span><span class="sxs-lookup"><span data-stu-id="231fb-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="231fb-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="231fb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="231fb-132">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="231fb-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




