---
description: 'Funzione D3DXSHEvalConeLight (D3dx9math.h): valuta una luce che è un cono di intensità costante e restituisce dati sferici armonici sferici (SH).'
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: Funzione D3DXSHEvalConeLight (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31c90e705a0bb4e82813fff42673e143c5acf171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117949"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a><span data-ttu-id="3da01-103">Funzione D3DXSHEvalConeLight (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="3da01-103">D3DXSHEvalConeLight function (D3dx9math.h)</span></span>

<span data-ttu-id="3da01-104">Valuta una luce che è un cono di intensità costante e restituisce dati sferici sferici armonici (SH).</span><span class="sxs-lookup"><span data-stu-id="3da01-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3da01-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="3da01-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3da01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da01-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3da01-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3da01-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3da01-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="3da01-109">Order of the SH evaluation.</span></span> <span data-ttu-id="3da01-110">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="3da01-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3da01-111">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="3da01-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3da01-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="3da01-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-113">*pDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3da01-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3da01-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3da01-115">Puntatore al vettore di direzione dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base SH.</span><span class="sxs-lookup"><span data-stu-id="3da01-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="3da01-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3da01-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-117">*Raggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3da01-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-118">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3da01-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3da01-119">Raggio del cono in radianti.</span><span class="sxs-lookup"><span data-stu-id="3da01-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-120">*RIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3da01-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3da01-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3da01-122">Intensità rossa della luce.</span><span class="sxs-lookup"><span data-stu-id="3da01-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-123">*GIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3da01-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3da01-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3da01-125">Intensità verde della luce.</span><span class="sxs-lookup"><span data-stu-id="3da01-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-126">*BIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3da01-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3da01-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3da01-128">Intensità blu della luce.</span><span class="sxs-lookup"><span data-stu-id="3da01-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-129">*pROut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3da01-129">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3da01-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3da01-131">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="3da01-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-132">*pGOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3da01-132">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3da01-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3da01-134">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="3da01-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="3da01-135">*pBOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3da01-135">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da01-136">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3da01-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3da01-137">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="3da01-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da01-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3da01-138">Return value</span></span>

<span data-ttu-id="3da01-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3da01-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3da01-140">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3da01-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3da01-141">Se la funzione ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3da01-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3da01-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="3da01-142">Remarks</span></span>

<span data-ttu-id="3da01-143">Valuta una luce che è un cono di intensità costante e restituisce dati SH spettrale.</span><span class="sxs-lookup"><span data-stu-id="3da01-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="3da01-144">Il vettore di output viene calcolato in modo che se il rapporto di intensità R/G/B è uguale a 1, la luminosità di uscita di un punto direttamente sotto la luce (orientata nella direzione del cono su un oggetto diffuso con albedo pari a 1) sarebbe 1,0.</span><span class="sxs-lookup"><span data-stu-id="3da01-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="3da01-145">Verranno calcolati tre esempi spettrale. *Verrà restituito pROut,* mentre *pGOut* e *pBOut* possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="3da01-145">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="3da01-146">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente [](coordinate-systems.md)con theta, l'angolo sull'asse z nella direzione destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="3da01-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="3da01-148">Le equazioni seguenti mostrano la relazione tra coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="3da01-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="3da01-149">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="3da01-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="3da01-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3da01-151">Requirements</span></span>



| <span data-ttu-id="3da01-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da01-152">Requirement</span></span> | <span data-ttu-id="3da01-153">Valore</span><span class="sxs-lookup"><span data-stu-id="3da01-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3da01-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3da01-154">Header</span></span><br/>  | <dl> <span data-ttu-id="3da01-155"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3da01-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3da01-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="3da01-156">Library</span></span><br/> | <dl> <span data-ttu-id="3da01-157"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3da01-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3da01-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3da01-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da01-159">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="3da01-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3da01-160">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3da01-160">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
