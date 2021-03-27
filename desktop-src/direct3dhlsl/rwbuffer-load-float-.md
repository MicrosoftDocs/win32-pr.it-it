---
title: 'Funzione RWBuffer:: Load (int)'
description: 'Legge i dati del buffer. | Funzione RWBuffer:: Load (int)'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761692"
---
# <a name="rwbufferloadint-function"></a><span data-ttu-id="5f654-105">Funzione RWBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="5f654-105">RWBuffer::Load(int) function</span></span>

<span data-ttu-id="5f654-106">Legge i dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="5f654-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f654-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f654-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="5f654-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f654-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f654-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f654-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f654-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5f654-110">Type: **int**</span></span>

<span data-ttu-id="5f654-111">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="5f654-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f654-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f654-112">Return value</span></span>

<span data-ttu-id="5f654-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="5f654-113">Type:</span></span>

<span data-ttu-id="5f654-114">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWBuffer**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5f654-114">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f654-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f654-115">Remarks</span></span>

<span data-ttu-id="5f654-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f654-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5f654-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="5f654-117">Vertex</span></span> | <span data-ttu-id="5f654-118">Hull</span><span class="sxs-lookup"><span data-stu-id="5f654-118">Hull</span></span> | <span data-ttu-id="5f654-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="5f654-119">Domain</span></span> | <span data-ttu-id="5f654-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="5f654-120">Geometry</span></span> | <span data-ttu-id="5f654-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="5f654-121">Pixel</span></span> | <span data-ttu-id="5f654-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="5f654-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5f654-123">x</span><span class="sxs-lookup"><span data-stu-id="5f654-123">x</span></span>      | <span data-ttu-id="5f654-124">x</span><span class="sxs-lookup"><span data-stu-id="5f654-124">x</span></span>    | <span data-ttu-id="5f654-125">x</span><span class="sxs-lookup"><span data-stu-id="5f654-125">x</span></span>      | <span data-ttu-id="5f654-126">x</span><span class="sxs-lookup"><span data-stu-id="5f654-126">x</span></span>        | <span data-ttu-id="5f654-127">x</span><span class="sxs-lookup"><span data-stu-id="5f654-127">x</span></span>     | <span data-ttu-id="5f654-128">x</span><span class="sxs-lookup"><span data-stu-id="5f654-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5f654-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f654-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f654-130">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="5f654-130">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 




