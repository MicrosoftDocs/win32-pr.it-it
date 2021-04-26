---
description: Costanti di generazione normali delle mappe.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f76b6afe6eb68e8ddbc3ca28085861a518effc
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996328"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="22db3-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="22db3-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="22db3-104">Costanti di generazione normali delle mappe.</span><span class="sxs-lookup"><span data-stu-id="22db3-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="22db3-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="22db3-105">\#define</span></span>                            | <span data-ttu-id="22db3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22db3-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22db3-107">D3DX \_ NORMALMAP \_ MIRROR \_ U</span><span class="sxs-lookup"><span data-stu-id="22db3-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="22db3-108">Indica che i pixel al di fuori del bordo della trama sull'asse u devono essere speculari, senza eseguire il wrapping.</span><span class="sxs-lookup"><span data-stu-id="22db3-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="22db3-109">D3DX \_ NORMALMAP \_ MIRROR \_ V</span><span class="sxs-lookup"><span data-stu-id="22db3-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="22db3-110">Indica che è necessario eseguire il mirroring dei pixel al di fuori del bordo della trama sull'asse v, senza eseguire il wrapping.</span><span class="sxs-lookup"><span data-stu-id="22db3-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="22db3-111">D3DX \_ NORMALMAP \_ MIRROR</span><span class="sxs-lookup"><span data-stu-id="22db3-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="22db3-112">Come specificare D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.</span><span class="sxs-lookup"><span data-stu-id="22db3-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="22db3-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="22db3-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="22db3-114">Inverte la direzione di ogni normale.</span><span class="sxs-lookup"><span data-stu-id="22db3-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="22db3-115">OCCLUSIONE DI CALCOLO D3DX \_ NORMALMAP \_ \_</span><span class="sxs-lookup"><span data-stu-id="22db3-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="22db3-116">Calcola il termine di occlusione per pixel e lo codifica in alfa.</span><span class="sxs-lookup"><span data-stu-id="22db3-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="22db3-117">Un valore alfa 1 indica che il pixel non viene nascosto in alcun modo e un valore alfa 0 indica che il pixel è completamente nascosto.</span><span class="sxs-lookup"><span data-stu-id="22db3-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="22db3-118">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="22db3-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="22db3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22db3-119">Header</span></span>                   | <span data-ttu-id="22db3-120">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="22db3-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="22db3-121">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="22db3-121">Minimum operating system</span></span> | <span data-ttu-id="22db3-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="22db3-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="22db3-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22db3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22db3-124">Costanti D3DX</span><span class="sxs-lookup"><span data-stu-id="22db3-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="22db3-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="22db3-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



