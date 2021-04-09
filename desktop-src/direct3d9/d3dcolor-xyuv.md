---
description: Inizializza un colore con i valori (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: D3DCOLOR_XYUV macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886271"
---
# <a name="d3dcolor_xyuv-macro"></a><span data-ttu-id="9fd2f-103">D3DCOLOR \_ XYUV-macro</span><span class="sxs-lookup"><span data-stu-id="9fd2f-103">D3DCOLOR\_XYUV macro</span></span>

<span data-ttu-id="9fd2f-104">Inizializza un colore con i valori (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="9fd2f-104">Initializes a color with the (y, u, v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd2f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fd2f-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="9fd2f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fd2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd2f-107">*y*</span><span class="sxs-lookup"><span data-stu-id="9fd2f-107">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd2f-108">Componente di luminanza del colore.</span><span class="sxs-lookup"><span data-stu-id="9fd2f-108">Luminance component of the color.</span></span> <span data-ttu-id="9fd2f-109">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="9fd2f-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="9fd2f-110">*u*</span><span class="sxs-lookup"><span data-stu-id="9fd2f-110">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd2f-111">Luminosità blu del colore.</span><span class="sxs-lookup"><span data-stu-id="9fd2f-111">Blue brightness of the color.</span></span> <span data-ttu-id="9fd2f-112">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="9fd2f-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="9fd2f-113">*v*</span><span class="sxs-lookup"><span data-stu-id="9fd2f-113">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd2f-114">Luminosità rossa del colore.</span><span class="sxs-lookup"><span data-stu-id="9fd2f-114">Red brightness of the color.</span></span> <span data-ttu-id="9fd2f-115">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="9fd2f-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd2f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fd2f-116">Return value</span></span>

<span data-ttu-id="9fd2f-117">Restituisce il valore [**D3DCOLOR**](d3dcolor.md) che corrisponde ai valori specificati (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="9fd2f-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied (y, u, v) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fd2f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fd2f-118">Remarks</span></span>

<span data-ttu-id="9fd2f-119">Un colore RGB può essere ridotto a 16 bit per pixel mediante conversione in luminanza e differenze di colore con le equazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9fd2f-119">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="9fd2f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fd2f-120">Requirements</span></span>



| <span data-ttu-id="9fd2f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fd2f-121">Requirement</span></span> | <span data-ttu-id="9fd2f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9fd2f-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd2f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fd2f-123">Header</span></span><br/> | <dl> <span data-ttu-id="9fd2f-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd2f-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd2f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fd2f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd2f-126">Macro</span><span class="sxs-lookup"><span data-stu-id="9fd2f-126">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="9fd2f-127">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="9fd2f-127">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="9fd2f-128">**\_AYUV D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="9fd2f-128">**D3DCOLOR\_AYUV**</span></span>](d3dcolor-ayuv.md)
</dt> </dl>

 

 




