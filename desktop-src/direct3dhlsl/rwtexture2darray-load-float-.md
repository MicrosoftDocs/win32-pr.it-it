---
title: 'Funzione RWTexture2DArray:: Load (int)'
description: 'Legge i dati della trama. | Funzione RWTexture2DArray:: Load (int)'
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b23439d471f4d22c807c8d45bb00c23a7d814e3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352991"
---
# <a name="rwtexture2darrayloadint-function"></a><span data-ttu-id="02a41-105">Funzione RWTexture2DArray:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="02a41-105">RWTexture2DArray::Load(int) function</span></span>

<span data-ttu-id="02a41-106">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="02a41-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02a41-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="02a41-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="02a41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a41-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02a41-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a41-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="02a41-110">Type: **int**</span></span>

<span data-ttu-id="02a41-111">Posizione della trama.</span><span class="sxs-lookup"><span data-stu-id="02a41-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a41-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02a41-112">Return value</span></span>

<span data-ttu-id="02a41-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="02a41-113">Type:</span></span>

<span data-ttu-id="02a41-114">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="02a41-114">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a41-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="02a41-115">Remarks</span></span>

<span data-ttu-id="02a41-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="02a41-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="02a41-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="02a41-117">Vertex</span></span> | <span data-ttu-id="02a41-118">Hull</span><span class="sxs-lookup"><span data-stu-id="02a41-118">Hull</span></span> | <span data-ttu-id="02a41-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="02a41-119">Domain</span></span> | <span data-ttu-id="02a41-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="02a41-120">Geometry</span></span> | <span data-ttu-id="02a41-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="02a41-121">Pixel</span></span> | <span data-ttu-id="02a41-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="02a41-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="02a41-123">x</span><span class="sxs-lookup"><span data-stu-id="02a41-123">x</span></span>     | <span data-ttu-id="02a41-124">x</span><span class="sxs-lookup"><span data-stu-id="02a41-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="02a41-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02a41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a41-126">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="02a41-126">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 




