---
description: Inizializza un colore usando i valori (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322374"
---
# <a name="d3dcolor_ayuv-macro"></a><span data-ttu-id="bc429-103">D3DCOLOR \_ AYUV-macro</span><span class="sxs-lookup"><span data-stu-id="bc429-103">D3DCOLOR\_AYUV macro</span></span>

<span data-ttu-id="bc429-104">Inizializza un colore usando i valori (a, y, u, v).</span><span class="sxs-lookup"><span data-stu-id="bc429-104">Initializes a color using the (a,y,u,v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc429-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc429-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="bc429-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc429-107">*un*</span><span class="sxs-lookup"><span data-stu-id="bc429-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="bc429-108">Componente alfa del colore.</span><span class="sxs-lookup"><span data-stu-id="bc429-108">Alpha component of the color.</span></span> <span data-ttu-id="bc429-109">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="bc429-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="bc429-110">*y*</span><span class="sxs-lookup"><span data-stu-id="bc429-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="bc429-111">Componente di luminanza del colore.</span><span class="sxs-lookup"><span data-stu-id="bc429-111">Luminance component of the color.</span></span> <span data-ttu-id="bc429-112">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="bc429-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="bc429-113">*u*</span><span class="sxs-lookup"><span data-stu-id="bc429-113">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="bc429-114">Luminosità blu del colore.</span><span class="sxs-lookup"><span data-stu-id="bc429-114">Blue brightness of the color.</span></span> <span data-ttu-id="bc429-115">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="bc429-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="bc429-116">*v*</span><span class="sxs-lookup"><span data-stu-id="bc429-116">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="bc429-117">Luminosità rossa del colore.</span><span class="sxs-lookup"><span data-stu-id="bc429-117">Red brightness of the color.</span></span> <span data-ttu-id="bc429-118">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="bc429-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc429-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc429-119">Return value</span></span>

<span data-ttu-id="bc429-120">Restituisce il valore [D3DCOLOR](d3dcolor.md) che corrisponde ai valori ARGB forniti.</span><span class="sxs-lookup"><span data-stu-id="bc429-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc429-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc429-121">Remarks</span></span>

<span data-ttu-id="bc429-122">Un colore RGB può essere ridotto a 16 bit per pixel mediante conversione in luminanza e differenze di colore con le equazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc429-122">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="bc429-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc429-123">Requirements</span></span>



| <span data-ttu-id="bc429-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc429-124">Requirement</span></span> | <span data-ttu-id="bc429-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bc429-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc429-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc429-126">Header</span></span><br/> | <dl> <span data-ttu-id="bc429-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc429-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc429-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc429-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc429-129">Macro</span><span class="sxs-lookup"><span data-stu-id="bc429-129">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="bc429-130">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="bc429-130">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="bc429-131">**\_XYUV D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="bc429-131">**D3DCOLOR\_XYUV**</span></span>](d3dcolor-xyuv.md)
</dt> </dl>

 

 




