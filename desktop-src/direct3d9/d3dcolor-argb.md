---
description: Inizializza un colore con i valori alfa, rosso, verde e blu forniti.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: D3DCOLOR_ARGB macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354424"
---
# <a name="d3dcolor_argb-macro"></a><span data-ttu-id="530e7-103">D3DCOLOR ( \_ macro ARGB)</span><span class="sxs-lookup"><span data-stu-id="530e7-103">D3DCOLOR\_ARGB macro</span></span>

<span data-ttu-id="530e7-104">Inizializza un colore con i valori alfa, rosso, verde e blu forniti.</span><span class="sxs-lookup"><span data-stu-id="530e7-104">Initializes a color with the supplied alpha, red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="530e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="530e7-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="530e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="530e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="530e7-107">*un*</span><span class="sxs-lookup"><span data-stu-id="530e7-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="530e7-108">Componente alfa del colore.</span><span class="sxs-lookup"><span data-stu-id="530e7-108">Alpha component of the color.</span></span> <span data-ttu-id="530e7-109">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="530e7-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="530e7-110">*r*</span><span class="sxs-lookup"><span data-stu-id="530e7-110">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="530e7-111">Componente rosso del colore.</span><span class="sxs-lookup"><span data-stu-id="530e7-111">Red component of the color.</span></span> <span data-ttu-id="530e7-112">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="530e7-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="530e7-113">*g*</span><span class="sxs-lookup"><span data-stu-id="530e7-113">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="530e7-114">Componente verde del colore.</span><span class="sxs-lookup"><span data-stu-id="530e7-114">Green component of the color.</span></span> <span data-ttu-id="530e7-115">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="530e7-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="530e7-116">*b*</span><span class="sxs-lookup"><span data-stu-id="530e7-116">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="530e7-117">Componente blu del colore.</span><span class="sxs-lookup"><span data-stu-id="530e7-117">Blue component of the color.</span></span> <span data-ttu-id="530e7-118">Questo valore deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="530e7-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="530e7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="530e7-119">Return value</span></span>

<span data-ttu-id="530e7-120">Restituisce il valore [D3DCOLOR](d3dcolor.md) che corrisponde ai valori ARGB forniti.</span><span class="sxs-lookup"><span data-stu-id="530e7-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="530e7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="530e7-121">Requirements</span></span>



| <span data-ttu-id="530e7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="530e7-122">Requirement</span></span> | <span data-ttu-id="530e7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="530e7-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="530e7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="530e7-124">Header</span></span><br/> | <dl> <span data-ttu-id="530e7-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="530e7-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530e7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="530e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530e7-127">Macro</span><span class="sxs-lookup"><span data-stu-id="530e7-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="530e7-128">**\_RGBA D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="530e7-128">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> <dt>

[<span data-ttu-id="530e7-129">**\_Sulle XRGB mentre D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="530e7-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




