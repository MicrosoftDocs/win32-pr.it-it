---
title: 'Funzione RWTexture3D:: operator'
description: Restituisce una variabile di risorsa di un RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
keywords:
- Funzione operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e41ff4db387c4d0926083419082fd589005d96a6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976935"
---
# <a name="rwtexture3doperator--function"></a><span data-ttu-id="4ca52-104">Funzione RWTexture3D:: operator</span><span class="sxs-lookup"><span data-stu-id="4ca52-104">RWTexture3D::Operator  function</span></span>

<span data-ttu-id="4ca52-105">Restituisce una variabile di risorsa di un [**RWTexture3D**](sm5-object-rwtexture3d.md).</span><span class="sxs-lookup"><span data-stu-id="4ca52-105">Returns a resource variable of a [**RWTexture3D**](sm5-object-rwtexture3d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca52-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ca52-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="4ca52-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ca52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca52-108">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ca52-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca52-109">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="4ca52-109">Type: **uint3**</span></span>

<span data-ttu-id="4ca52-110">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="4ca52-110">The index position.</span></span> <span data-ttu-id="4ca52-111">Contiene le coordinate (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="4ca52-111">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca52-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ca52-112">Return value</span></span>

<span data-ttu-id="4ca52-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="4ca52-113">Type: **R**</span></span>

<span data-ttu-id="4ca52-114">Variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="4ca52-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca52-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ca52-115">Remarks</span></span>

<span data-ttu-id="4ca52-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ca52-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4ca52-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="4ca52-117">Vertex</span></span> | <span data-ttu-id="4ca52-118">Hull</span><span class="sxs-lookup"><span data-stu-id="4ca52-118">Hull</span></span> | <span data-ttu-id="4ca52-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="4ca52-119">Domain</span></span> | <span data-ttu-id="4ca52-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="4ca52-120">Geometry</span></span> | <span data-ttu-id="4ca52-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="4ca52-121">Pixel</span></span> | <span data-ttu-id="4ca52-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4ca52-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4ca52-123">x</span><span class="sxs-lookup"><span data-stu-id="4ca52-123">x</span></span>     | <span data-ttu-id="4ca52-124">x</span><span class="sxs-lookup"><span data-stu-id="4ca52-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4ca52-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ca52-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca52-126">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="4ca52-126">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="4ca52-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4ca52-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




