---
title: 'Funzione Texture2DMS:: Load (int, int)'
description: 'Ottiene un valore. | Funzione Texture2DMS:: Load (int, int)'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Funzione Load DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981591"
---
# <a name="texture2dmsloadintint-function"></a><span data-ttu-id="71f82-105">Funzione Texture2DMS:: Load (int, int)</span><span class="sxs-lookup"><span data-stu-id="71f82-105">Texture2DMS::Load(int,int) function</span></span>

<span data-ttu-id="71f82-106">Ottiene un valore.</span><span class="sxs-lookup"><span data-stu-id="71f82-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f82-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71f82-107">Syntax</span></span>

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="71f82-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71f82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f82-109">*Coord* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f82-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f82-110">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="71f82-110">Type: **int2**</span></span>

<span data-ttu-id="71f82-111">Percorso di input.</span><span class="sxs-lookup"><span data-stu-id="71f82-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="71f82-112">*sampleindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f82-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f82-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="71f82-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="71f82-114">Indice di esempio.</span><span class="sxs-lookup"><span data-stu-id="71f82-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f82-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71f82-115">Return value</span></span>

<span data-ttu-id="71f82-116">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="71f82-116">Type: **T**</span></span>

<span data-ttu-id="71f82-117">Un valore il cui tipo corrisponde al tipo di modello di trama.</span><span class="sxs-lookup"><span data-stu-id="71f82-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="71f82-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="71f82-118">Remarks</span></span>

<span data-ttu-id="71f82-119">Si tratta di un elenco delle versioni di overload di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="71f82-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="71f82-120">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="71f82-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="71f82-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="71f82-121">Vertex</span></span> | <span data-ttu-id="71f82-122">Hull</span><span class="sxs-lookup"><span data-stu-id="71f82-122">Hull</span></span> | <span data-ttu-id="71f82-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="71f82-123">Domain</span></span> | <span data-ttu-id="71f82-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="71f82-124">Geometry</span></span> | <span data-ttu-id="71f82-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="71f82-125">Pixel</span></span> | <span data-ttu-id="71f82-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="71f82-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="71f82-127">x</span><span class="sxs-lookup"><span data-stu-id="71f82-127">x</span></span>     | <span data-ttu-id="71f82-128">x</span><span class="sxs-lookup"><span data-stu-id="71f82-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="71f82-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71f82-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f82-130">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="71f82-130">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="71f82-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="71f82-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
