---
description: 'Funzione D3DXSHEvalSphericalLight (D3dx9math.h): valuta una luce sferica e restituisce dati sferici armonici sferici (SH).'
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: Funzione D3DXSHEvalSphericalLight (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db671d58806d999e07b1aac1e8e4da2fb38acc6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117889"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="67895-103">Funzione D3DXSHEvalSphericalLight (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="67895-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="67895-104">Valuta una luce sferica e restituisce dati sferici sferici armonici (SH).</span><span class="sxs-lookup"><span data-stu-id="67895-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="67895-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67895-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="67895-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="67895-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67895-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="67895-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67895-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67895-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="67895-109">Order of the SH evaluation.</span></span> <span data-ttu-id="67895-110">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="67895-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="67895-111">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="67895-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="67895-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="67895-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="67895-113">*pPos* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="67895-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="67895-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="67895-115">Puntatore alla posizione della luce.</span><span class="sxs-lookup"><span data-stu-id="67895-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="67895-116">*Raggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="67895-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67895-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67895-118">Raggio della sorgente di luce sferica.</span><span class="sxs-lookup"><span data-stu-id="67895-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="67895-119">*RIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="67895-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67895-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67895-121">Intensità rossa della luce.</span><span class="sxs-lookup"><span data-stu-id="67895-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="67895-122">*GIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="67895-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67895-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67895-124">Intensità verde della luce.</span><span class="sxs-lookup"><span data-stu-id="67895-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="67895-125">*BIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="67895-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67895-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67895-127">Intensità blu della luce.</span><span class="sxs-lookup"><span data-stu-id="67895-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="67895-128">*pROut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="67895-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="67895-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67895-130">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="67895-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="67895-131">*pGOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="67895-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-132">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="67895-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67895-133">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="67895-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="67895-134">*pBOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="67895-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67895-135">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="67895-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67895-136">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="67895-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67895-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67895-137">Return value</span></span>

<span data-ttu-id="67895-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67895-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67895-139">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67895-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="67895-140">Se la funzione ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="67895-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="67895-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="67895-141">Remarks</span></span>

<span data-ttu-id="67895-142">Valuta una luce sferica e restituisce dati SH spettrale.</span><span class="sxs-lookup"><span data-stu-id="67895-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="67895-143">Non esiste alcuna normalizzazione dell'intensità della [](light-types.md)luce come per le luci direzionali, quindi è necessario fare attenzione quando si specificano le intensità.</span><span class="sxs-lookup"><span data-stu-id="67895-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="67895-144">Verranno calcolati tre esempi spettrale. *Verrà restituito pROut,* mentre *pGOut* e *pBOut* possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="67895-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="67895-145">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente [](coordinate-systems.md)con theta, l'angolo sull'asse z nella direzione destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="67895-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="67895-147">Le equazioni seguenti mostrano la relazione tra coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="67895-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="67895-148">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="67895-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="67895-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67895-150">Requirements</span></span>



| <span data-ttu-id="67895-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="67895-151">Requirement</span></span> | <span data-ttu-id="67895-152">Valore</span><span class="sxs-lookup"><span data-stu-id="67895-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67895-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67895-153">Header</span></span><br/>  | <dl> <span data-ttu-id="67895-154"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="67895-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="67895-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="67895-155">Library</span></span><br/> | <dl> <span data-ttu-id="67895-156"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="67895-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67895-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67895-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67895-158">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="67895-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="67895-159">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="67895-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
