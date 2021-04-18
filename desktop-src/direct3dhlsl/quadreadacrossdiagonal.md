---
title: QuadReadAcrossDiagonal (funzione)
description: Restituisce il valore locale specificato che viene letto dalla corsia opposta in senso diagonale in questo quad.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- Funzione QuadReadAcrossDiagonal HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e208a022f339e69ea63120db1f67070fa4dfed7
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993629"
---
# <a name="quadreadacrossdiagonal-function"></a><span data-ttu-id="d5998-104">QuadReadAcrossDiagonal (funzione)</span><span class="sxs-lookup"><span data-stu-id="d5998-104">QuadReadAcrossDiagonal function</span></span>

<span data-ttu-id="d5998-105">Restituisce il valore locale specificato che viene letto dalla corsia opposta in senso diagonale in questo quad.</span><span class="sxs-lookup"><span data-stu-id="d5998-105">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5998-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5998-106">Syntax</span></span>


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a><span data-ttu-id="d5998-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5998-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5998-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="d5998-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="d5998-109">Tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="d5998-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5998-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5998-110">Return value</span></span>

<span data-ttu-id="d5998-111">Valore locale specificato che viene letto dalla corsia opposta in senso diagonale in questo quad.</span><span class="sxs-lookup"><span data-stu-id="d5998-111">The specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5998-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5998-112">Remarks</span></span>

<span data-ttu-id="d5998-113">Per altre informazioni sui quad, vedere [Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="d5998-113">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="d5998-114">Questa funzione è supportata dal modello di shader 6,0 solo in pixel e compute shader.</span><span class="sxs-lookup"><span data-stu-id="d5998-114">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="d5998-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5998-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5998-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="d5998-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




