---
title: 'Funzione RWTexture1D:: Load (int)'
description: 'Legge i dati della trama. | Funzione RWTexture1D:: Load (int)'
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: e78cd12502ada91e48df1ce88be6a19fb714327f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353116"
---
# <a name="rwtexture1dloadint-function"></a><span data-ttu-id="feddc-105">Funzione RWTexture1D:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="feddc-105">RWTexture1D::Load(int) function</span></span>

<span data-ttu-id="feddc-106">Legge i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="feddc-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="feddc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="feddc-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="feddc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="feddc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feddc-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="feddc-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feddc-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="feddc-110">Type: **int**</span></span>

<span data-ttu-id="feddc-111">Posizione della trama.</span><span class="sxs-lookup"><span data-stu-id="feddc-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feddc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="feddc-112">Return value</span></span>

<span data-ttu-id="feddc-113">Digitare:</span><span class="sxs-lookup"><span data-stu-id="feddc-113">Type:</span></span>

<span data-ttu-id="feddc-114">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWTexture1D**](sm5-object-rwtexture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="feddc-114">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="feddc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="feddc-115">Remarks</span></span>

<span data-ttu-id="feddc-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="feddc-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="feddc-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="feddc-117">Vertex</span></span> | <span data-ttu-id="feddc-118">Hull</span><span class="sxs-lookup"><span data-stu-id="feddc-118">Hull</span></span> | <span data-ttu-id="feddc-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="feddc-119">Domain</span></span> | <span data-ttu-id="feddc-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="feddc-120">Geometry</span></span> | <span data-ttu-id="feddc-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="feddc-121">Pixel</span></span> | <span data-ttu-id="feddc-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="feddc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="feddc-123">x</span><span class="sxs-lookup"><span data-stu-id="feddc-123">x</span></span>     | <span data-ttu-id="feddc-124">x</span><span class="sxs-lookup"><span data-stu-id="feddc-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="feddc-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="feddc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feddc-126">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="feddc-126">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 




