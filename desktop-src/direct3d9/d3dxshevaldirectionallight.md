---
description: 'Funzione D3DXSHEvalDirectionalLight (D3dx9math.h): valuta una luce direzionale e restituisce dati sferici (SH).'
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: Funzione D3DXSHEvalDirectionalLight (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488682eca230c8da6cc5048aded4a7a1e7f71bfd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117909"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a><span data-ttu-id="7af06-103">Funzione D3DXSHEvalDirectionalLight (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="7af06-103">D3DXSHEvalDirectionalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="7af06-104">Valuta una [luce direzionale e](light-types.md) restituisce dati sferici sferici aricali (SH).</span><span class="sxs-lookup"><span data-stu-id="7af06-104">Evaluates a [directional light](light-types.md) and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7af06-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="7af06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7af06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af06-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7af06-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7af06-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7af06-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="7af06-109">Order of the SH evaluation.</span></span> <span data-ttu-id="7af06-110">Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="7af06-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="7af06-111">La valutazione genera coefficienti Di ordine.</span><span class="sxs-lookup"><span data-stu-id="7af06-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="7af06-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="7af06-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="7af06-113">*pDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7af06-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7af06-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7af06-115">Puntatore al vettore di direzione dell'asse dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base sh.</span><span class="sxs-lookup"><span data-stu-id="7af06-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="7af06-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7af06-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7af06-117">*RIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7af06-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-118">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7af06-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7af06-119">Intensità rossa della luce.</span><span class="sxs-lookup"><span data-stu-id="7af06-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="7af06-120">*GIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7af06-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7af06-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7af06-122">Intensità verde della luce.</span><span class="sxs-lookup"><span data-stu-id="7af06-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="7af06-123">*BIntensity* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7af06-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7af06-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7af06-125">Intensità blu della luce.</span><span class="sxs-lookup"><span data-stu-id="7af06-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="7af06-126">*pROut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="7af06-126">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7af06-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7af06-128">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="7af06-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="7af06-129">*pGOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="7af06-129">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7af06-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7af06-131">Puntatore facoltativo al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="7af06-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="7af06-132">*pBOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="7af06-132">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7af06-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7af06-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7af06-134">Puntatore facoltativo al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="7af06-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af06-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7af06-135">Return value</span></span>

<span data-ttu-id="7af06-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7af06-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7af06-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7af06-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7af06-138">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7af06-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af06-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="7af06-139">Remarks</span></span>

<span data-ttu-id="7af06-140">Il vettore di output viene calcolato in modo che se il rapporto di intensità R/G/B è uguale a 1, la luminosità di uscita risultante di un punto direttamente sotto la luce su un oggetto diffuso con un albedo pari a 1 sarebbe 1,0.</span><span class="sxs-lookup"><span data-stu-id="7af06-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="7af06-141">Verranno calcolati tre esempi spettrale. *Verrà restituito pROut,* mentre *pGOut* e *pBOut* possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="7af06-141">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="7af06-142">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente [](coordinate-systems.md)con theta, l'angolo sull'asse z nella direzione destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="7af06-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="7af06-144">Le equazioni seguenti mostrano la relazione tra coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="7af06-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="7af06-145">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="7af06-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="7af06-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7af06-147">Requirements</span></span>



| <span data-ttu-id="7af06-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="7af06-148">Requirement</span></span> | <span data-ttu-id="7af06-149">Valore</span><span class="sxs-lookup"><span data-stu-id="7af06-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7af06-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7af06-150">Header</span></span><br/>  | <dl> <span data-ttu-id="7af06-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7af06-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7af06-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="7af06-152">Library</span></span><br/> | <dl> <span data-ttu-id="7af06-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7af06-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7af06-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7af06-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af06-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7af06-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7af06-156">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7af06-156">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
