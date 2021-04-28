---
description: 'Funzione D3DXSHEvalConeLight (D3DX10.h): valuta una luce che è un cono di intensità costante e restituisce dati sferici sferici(SH).'
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: Funzione D3DXSHEvalConeLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fc11e7bab4cbbd6c8a685b289d4bde476cd465ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108609"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a><span data-ttu-id="2d8a1-103">Funzione D3DXSHEvalConeLight (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="2d8a1-103">D3DXSHEvalConeLight function (D3DX10.h)</span></span>

<span data-ttu-id="2d8a1-104">Valuta una luce che è un cono di intensità costante e restituisce dati sferici sferici armonici (SH).</span><span class="sxs-lookup"><span data-stu-id="2d8a1-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8a1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d8a1-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="2d8a1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d8a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d8a1-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d8a1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d8a1-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-109">Order of the SH evaluation.</span></span> <span data-ttu-id="2d8a1-110">Deve essere compreso nell'intervallo da D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2d8a1-111">La valutazione genera coefficienti Di ordine.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2d8a1-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-113">*pDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d8a1-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2d8a1-115">Puntatore al vettore di direzione dell'asse dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base sh.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="2d8a1-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-117">*Raggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-118">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d8a1-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d8a1-119">Raggio del cono in radianti.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-120">*RIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d8a1-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d8a1-122">Intensità rossa della luce.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-123">*GIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d8a1-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d8a1-125">Intensità verde della luce.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-126">*BIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d8a1-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d8a1-128">Intensità blu della luce.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-129">*pROut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-129">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d8a1-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d8a1-131">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-132">*pGOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-132">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d8a1-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d8a1-134">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="2d8a1-135">*pBOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d8a1-135">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8a1-136">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d8a1-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d8a1-137">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d8a1-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d8a1-138">Return value</span></span>

<span data-ttu-id="2d8a1-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d8a1-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d8a1-140">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d8a1-141">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8a1-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d8a1-142">Remarks</span></span>

<span data-ttu-id="2d8a1-143">Valuta una luce che è un cono di intensità costante e restituisce dati SH spettrali.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="2d8a1-144">Il vettore di output viene calcolato in modo che se il rapporto di intensità R/G/B è uguale a 1, la luminosità di uscita di un punto direttamente sotto la luce (orientata nella direzione del cono su un oggetto diffuso con albedo pari a 1) sarà 1,0.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="2d8a1-145">Verranno calcolati tre esempi spettrali. Verrà restituito pROut, mentre pGOut e pBOut possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-145">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="2d8a1-146">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con theta, l'angolo circa l'asse z nella direzione destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="2d8a1-148">Le equazioni seguenti mostrano la relazione tra coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="2d8a1-149">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="2d8a1-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="2d8a1-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d8a1-151">Requirements</span></span>



| <span data-ttu-id="2d8a1-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d8a1-152">Requirement</span></span> | <span data-ttu-id="2d8a1-153">Valore</span><span class="sxs-lookup"><span data-stu-id="2d8a1-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8a1-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d8a1-154">Header</span></span><br/>  | <dl> <span data-ttu-id="2d8a1-155"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2d8a1-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d8a1-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d8a1-156">Library</span></span><br/> | <dl> <span data-ttu-id="2d8a1-157"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d8a1-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d8a1-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d8a1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d8a1-159">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2d8a1-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
