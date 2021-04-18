---
description: Costanti di generazione di mappe normali.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37985456e81b20af9b3e4396d10045d5e58c9b7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303850"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="ca27e-103">\_Normalmap D3DX</span><span class="sxs-lookup"><span data-stu-id="ca27e-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="ca27e-104">Costanti di generazione di mappe normali.</span><span class="sxs-lookup"><span data-stu-id="ca27e-104">Normal maps generation constants.</span></span>



|                                     |                                                                                                                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca27e-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="ca27e-105">\#define</span></span>                            | <span data-ttu-id="ca27e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca27e-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="ca27e-107">D3DX \_ normalmap \_ mirror \_ U</span><span class="sxs-lookup"><span data-stu-id="ca27e-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="ca27e-108">Indica che i pixel al di fuori del bordo della trama sull'asse u devono essere speculari, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="ca27e-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="ca27e-109">D3DX \_ normalmap \_ mirror \_ V</span><span class="sxs-lookup"><span data-stu-id="ca27e-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="ca27e-110">Indica che i pixel al di fuori del bordo della trama sull'asse v devono essere speculari, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="ca27e-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="ca27e-111">\_Mirror normalmap \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="ca27e-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="ca27e-112">Come specificare D3DX \_ normalmap \_ mirror \_ U \| D3DX \_ normalmap \_ mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="ca27e-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="ca27e-113">D3DX \_ normalmap \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="ca27e-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="ca27e-114">Inverte la direzione di ogni normale.</span><span class="sxs-lookup"><span data-stu-id="ca27e-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="ca27e-115">\_ \_ Occlusione di calcolo normalmap D3DX \_</span><span class="sxs-lookup"><span data-stu-id="ca27e-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="ca27e-116">Calcola il termine di occlusione per pixel e lo codifica in alfa.</span><span class="sxs-lookup"><span data-stu-id="ca27e-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="ca27e-117">Un valore alfa pari a 1 indica che il pixel non è nascosto in alcun modo, mentre un valore alfa pari a 0 indica che il pixel è completamente nascosto.</span><span class="sxs-lookup"><span data-stu-id="ca27e-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="ca27e-118">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="ca27e-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="ca27e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca27e-119">Header</span></span>                   | <span data-ttu-id="ca27e-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="ca27e-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="ca27e-121">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="ca27e-121">Minimum operating system</span></span> | <span data-ttu-id="ca27e-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ca27e-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ca27e-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca27e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca27e-124">Costanti D3DX</span><span class="sxs-lookup"><span data-stu-id="ca27e-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="ca27e-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="ca27e-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



