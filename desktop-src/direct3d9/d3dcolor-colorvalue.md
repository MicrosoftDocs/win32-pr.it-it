---
description: Inizializza un colore con i valori a virgola mobile rosso, verde, blu e alfa forniti.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761956"
---
# <a name="d3dcolor_colorvalue-macro"></a><span data-ttu-id="b4dd9-103">D3DCOLOR \_ COLORVALUE-macro</span><span class="sxs-lookup"><span data-stu-id="b4dd9-103">D3DCOLOR\_COLORVALUE macro</span></span>

<span data-ttu-id="b4dd9-104">Inizializza un colore con i valori a virgola mobile rosso, verde, blu e alfa forniti.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-104">Initializes a color with the supplied red, green, blue, and alpha floating-point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4dd9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4dd9-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a><span data-ttu-id="b4dd9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4dd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4dd9-107">*r*</span><span class="sxs-lookup"><span data-stu-id="b4dd9-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="b4dd9-108">Componente rosso del colore.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-108">Red component of the color.</span></span> <span data-ttu-id="b4dd9-109">Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-109">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="b4dd9-110">*g*</span><span class="sxs-lookup"><span data-stu-id="b4dd9-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="b4dd9-111">Componente verde del colore.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-111">Green component of the color.</span></span> <span data-ttu-id="b4dd9-112">Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-112">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="b4dd9-113">*b*</span><span class="sxs-lookup"><span data-stu-id="b4dd9-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="b4dd9-114">Componente blu del colore.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-114">Blue component of the color.</span></span> <span data-ttu-id="b4dd9-115">Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-115">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="b4dd9-116">*un*</span><span class="sxs-lookup"><span data-stu-id="b4dd9-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="b4dd9-117">Componente alfa del colore.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-117">Alpha component of the color.</span></span> <span data-ttu-id="b4dd9-118">Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-118">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4dd9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4dd9-119">Return value</span></span>

<span data-ttu-id="b4dd9-120">Restituisce il valore [**D3DCOLOR**](d3dcolor.md) che corrisponde ai valori RGBA forniti.</span><span class="sxs-lookup"><span data-stu-id="b4dd9-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4dd9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4dd9-121">Requirements</span></span>



| <span data-ttu-id="b4dd9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4dd9-122">Requirement</span></span> | <span data-ttu-id="b4dd9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b4dd9-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4dd9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4dd9-124">Header</span></span><br/> | <dl> <span data-ttu-id="b4dd9-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4dd9-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4dd9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4dd9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4dd9-127">Macro</span><span class="sxs-lookup"><span data-stu-id="b4dd9-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




