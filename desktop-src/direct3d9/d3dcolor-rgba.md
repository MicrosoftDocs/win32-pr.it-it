---
description: Inizializza un colore con i valori rosso, verde, blu e alfa forniti.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: D3DCOLOR_RGBA macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322372"
---
# <a name="d3dcolor_rgba-macro"></a><span data-ttu-id="e5c93-103">D3DCOLOR \_ RGBA-macro</span><span class="sxs-lookup"><span data-stu-id="e5c93-103">D3DCOLOR\_RGBA macro</span></span>

<span data-ttu-id="e5c93-104">Inizializza un colore con i valori rosso, verde, blu e alfa forniti.</span><span class="sxs-lookup"><span data-stu-id="e5c93-104">Initializes a color with the supplied red, green, blue, and alpha values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c93-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5c93-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a><span data-ttu-id="e5c93-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5c93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c93-107">*r*</span><span class="sxs-lookup"><span data-stu-id="e5c93-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c93-108">Componente rosso del colore.</span><span class="sxs-lookup"><span data-stu-id="e5c93-108">Red component of the color.</span></span> <span data-ttu-id="e5c93-109">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e5c93-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="e5c93-110">*g*</span><span class="sxs-lookup"><span data-stu-id="e5c93-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c93-111">Componente verde del colore.</span><span class="sxs-lookup"><span data-stu-id="e5c93-111">Green component of the color.</span></span> <span data-ttu-id="e5c93-112">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e5c93-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="e5c93-113">*b*</span><span class="sxs-lookup"><span data-stu-id="e5c93-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c93-114">Componente blu del colore.</span><span class="sxs-lookup"><span data-stu-id="e5c93-114">Blue component of the color.</span></span> <span data-ttu-id="e5c93-115">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e5c93-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="e5c93-116">*un*</span><span class="sxs-lookup"><span data-stu-id="e5c93-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c93-117">Componente alfa del colore.</span><span class="sxs-lookup"><span data-stu-id="e5c93-117">Alpha component of the color.</span></span> <span data-ttu-id="e5c93-118">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e5c93-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c93-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5c93-119">Return value</span></span>

<span data-ttu-id="e5c93-120">Restituisce il valore [**D3DCOLOR**](d3dcolor.md) che corrisponde ai valori RGBA forniti.</span><span class="sxs-lookup"><span data-stu-id="e5c93-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c93-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5c93-121">Requirements</span></span>



| <span data-ttu-id="e5c93-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c93-122">Requirement</span></span> | <span data-ttu-id="e5c93-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e5c93-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c93-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5c93-124">Header</span></span><br/> | <dl> <span data-ttu-id="e5c93-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c93-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c93-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5c93-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c93-127">Macro</span><span class="sxs-lookup"><span data-stu-id="e5c93-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="e5c93-128">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="e5c93-128">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="e5c93-129">**\_Sulle XRGB mentre D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="e5c93-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




