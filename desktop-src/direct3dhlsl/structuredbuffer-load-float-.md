---
title: 'Funzione StructuredBuffer:: Load (int)'
description: 'Legge i dati del buffer. | Funzione StructuredBuffer:: Load (int)'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981898"
---
# <a name="structuredbufferloadint-function"></a><span data-ttu-id="8f3f7-105">Funzione StructuredBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="8f3f7-105">StructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="8f3f7-106">Legge i dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="8f3f7-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f3f7-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="8f3f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f3f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f3f7-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f3f7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3f7-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="8f3f7-110">Type: **int**</span></span>

<span data-ttu-id="8f3f7-111">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="8f3f7-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f3f7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f3f7-112">Return value</span></span>

<span data-ttu-id="8f3f7-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="8f3f7-113">Type:</span></span>

<span data-ttu-id="8f3f7-114">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**StructuredBuffer**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8f3f7-114">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f3f7-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f3f7-115">Remarks</span></span>

<span data-ttu-id="8f3f7-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f3f7-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8f3f7-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="8f3f7-117">Vertex</span></span> | <span data-ttu-id="8f3f7-118">Hull</span><span class="sxs-lookup"><span data-stu-id="8f3f7-118">Hull</span></span> | <span data-ttu-id="8f3f7-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="8f3f7-119">Domain</span></span> | <span data-ttu-id="8f3f7-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="8f3f7-120">Geometry</span></span> | <span data-ttu-id="8f3f7-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="8f3f7-121">Pixel</span></span> | <span data-ttu-id="8f3f7-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="8f3f7-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8f3f7-123">x</span><span class="sxs-lookup"><span data-stu-id="8f3f7-123">x</span></span>     | <span data-ttu-id="8f3f7-124">x</span><span class="sxs-lookup"><span data-stu-id="8f3f7-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8f3f7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f3f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3f7-126">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="8f3f7-126">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 




