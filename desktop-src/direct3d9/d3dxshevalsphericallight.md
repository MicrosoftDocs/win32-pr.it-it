---
description: Valuta una luce sferica e restituisce dati ad armonica sferica (SH).
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: Funzione D3DXSHEvalSphericalLight (D3dx9math. h)
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
ms.openlocfilehash: 8581b4284e270b6df587be1a71fcf11f29c843d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354619"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="c8051-103">Funzione D3DXSHEvalSphericalLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c8051-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="c8051-104">Valuta una luce sferica e restituisce dati ad armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="c8051-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8051-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8051-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c8051-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8051-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8051-107">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c8051-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8051-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8051-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="c8051-109">Order of the SH evaluation.</span></span> <span data-ttu-id="c8051-110">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="c8051-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c8051-111">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="c8051-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c8051-112">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="c8051-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-113">*PPO* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8051-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8051-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8051-115">Puntatore alla posizione chiara.</span><span class="sxs-lookup"><span data-stu-id="c8051-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-116">*Raggio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8051-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8051-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8051-118">Raggio della sorgente di luce sferica.</span><span class="sxs-lookup"><span data-stu-id="c8051-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-119">*RIntensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8051-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8051-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8051-121">Intensità rossa della luce.</span><span class="sxs-lookup"><span data-stu-id="c8051-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-122">*GIntensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8051-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8051-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8051-124">Intensità verde della luce.</span><span class="sxs-lookup"><span data-stu-id="c8051-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-125">*BIntensity* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8051-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8051-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8051-127">Intensità blu della luce.</span><span class="sxs-lookup"><span data-stu-id="c8051-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-128">*pROut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8051-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8051-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c8051-130">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="c8051-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-131">*pGOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8051-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-132">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8051-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c8051-133">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="c8051-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="c8051-134">*pBOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8051-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8051-135">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8051-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c8051-136">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="c8051-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8051-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8051-137">Return value</span></span>

<span data-ttu-id="c8051-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8051-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8051-139">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8051-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c8051-140">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c8051-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8051-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8051-141">Remarks</span></span>

<span data-ttu-id="c8051-142">Valuta una luce sferica e restituisce dati SH spettrali.</span><span class="sxs-lookup"><span data-stu-id="c8051-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="c8051-143">Non è prevista la normalizzazione dell'intensità della luce come per le [luci direzionali](light-types.md), quindi è necessario prestare attenzione quando si specificano le intensità.</span><span class="sxs-lookup"><span data-stu-id="c8051-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="c8051-144">Verrà calcolato tre campioni spettrali; viene restituito *pROut* , mentre *pGOut* e *pBOut* possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="c8051-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="c8051-145">Nella sfera con raggio di unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con Theta, l'angolo sull'asse z nella [direzione destra](coordinate-systems.md)e Phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="c8051-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unitario](images/spherical-coordinates.png)

<span data-ttu-id="c8051-147">Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, Phi) nella sfera dell'unità.</span><span class="sxs-lookup"><span data-stu-id="c8051-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="c8051-148">L'angolo theta varia nell'intervallo compreso tra 0 e 2 pi, mentre Phi varia da 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="c8051-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="c8051-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8051-150">Requirements</span></span>



| <span data-ttu-id="c8051-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8051-151">Requirement</span></span> | <span data-ttu-id="c8051-152">Valore</span><span class="sxs-lookup"><span data-stu-id="c8051-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8051-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8051-153">Header</span></span><br/>  | <dl> <span data-ttu-id="c8051-154"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8051-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8051-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="c8051-155">Library</span></span><br/> | <dl> <span data-ttu-id="c8051-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8051-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8051-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8051-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8051-158">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="c8051-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c8051-159">Trasferimento Radiance pre-calcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c8051-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
