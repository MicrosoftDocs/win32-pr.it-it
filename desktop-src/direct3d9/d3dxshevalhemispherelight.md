---
description: "Funzione D3DXSHEvalHemisphereLight (D3dx9math.h): valuta una luce che è un'interpolazione lineare tra due colori sulla sfera."
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: Funzione D3DXSHEvalHemisphereLight (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc06dcf866c21cc5dcb96b23dea5a4640293fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093967"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a><span data-ttu-id="1ec39-103">Funzione D3DXSHEvalHemisphereLight (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1ec39-103">D3DXSHEvalHemisphereLight function (D3dx9math.h)</span></span>

<span data-ttu-id="1ec39-104">Valuta una luce che è un'interpolazione lineare tra due colori sulla sfera.</span><span class="sxs-lookup"><span data-stu-id="1ec39-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ec39-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1ec39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ec39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec39-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ec39-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec39-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ec39-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ec39-109">Ordine della valutazione armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="1ec39-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="1ec39-110">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="1ec39-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1ec39-111">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="1ec39-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1ec39-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="1ec39-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1ec39-113">*pDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ec39-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec39-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ec39-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ec39-115">Puntatore al vettore di direzione dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base sh.</span><span class="sxs-lookup"><span data-stu-id="1ec39-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="1ec39-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1ec39-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1ec39-117">*In alto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ec39-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec39-118">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1ec39-118">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="1ec39-119">Colore del cielo.</span><span class="sxs-lookup"><span data-stu-id="1ec39-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="1ec39-120">*In basso* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ec39-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec39-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1ec39-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="1ec39-122">Colore del suolo.</span><span class="sxs-lookup"><span data-stu-id="1ec39-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="1ec39-123">*pROut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ec39-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec39-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ec39-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1ec39-125">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="1ec39-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="1ec39-126">*pGOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ec39-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec39-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ec39-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1ec39-128">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="1ec39-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="1ec39-129">*pBOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ec39-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec39-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ec39-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1ec39-131">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="1ec39-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec39-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ec39-132">Return value</span></span>

<span data-ttu-id="1ec39-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ec39-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ec39-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ec39-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ec39-135">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1ec39-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec39-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ec39-136">Remarks</span></span>

<span data-ttu-id="1ec39-137">L'interpolazione viene eseguita in modo lineare tra i due punti, non sulla superficie della sfera ,ovvero se l'asse è (0,0,1) è lineare in Z, non nell'angolo azimutabile.</span><span class="sxs-lookup"><span data-stu-id="1ec39-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="1ec39-138">La funzione di illuminazione sferica risultante viene normalizzata in modo che un punto su una superficie perfettamente diffusa senza ombreggiatura e un normale puntato nella direzione *pDir* comporterebbe la luminosità di uscita con un valore pari a 1 (se il colore superiore era bianco e il colore inferiore era nero).</span><span class="sxs-lookup"><span data-stu-id="1ec39-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction *pDir* would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="1ec39-139">Si tratta di un modello molto semplice in cui *Top* rappresenta l'intensità del "cielo" e *Bottom* rappresenta l'intensità del "terreno".</span><span class="sxs-lookup"><span data-stu-id="1ec39-139">This is a very simple model where *Top* represents the intensity of the "sky" and *Bottom* represents the intensity of the "ground."</span></span>

<span data-ttu-id="1ec39-140">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente [](coordinate-systems.md)con theta, l'angolo sull'asse z nella direzione a destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="1ec39-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="1ec39-142">Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="1ec39-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="1ec39-143">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="1ec39-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="1ec39-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ec39-145">Requirements</span></span>



| <span data-ttu-id="1ec39-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec39-146">Requirement</span></span> | <span data-ttu-id="1ec39-147">Valore</span><span class="sxs-lookup"><span data-stu-id="1ec39-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec39-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ec39-148">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec39-149"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec39-149"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1ec39-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ec39-150">Library</span></span><br/> | <dl> <span data-ttu-id="1ec39-151"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ec39-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ec39-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ec39-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec39-153">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1ec39-153">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1ec39-154">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1ec39-154">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
