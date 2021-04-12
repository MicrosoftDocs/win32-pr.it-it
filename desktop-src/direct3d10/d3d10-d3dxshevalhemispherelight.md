---
description: Valuta una luce che rappresenta un'interpolazione lineare tra due colori sulla sfera.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Funzione D3DXSHEvalHemisphereLight (D3DX10. h)
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
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355324"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a><span data-ttu-id="d7305-103">Funzione D3DXSHEvalHemisphereLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d7305-103">D3DXSHEvalHemisphereLight function (D3DX10.h)</span></span>

<span data-ttu-id="d7305-104">Valuta una luce che rappresenta un'interpolazione lineare tra due colori sulla sfera.</span><span class="sxs-lookup"><span data-stu-id="d7305-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7305-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7305-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d7305-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7305-107">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d7305-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7305-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7305-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7305-109">Ordine della valutazione dell'armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="d7305-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="d7305-110">Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="d7305-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d7305-111">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="d7305-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d7305-112">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="d7305-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d7305-113">*pDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7305-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7305-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d7305-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d7305-115">Puntatore al vettore di direzione dell'asse del (x, y, z) in cui valutare le funzioni di base SH.</span><span class="sxs-lookup"><span data-stu-id="d7305-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="d7305-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d7305-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d7305-117">In *alto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7305-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7305-118">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="d7305-118">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="d7305-119">Colore celeste.</span><span class="sxs-lookup"><span data-stu-id="d7305-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="d7305-120">In *basso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7305-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7305-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="d7305-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="d7305-122">Colore di base.</span><span class="sxs-lookup"><span data-stu-id="d7305-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="d7305-123">*pROut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7305-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7305-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7305-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d7305-125">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="d7305-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="d7305-126">*pGOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7305-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7305-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7305-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d7305-128">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="d7305-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="d7305-129">*pBOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7305-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7305-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7305-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d7305-131">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="d7305-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7305-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7305-132">Return value</span></span>

<span data-ttu-id="d7305-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7305-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7305-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d7305-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d7305-135">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d7305-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7305-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7305-136">Remarks</span></span>

<span data-ttu-id="d7305-137">L'interpolazione viene eseguita in modo lineare tra i due punti, non sulla superficie della sfera (ovvero se l'asse è (0, 0, 1) è lineare in Z, non nell'angolo azimutale).</span><span class="sxs-lookup"><span data-stu-id="d7305-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="d7305-138">La funzione di illuminazione sferica risultante viene normalizzata in modo che un punto su una superficie perfettamente diffusa senza ombreggiatura e un normale punto nella direzione pDir comporti la radianza di uscita con un valore pari a 1 (se il colore superiore era bianco e il colore inferiore era nero).</span><span class="sxs-lookup"><span data-stu-id="d7305-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction pDir would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="d7305-139">Si tratta di un modello molto semplice in cui top rappresenta l'intensità del "cielo" e della parte inferiore rappresenta l'intensità della "superficie".</span><span class="sxs-lookup"><span data-stu-id="d7305-139">This is a very simple model where Top represents the intensity of the "sky" and Bottom represents the intensity of the "ground."</span></span>

<span data-ttu-id="d7305-140">Nella sfera con raggio di unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con Theta, l'angolo sull'asse z nella direzione destra e Phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="d7305-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unitario](images/spherical-coordinates.png)

<span data-ttu-id="d7305-142">Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, Phi) nella sfera dell'unità.</span><span class="sxs-lookup"><span data-stu-id="d7305-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="d7305-143">L'angolo theta varia nell'intervallo compreso tra 0 e 2 pi, mentre Phi varia da 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="d7305-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="d7305-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7305-145">Requirements</span></span>



| <span data-ttu-id="d7305-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7305-146">Requirement</span></span> | <span data-ttu-id="d7305-147">Valore</span><span class="sxs-lookup"><span data-stu-id="d7305-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7305-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7305-148">Header</span></span><br/>  | <dl> <span data-ttu-id="d7305-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7305-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7305-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7305-150">Library</span></span><br/> | <dl> <span data-ttu-id="d7305-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7305-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7305-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7305-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7305-153">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d7305-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
