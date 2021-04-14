---
description: Valuta una luce direzionale e restituisce dati ad armonica sferica (SH) spettrale.
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: Funzione D3DXSHEvalDirectionalLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9c6b5c9590132d9fe3d0fc07ae419d442144079a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104569221"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a><span data-ttu-id="3fe8c-103">Funzione D3DXSHEvalDirectionalLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="3fe8c-103">D3DXSHEvalDirectionalLight function (D3DX10.h)</span></span>

<span data-ttu-id="3fe8c-104">Valuta una luce direzionale e restituisce dati ad armonica sferica (SH) spettrale.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-104">Evaluates a directional light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe8c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fe8c-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="3fe8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fe8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fe8c-107">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe8c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fe8c-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-109">Order of the SH evaluation.</span></span> <span data-ttu-id="3fe8c-110">Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3fe8c-111">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="3fe8c-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3fe8c-112">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3fe8c-113">*pDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3fe8c-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3fe8c-115">Puntatore al vettore di direzione dell'asse del (x, y, z) in cui valutare le funzioni di base SH.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="3fe8c-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3fe8c-117">*RIntensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe8c-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fe8c-119">Intensità rossa della luce.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3fe8c-120">*GIntensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe8c-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fe8c-122">Intensità verde della luce.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3fe8c-123">*BIntensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe8c-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fe8c-125">Intensità blu della luce.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3fe8c-126">*pROut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-126">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fe8c-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3fe8c-128">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="3fe8c-129">*pGOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-129">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fe8c-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3fe8c-131">Puntatore facoltativo al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="3fe8c-132">*pBOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fe8c-132">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe8c-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fe8c-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3fe8c-134">Puntatore facoltativo al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fe8c-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fe8c-135">Return value</span></span>

<span data-ttu-id="3fe8c-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3fe8c-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3fe8c-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3fe8c-138">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fe8c-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fe8c-139">Remarks</span></span>

<span data-ttu-id="3fe8c-140">Il vettore di output viene calcolato in modo tale che se il rapporto di intensità R/G/B è uguale a 1, la luminosità di uscita risultante di un punto immediatamente sotto la luce di un oggetto diffuso con un'albedo pari a 1 è 1,0.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="3fe8c-141">Verrà calcolato tre campioni spettrali; viene restituito pROut, mentre pGOut e pBOut possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-141">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="3fe8c-142">Nella sfera con raggio di unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con Theta, l'angolo sull'asse z nella direzione destra e Phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unitario](images/spherical-coordinates.png)

<span data-ttu-id="3fe8c-144">Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, Phi) nella sfera dell'unità.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="3fe8c-145">L'angolo theta varia nell'intervallo compreso tra 0 e 2 pi, mentre Phi varia da 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="3fe8c-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="3fe8c-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fe8c-147">Requirements</span></span>



| <span data-ttu-id="3fe8c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fe8c-148">Requirement</span></span> | <span data-ttu-id="3fe8c-149">Valore</span><span class="sxs-lookup"><span data-stu-id="3fe8c-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe8c-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fe8c-150">Header</span></span><br/>  | <dl> <span data-ttu-id="3fe8c-151"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fe8c-151"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fe8c-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="3fe8c-152">Library</span></span><br/> | <dl> <span data-ttu-id="3fe8c-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fe8c-153"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fe8c-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fe8c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe8c-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="3fe8c-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
