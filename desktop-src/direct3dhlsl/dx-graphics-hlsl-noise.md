---
title: rumore
description: Genera un valore casuale usando l'algoritmo Perlin-noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- HLSL rumore
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399956"
---
# <a name="noise"></a><span data-ttu-id="860b2-104">rumore</span><span class="sxs-lookup"><span data-stu-id="860b2-104">noise</span></span>

<span data-ttu-id="860b2-105">Genera un valore casuale usando l'algoritmo Perlin-noise.</span><span class="sxs-lookup"><span data-stu-id="860b2-105">Generates a random value using the Perlin-noise algorithm.</span></span>




| <span data-ttu-id="860b2-106">rumore *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="860b2-106">*ret* noise(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="860b2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="860b2-107">Parameters</span></span>



| <span data-ttu-id="860b2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="860b2-108">Item</span></span>                                                   | <span data-ttu-id="860b2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="860b2-109">Description</span></span>                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="860b2-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="860b2-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="860b2-111">\[in \] un vettore a virgola mobile da cui generare il rumore Perlin.</span><span class="sxs-lookup"><span data-stu-id="860b2-111">\[in\] A floating-point vector from which to generate Perlin noise.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="860b2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="860b2-112">Return Value</span></span>

<span data-ttu-id="860b2-113">Valore del rumore Perlin compreso in un intervallo compreso tra-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="860b2-113">The Perlin noise value within a range between -1 and 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="860b2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="860b2-114">Remarks</span></span>

<span data-ttu-id="860b2-115">I valori del rumore Perlin cambiano senza intoppi da un punto a un altro su uno spazio, creando valori generati in modo casuale e alla ricerca naturale.</span><span class="sxs-lookup"><span data-stu-id="860b2-115">Perlin noise values change smoothly from one point to another over a space, creating natural looking, randomly generated values.</span></span> <span data-ttu-id="860b2-116">È possibile usare il rumore Perlin per generare trame procedurali per effetti quali fumo e incendi.</span><span class="sxs-lookup"><span data-stu-id="860b2-116">You can use Perlin noise to generate procedural textures for effects like smoke and fire.</span></span>

## <a name="type-description"></a><span data-ttu-id="860b2-117">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="860b2-117">Type Description</span></span>



| <span data-ttu-id="860b2-118">Nome</span><span class="sxs-lookup"><span data-stu-id="860b2-118">Name</span></span>  | [<span data-ttu-id="860b2-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="860b2-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="860b2-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="860b2-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="860b2-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="860b2-121">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="860b2-122">*x*</span><span class="sxs-lookup"><span data-stu-id="860b2-122">*x*</span></span>   | [<span data-ttu-id="860b2-123">**vettore**</span><span class="sxs-lookup"><span data-stu-id="860b2-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="860b2-124">**float**</span><span class="sxs-lookup"><span data-stu-id="860b2-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="860b2-125">any</span><span class="sxs-lookup"><span data-stu-id="860b2-125">any</span></span>  |
| <span data-ttu-id="860b2-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="860b2-126">*ret*</span></span> | [<span data-ttu-id="860b2-127">**scalare**</span><span class="sxs-lookup"><span data-stu-id="860b2-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="860b2-128">**float**</span><span class="sxs-lookup"><span data-stu-id="860b2-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="860b2-129">1</span><span class="sxs-lookup"><span data-stu-id="860b2-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="860b2-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="860b2-130">Minimum Shader Model</span></span>

<span data-ttu-id="860b2-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="860b2-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="860b2-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="860b2-132">Shader Model</span></span>                                                                       | <span data-ttu-id="860b2-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="860b2-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="860b2-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="860b2-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="860b2-135">no</span><span class="sxs-lookup"><span data-stu-id="860b2-135">no</span></span>                  |
| [<span data-ttu-id="860b2-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="860b2-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="860b2-137">Sì ( \_ solo TX 1 \_ 0)</span><span class="sxs-lookup"><span data-stu-id="860b2-137">yes (tx\_1\_0 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="860b2-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="860b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="860b2-139">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="860b2-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

