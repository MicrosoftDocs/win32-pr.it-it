---
title: 'Funzione RWTexture1DArray:: Load (int)'
description: 'Legge i dati della trama. | Funzione RWTexture1DArray:: Load (int)'
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 4eb0dcbfe7a465756f865b90d2a39f65784bcd8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981242"
---
# <a name="rwtexture1darrayloadint-function"></a><span data-ttu-id="1c65f-105">Funzione RWTexture1DArray:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="1c65f-105">RWTexture1DArray::Load(int) function</span></span>

<span data-ttu-id="1c65f-106">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="1c65f-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c65f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c65f-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="1c65f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c65f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c65f-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c65f-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c65f-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1c65f-110">Type: **int**</span></span>

<span data-ttu-id="1c65f-111">Posizione della trama.</span><span class="sxs-lookup"><span data-stu-id="1c65f-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c65f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c65f-112">Return value</span></span>

<span data-ttu-id="1c65f-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="1c65f-113">Type:</span></span>

<span data-ttu-id="1c65f-114">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="1c65f-114">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c65f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c65f-115">Remarks</span></span>

<span data-ttu-id="1c65f-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1c65f-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1c65f-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="1c65f-117">Vertex</span></span> | <span data-ttu-id="1c65f-118">Hull</span><span class="sxs-lookup"><span data-stu-id="1c65f-118">Hull</span></span> | <span data-ttu-id="1c65f-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="1c65f-119">Domain</span></span> | <span data-ttu-id="1c65f-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="1c65f-120">Geometry</span></span> | <span data-ttu-id="1c65f-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="1c65f-121">Pixel</span></span> | <span data-ttu-id="1c65f-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="1c65f-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1c65f-123">x</span><span class="sxs-lookup"><span data-stu-id="1c65f-123">x</span></span>     | <span data-ttu-id="1c65f-124">x</span><span class="sxs-lookup"><span data-stu-id="1c65f-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1c65f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c65f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c65f-126">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="1c65f-126">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 




