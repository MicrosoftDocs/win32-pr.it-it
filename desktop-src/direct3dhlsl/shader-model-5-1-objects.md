---
title: Oggetti modello shader 5,1
description: Al modello di shader 5,1 sono stati aggiunti gli oggetti seguenti.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616afd8e4036988b6f91cb09cddf0db26c1dd480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338062"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="7ffad-103">Oggetti modello shader 5,1</span><span class="sxs-lookup"><span data-stu-id="7ffad-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="7ffad-104">Al modello di shader 5,1 sono stati aggiunti gli oggetti seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ffad-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="7ffad-105">Per le [visualizzazioni degli ordini di rasterizzazione](/windows/desktop/direct3d11/rasterizer-order-views) (disponibili in D3D 11.3 e D3D12), gli oggetti seguenti sono nuovi e sono consentiti solo nella pixel shader.</span><span class="sxs-lookup"><span data-stu-id="7ffad-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="7ffad-106">Si noti che i metodi supportati sono identici agli oggetti UAV corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="7ffad-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7ffad-107">Oggetto rasterizzatore</span><span class="sxs-lookup"><span data-stu-id="7ffad-107">Rasterizer Object</span></span>                  | <span data-ttu-id="7ffad-108">UAV (oggetto)</span><span class="sxs-lookup"><span data-stu-id="7ffad-108">UAV Object</span></span>                                                    |
| <span data-ttu-id="7ffad-109">RasterizerOrderedBuffer</span><span class="sxs-lookup"><span data-stu-id="7ffad-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="7ffad-110">**RWBuffer**</span><span class="sxs-lookup"><span data-stu-id="7ffad-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="7ffad-111">RasterizerOrderedByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="7ffad-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="7ffad-112">**RWByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="7ffad-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="7ffad-113">RasterizerOrderedStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="7ffad-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="7ffad-114">**RWStructuredBuffer**</span><span class="sxs-lookup"><span data-stu-id="7ffad-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="7ffad-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="7ffad-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="7ffad-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="7ffad-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="7ffad-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="7ffad-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="7ffad-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="7ffad-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="7ffad-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="7ffad-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="7ffad-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="7ffad-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="7ffad-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="7ffad-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="7ffad-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="7ffad-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="7ffad-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="7ffad-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="7ffad-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="7ffad-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="7ffad-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ffad-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ffad-126">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="7ffad-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="7ffad-127">Funzionalità del modello HLSL shader 5,1 per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7ffad-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 