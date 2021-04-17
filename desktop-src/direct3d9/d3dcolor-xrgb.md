---
description: Inizializza un colore con i valori rosso, verde e blu forniti.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: D3DCOLOR_XRGB macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401939"
---
# <a name="d3dcolor_xrgb-macro"></a><span data-ttu-id="d3541-103">D3DCOLOR \_ sulle XRGB mentre-macro</span><span class="sxs-lookup"><span data-stu-id="d3541-103">D3DCOLOR\_XRGB macro</span></span>

<span data-ttu-id="d3541-104">Inizializza un colore con i valori rosso, verde e blu forniti.</span><span class="sxs-lookup"><span data-stu-id="d3541-104">Initializes a color with the supplied red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3541-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3541-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="d3541-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3541-107">*r*</span><span class="sxs-lookup"><span data-stu-id="d3541-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="d3541-108">Componente rosso del colore.</span><span class="sxs-lookup"><span data-stu-id="d3541-108">Red component of the color.</span></span> <span data-ttu-id="d3541-109">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="d3541-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="d3541-110">*g*</span><span class="sxs-lookup"><span data-stu-id="d3541-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="d3541-111">Componente verde del colore.</span><span class="sxs-lookup"><span data-stu-id="d3541-111">Green component of the color.</span></span> <span data-ttu-id="d3541-112">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="d3541-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="d3541-113">*b*</span><span class="sxs-lookup"><span data-stu-id="d3541-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="d3541-114">Componente blu del colore.</span><span class="sxs-lookup"><span data-stu-id="d3541-114">Blue component of the color.</span></span> <span data-ttu-id="d3541-115">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="d3541-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3541-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3541-116">Return value</span></span>

<span data-ttu-id="d3541-117">Restituisce il valore [**D3DCOLOR**](d3dcolor.md) che corrisponde ai valori RGB forniti.</span><span class="sxs-lookup"><span data-stu-id="d3541-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3541-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3541-118">Requirements</span></span>



| <span data-ttu-id="d3541-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3541-119">Requirement</span></span> | <span data-ttu-id="d3541-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d3541-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3541-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3541-121">Header</span></span><br/> | <dl> <span data-ttu-id="d3541-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3541-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3541-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3541-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3541-124">Macro</span><span class="sxs-lookup"><span data-stu-id="d3541-124">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="d3541-125">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="d3541-125">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="d3541-126">**\_RGBA D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="d3541-126">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> </dl>

 

 




