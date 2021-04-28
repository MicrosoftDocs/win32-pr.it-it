---
description: 'Funzione D3DXSHEvalSphericalLight (D3DX10.h): valuta una luce sferica e restituisce dati sferici sferici armonici (SH).'
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: Funzione D3DXSHEvalSphericalLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1e509ea4695f143bd5399cbda004bcba53f514c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108559"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a><span data-ttu-id="5e688-103">Funzione D3DXSHEvalSphericalLight (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="5e688-103">D3DXSHEvalSphericalLight function (D3DX10.h)</span></span>

<span data-ttu-id="5e688-104">Valuta una luce sferica e restituisce dati sferici sferici armonici (SH).</span><span class="sxs-lookup"><span data-stu-id="5e688-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e688-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e688-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="5e688-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e688-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e688-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e688-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e688-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="5e688-109">Order of the SH evaluation.</span></span> <span data-ttu-id="5e688-110">Deve essere compreso nell'intervallo tra D3DXSH \_ MINORDER e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="5e688-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5e688-111">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="5e688-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5e688-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="5e688-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-113">*pPos* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e688-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5e688-115">Puntatore alla posizione della luce.</span><span class="sxs-lookup"><span data-stu-id="5e688-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-116">*Raggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e688-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e688-118">Raggio della sorgente di luce sferica.</span><span class="sxs-lookup"><span data-stu-id="5e688-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-119">*RIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e688-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e688-121">Intensità rossa della luce.</span><span class="sxs-lookup"><span data-stu-id="5e688-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-122">*GIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e688-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e688-124">Intensità verde della luce.</span><span class="sxs-lookup"><span data-stu-id="5e688-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-125">*BIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e688-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e688-127">Intensità blu della luce.</span><span class="sxs-lookup"><span data-stu-id="5e688-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-128">*pROut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-128">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e688-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5e688-130">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="5e688-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-131">*pGOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-131">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-132">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e688-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5e688-133">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="5e688-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="5e688-134">*pBOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e688-134">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e688-135">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e688-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5e688-136">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="5e688-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e688-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e688-137">Return value</span></span>

<span data-ttu-id="5e688-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e688-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e688-139">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5e688-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5e688-140">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5e688-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e688-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e688-141">Remarks</span></span>

<span data-ttu-id="5e688-142">Valuta una luce sferica e restituisce dati SH spretrali.</span><span class="sxs-lookup"><span data-stu-id="5e688-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="5e688-143">Non esiste alcuna normalizzazione dell'intensità della luce come per le luci direzionali, quindi è necessario fare attenzione quando si specifica l'intensità.</span><span class="sxs-lookup"><span data-stu-id="5e688-143">There is no normalization of the intensity of the light like there is for directional lights, so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="5e688-144">Verranno calcolati tre esempi spettrali. Verrà restituito pROut, mentre pGOut e pBOut possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="5e688-144">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="5e688-145">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con theta, l'angolo sull'asse z nella direzione destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="5e688-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="5e688-147">Le equazioni seguenti mostrano la relazione tra coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="5e688-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="5e688-148">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="5e688-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="5e688-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e688-150">Requirements</span></span>



| <span data-ttu-id="5e688-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e688-151">Requirement</span></span> | <span data-ttu-id="5e688-152">Valore</span><span class="sxs-lookup"><span data-stu-id="5e688-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e688-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e688-153">Header</span></span><br/>  | <dl> <span data-ttu-id="5e688-154"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="5e688-154"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e688-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e688-155">Library</span></span><br/> | <dl> <span data-ttu-id="5e688-156"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e688-156"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e688-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e688-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e688-158">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5e688-158">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
