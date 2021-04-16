---
description: Calcolare il termine Fresnel.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Funzione D3DXFresnelTerm (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e87649d340e7d90c4df02c641919fd906631268
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531051"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a><span data-ttu-id="d4bcc-103">Funzione D3DXFresnelTerm (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d4bcc-103">D3DXFresnelTerm function (D3DX10Math.h)</span></span>

<span data-ttu-id="d4bcc-104">Calcolare il termine Fresnel.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4bcc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4bcc-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d4bcc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4bcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4bcc-107">*CosTheta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4bcc-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4bcc-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4bcc-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4bcc-109">Il valore deve essere compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="d4bcc-110">*RefractionIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4bcc-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4bcc-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4bcc-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4bcc-112">Indice di rifrazione di un materiale.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-112">The refraction index of a material.</span></span> <span data-ttu-id="d4bcc-113">Il valore deve essere maggiore di 1.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4bcc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4bcc-114">Return value</span></span>

<span data-ttu-id="d4bcc-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4bcc-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4bcc-116">Questa funzione restituisce il termine Fresnel per la luce non polarizzata.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="d4bcc-117">CosTheta è il coseno dell'angolo dell'evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d4bcc-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4bcc-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4bcc-118">Remarks</span></span>

<span data-ttu-id="d4bcc-119">Per trovare il termine Fresnel (F):</span><span class="sxs-lookup"><span data-stu-id="d4bcc-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="d4bcc-120">Se A è angolo di incidenza e B è l'angolo della rifrazione,</span><span class="sxs-lookup"><span data-stu-id="d4bcc-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="d4bcc-121">Quindi, espandendo usando le identità trigonometriche e semplificando, si ottengono:</span><span class="sxs-lookup"><span data-stu-id="d4bcc-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="d4bcc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4bcc-122">Requirements</span></span>



| <span data-ttu-id="d4bcc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4bcc-123">Requirement</span></span> | <span data-ttu-id="d4bcc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d4bcc-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bcc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4bcc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d4bcc-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4bcc-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d4bcc-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4bcc-127">Library</span></span><br/> | <dl> <span data-ttu-id="d4bcc-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4bcc-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4bcc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4bcc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4bcc-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d4bcc-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
