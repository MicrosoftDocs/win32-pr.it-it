---
description: Enumerazione utilizzata per indicare il motivo per cui un pixel è stato rifiutato.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341821"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span data-ttu-id="b9efe-103"><span id="vspixengine.pixelkillreason"></span>Enumerazione PIXELKILLREASON</span><span class="sxs-lookup"><span data-stu-id="b9efe-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON enumeration</span></span>

<span data-ttu-id="b9efe-104">Enumerazione utilizzata per indicare il motivo per cui un pixel è stato rifiutato.</span><span class="sxs-lookup"><span data-stu-id="b9efe-104">An enum used to indicate why a pixel was rejected.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9efe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9efe-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="b9efe-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b9efe-106">Constants</span></span>

<span data-ttu-id="b9efe-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ None**</span><span class="sxs-lookup"><span data-stu-id="b9efe-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR\_NONE**</span></span>  
<span data-ttu-id="b9efe-108">Valore che indica che il pixel non è stato rifiutato.</span><span class="sxs-lookup"><span data-stu-id="b9efe-108">A value that indicates that the pixel was not rejected.</span></span>

<span data-ttu-id="b9efe-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**\_SHADERKILL PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR\_SHADERKILL**</span></span>  
<span data-ttu-id="b9efe-110">Valore che indica che il pixel è stato rifiutato perché lo shader non è stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9efe-110">A value that indicates that the pixel was rejected because the shader didn't run.</span></span>

<span data-ttu-id="b9efe-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**\_SCISSORTEST PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR\_SCISSORTEST**</span></span>  
<span data-ttu-id="b9efe-112">Valore che indica che il pixel è stato rifiutato perché il test della forbice ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b9efe-112">A value that indicates that the pixel was rejected because the scissor test failed.</span></span>

<span data-ttu-id="b9efe-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**\_ALPHATEST PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR\_ALPHATEST**</span></span>  
<span data-ttu-id="b9efe-114">Valore che indica che il pixel è stato rifiutato perché il test alfa ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b9efe-114">A value that indicates that the pixel was rejected because the alpha test failed.</span></span>

<span data-ttu-id="b9efe-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**\_STENCILTEST PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR\_STENCILTEST**</span></span>  
<span data-ttu-id="b9efe-116">Valore che indica che il pixel è stato rifiutato perché il test dello stencil ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b9efe-116">A value that indicates that the pixel was rejected because the stencil test failed.</span></span>

<span data-ttu-id="b9efe-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**\_DEPTHTEST PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR\_DEPTHTEST**</span></span>  
<span data-ttu-id="b9efe-118">Valore che indica che il pixel è stato rifiutato perché il test di profondità non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b9efe-118">A value that indicates that the pixel was rejected because the depth test failed.</span></span>

<span data-ttu-id="b9efe-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**\_NOTCOMPUTABLE PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR\_NOTCOMPUTABLE**</span></span>  
<span data-ttu-id="b9efe-120">Valore che indica che non è possibile calcolare la cronologia dei pixel.</span><span class="sxs-lookup"><span data-stu-id="b9efe-120">A value that indicates that the pixel history can't be computed.</span></span>

<span data-ttu-id="b9efe-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**\_errore PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR\_ERROR**</span></span>  
<span data-ttu-id="b9efe-122">Valore che indica che il pixel è stato rifiutato a causa di un errore generale.</span><span class="sxs-lookup"><span data-stu-id="b9efe-122">A value that indicates that the pixel was rejected because of a general error.</span></span>

<span data-ttu-id="b9efe-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOintersection**</span><span class="sxs-lookup"><span data-stu-id="b9efe-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR\_NOINTERSECTION**</span></span>  
<span data-ttu-id="b9efe-124">Valore che indica che il pixel è stato rifiutato perché la chiamata di progetto non interseca il pixel.</span><span class="sxs-lookup"><span data-stu-id="b9efe-124">A value that indicates that the pixel was rejected because the draw call does not intersect the pixel.</span></span>

<span data-ttu-id="b9efe-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ nascosto**</span><span class="sxs-lookup"><span data-stu-id="b9efe-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR\_OCCLUDED**</span></span>  
<span data-ttu-id="b9efe-126">Valore che indica che il pixel è stato rifiutato perché il progetto è nascosto.</span><span class="sxs-lookup"><span data-stu-id="b9efe-126">A value that indicates that the pixel was rejected because the draw was occluded.</span></span>

<span data-ttu-id="b9efe-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**\_DEPTHSTENCILTEST PKR**</span><span class="sxs-lookup"><span data-stu-id="b9efe-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR\_DEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="b9efe-128">Valore che indica che il pixel è stato rifiutato perché il test di profondità e stencil ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b9efe-128">A value that indicates that the pixel was rejected because the depth and stencil test failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9efe-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9efe-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b9efe-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9efe-130">Header</span></span></p></td><td><span data-ttu-id="b9efe-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b9efe-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



