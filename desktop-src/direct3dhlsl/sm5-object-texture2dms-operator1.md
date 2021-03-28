---
title: 'Funzione Texture2DMS:: operator'
description: Recupera un valore dalla risorsa nel percorso specificato nell'indice di esempio 0.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976959"
---
# <a name="texture2dmsoperator--function"></a><span data-ttu-id="6b2af-104">Funzione Texture2DMS:: operator</span><span class="sxs-lookup"><span data-stu-id="6b2af-104">Texture2DMS::Operator  function</span></span>

<span data-ttu-id="6b2af-105">Recupera un valore dalla risorsa nel percorso specificato nell'indice di esempio 0.</span><span class="sxs-lookup"><span data-stu-id="6b2af-105">Retrieves a value from the resource at the location provided at sample index 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2af-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b2af-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="6b2af-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b2af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2af-108">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b2af-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b2af-109">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="6b2af-109">Type: **uint2**</span></span>

<span data-ttu-id="6b2af-110">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="6b2af-110">The index position.</span></span> <span data-ttu-id="6b2af-111">Contiene le coordinate (x, y).</span><span class="sxs-lookup"><span data-stu-id="6b2af-111">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b2af-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b2af-112">Return value</span></span>

<span data-ttu-id="6b2af-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="6b2af-113">Type: **R**</span></span>

<span data-ttu-id="6b2af-114">Variabile di sola lettura di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b2af-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b2af-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b2af-115">Remarks</span></span>

<span data-ttu-id="6b2af-116">Per selezionare un particolare esempio, vedere l' [**esempio. \[Operatore \] . \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="6b2af-116">To select a particular sample, refer to [**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md).</span></span>

<span data-ttu-id="6b2af-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b2af-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6b2af-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="6b2af-118">Vertex</span></span> | <span data-ttu-id="6b2af-119">Hull</span><span class="sxs-lookup"><span data-stu-id="6b2af-119">Hull</span></span> | <span data-ttu-id="6b2af-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="6b2af-120">Domain</span></span> | <span data-ttu-id="6b2af-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="6b2af-121">Geometry</span></span> | <span data-ttu-id="6b2af-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="6b2af-122">Pixel</span></span> | <span data-ttu-id="6b2af-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6b2af-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6b2af-124">x</span><span class="sxs-lookup"><span data-stu-id="6b2af-124">x</span></span>      | <span data-ttu-id="6b2af-125">x</span><span class="sxs-lookup"><span data-stu-id="6b2af-125">x</span></span>    | <span data-ttu-id="6b2af-126">x</span><span class="sxs-lookup"><span data-stu-id="6b2af-126">x</span></span>      | <span data-ttu-id="6b2af-127">x</span><span class="sxs-lookup"><span data-stu-id="6b2af-127">x</span></span>        | <span data-ttu-id="6b2af-128">x</span><span class="sxs-lookup"><span data-stu-id="6b2af-128">x</span></span>     | <span data-ttu-id="6b2af-129">x</span><span class="sxs-lookup"><span data-stu-id="6b2af-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6b2af-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b2af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2af-131">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="6b2af-131">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="6b2af-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="6b2af-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




