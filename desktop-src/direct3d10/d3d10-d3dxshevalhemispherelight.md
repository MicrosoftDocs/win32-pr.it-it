---
description: "Funzione D3DXSHEvalHemisphereLight (D3DX10.h): valuta una luce che è un'interpolazione lineare tra due colori sulla sfera."
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Funzione D3DXSHEvalHemisphereLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 355dae7b843d5acfbb842b7bd08c329bdaed4306
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108569"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a><span data-ttu-id="83125-103">Funzione D3DXSHEvalHemisphereLight (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="83125-103">D3DXSHEvalHemisphereLight function (D3DX10.h)</span></span>

<span data-ttu-id="83125-104">Valuta una luce che è un'interpolazione lineare tra due colori sulla sfera.</span><span class="sxs-lookup"><span data-stu-id="83125-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="83125-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83125-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="83125-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83125-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83125-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83125-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83125-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83125-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83125-109">Ordine della valutazione sferica aricale (SH).</span><span class="sxs-lookup"><span data-stu-id="83125-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="83125-110">Deve essere compreso nell'intervallo da D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="83125-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="83125-111">La valutazione genera coefficienti Di ordine.</span><span class="sxs-lookup"><span data-stu-id="83125-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="83125-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="83125-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="83125-113">*pDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83125-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83125-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="83125-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="83125-115">Puntatore al vettore di direzione dell'asse dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base sh.</span><span class="sxs-lookup"><span data-stu-id="83125-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="83125-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="83125-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="83125-117">*In alto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83125-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83125-118">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="83125-118">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="83125-119">Colore del cielo.</span><span class="sxs-lookup"><span data-stu-id="83125-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="83125-120">*In basso* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83125-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83125-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="83125-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="83125-122">Colore del terreno.</span><span class="sxs-lookup"><span data-stu-id="83125-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="83125-123">*pROut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83125-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83125-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83125-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83125-125">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="83125-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="83125-126">*pGOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83125-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83125-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83125-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83125-128">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="83125-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="83125-129">*pBOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83125-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83125-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83125-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83125-131">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="83125-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83125-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83125-132">Return value</span></span>

<span data-ttu-id="83125-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83125-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83125-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83125-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83125-135">Se la funzione ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="83125-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="83125-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="83125-136">Remarks</span></span>

<span data-ttu-id="83125-137">L'interpolazione viene eseguita in modo lineare tra i due punti, non sulla superficie della sfera ,ovvero se l'asse è (0,0,1) è lineare in Z, non nell'angolo azimuthal.</span><span class="sxs-lookup"><span data-stu-id="83125-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="83125-138">La funzione di illuminazione sferica risultante viene normalizzata in modo che un punto su una superficie perfettamente diffusa senza ombreggiatura e un normale puntato nella direzione pDir comporterebbe una luminosità di uscita con valore 1 (se il colore superiore era bianco e il colore inferiore era nero).</span><span class="sxs-lookup"><span data-stu-id="83125-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction pDir would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="83125-139">Si tratta di un modello molto semplice in cui Top rappresenta l'intensità del "cielo" e Bottom rappresenta l'intensità del "terreno".</span><span class="sxs-lookup"><span data-stu-id="83125-139">This is a very simple model where Top represents the intensity of the "sky" and Bottom represents the intensity of the "ground."</span></span>

<span data-ttu-id="83125-140">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con theta, l'angolo circa l'asse z nella direzione destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="83125-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="83125-142">Le equazioni seguenti mostrano la relazione tra coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="83125-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="83125-143">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="83125-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="83125-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83125-145">Requirements</span></span>



| <span data-ttu-id="83125-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="83125-146">Requirement</span></span> | <span data-ttu-id="83125-147">Valore</span><span class="sxs-lookup"><span data-stu-id="83125-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83125-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83125-148">Header</span></span><br/>  | <dl> <span data-ttu-id="83125-149"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="83125-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="83125-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="83125-150">Library</span></span><br/> | <dl> <span data-ttu-id="83125-151"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="83125-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83125-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83125-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83125-153">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="83125-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
