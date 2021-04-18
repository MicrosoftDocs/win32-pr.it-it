---
description: Caratteristiche del materiale PRT (pre-Computed Radiance Transfer) di sfericità (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Struttura D3DXSHMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322592"
---
# <a name="d3dxshmaterial-structure"></a><span data-ttu-id="2d087-103">Struttura D3DXSHMATERIAL</span><span class="sxs-lookup"><span data-stu-id="2d087-103">D3DXSHMATERIAL structure</span></span>

<span data-ttu-id="2d087-104">Caratteristiche del materiale PRT (pre-Computed Radiance Transfer) di sfericità (SH).</span><span class="sxs-lookup"><span data-stu-id="2d087-104">Spherical harmonic (SH) precomputed radiance transfer (PRT) material characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d087-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d087-105">Syntax</span></span>


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a><span data-ttu-id="2d087-106">Members</span><span class="sxs-lookup"><span data-stu-id="2d087-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2d087-107">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="2d087-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="2d087-108">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="2d087-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d087-109">Diffonde l'albedo della superficie.</span><span class="sxs-lookup"><span data-stu-id="2d087-109">Diffuse albedo of the surface.</span></span> <span data-ttu-id="2d087-110">Questo valore viene ignorato se l'oggetto è un mirror.</span><span class="sxs-lookup"><span data-stu-id="2d087-110">This value is ignored if the object is a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="2d087-111">**bMirror**</span><span class="sxs-lookup"><span data-stu-id="2d087-111">**bMirror**</span></span>
</dt> <dd>

<span data-ttu-id="2d087-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d087-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d087-113">Deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="2d087-113">Must be set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2d087-114">**bSubSurf**</span><span class="sxs-lookup"><span data-stu-id="2d087-114">**bSubSurf**</span></span>
</dt> <dd>

<span data-ttu-id="2d087-115">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d087-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d087-116">Impostare su **true** per abilitare la dispersione della sottosuperficie; qualsiasi oggetto che esegue la dispersione della sottosuperficie non può essere un mirror.</span><span class="sxs-lookup"><span data-stu-id="2d087-116">Set to **TRUE** to enable subsurface scattering; any object that does subsurface scattering cannot be a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="2d087-117">**RelativeIndexOfRefraction**</span><span class="sxs-lookup"><span data-stu-id="2d087-117">**RelativeIndexOfRefraction**</span></span>
</dt> <dd>

<span data-ttu-id="2d087-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d087-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d087-119">L'indice relativo della rifrazione è il rapporto tra due indici assoluti di rifrazione.</span><span class="sxs-lookup"><span data-stu-id="2d087-119">Relative index of refraction is the ratio between two absolute indexes of refraction.</span></span> <span data-ttu-id="2d087-120">Un indice di rifrazione è il rapporto tra il seno dell'angolo di incidenza e il seno dell'angolo di rifrazione.</span><span class="sxs-lookup"><span data-stu-id="2d087-120">An index of refraction is the ratio of the sine of the angle of incidence to the sine of the angle of refraction.</span></span>

</dd> <dt>

<span data-ttu-id="2d087-121">**Assorbimento**</span><span class="sxs-lookup"><span data-stu-id="2d087-121">**Absorption**</span></span>
</dt> <dd>

<span data-ttu-id="2d087-122">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="2d087-122">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d087-123">Il coefficiente di assorbimento è un parametro dell'equazione di rendering del volume utilizzato per modellare la propagazione leggera in un supporto partecipante.</span><span class="sxs-lookup"><span data-stu-id="2d087-123">The absorption coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> <dt>

<span data-ttu-id="2d087-124">**ReducedScattering**</span><span class="sxs-lookup"><span data-stu-id="2d087-124">**ReducedScattering**</span></span>
</dt> <dd>

<span data-ttu-id="2d087-125">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="2d087-125">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d087-126">Il coefficiente di dispersione ridotto è un parametro per l'equazione di rendering del volume utilizzato per modellare la propagazione leggera in un supporto partecipante.</span><span class="sxs-lookup"><span data-stu-id="2d087-126">The reduced scattering coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d087-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d087-127">Remarks</span></span>

<span data-ttu-id="2d087-128">Le scene non spettrali usano il canale rosso dai materiali anziché il valore della luminanza.</span><span class="sxs-lookup"><span data-stu-id="2d087-128">Non-spectral scenes use the red channel from the materials instead of the luminance value.</span></span>

<span data-ttu-id="2d087-129">Per ulteriori informazioni su PRT, vedere:</span><span class="sxs-lookup"><span data-stu-id="2d087-129">For more information about PRT see:</span></span>

-   <span data-ttu-id="2d087-130">Procedura di Jensen, Henrik Wann, et al. Siggraph: modello pratico per il trasporto leggero della sottosuperficie, 2001.</span><span class="sxs-lookup"><span data-stu-id="2d087-130">Jensen, Henrik Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d087-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d087-131">Requirements</span></span>



| <span data-ttu-id="2d087-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d087-132">Requirement</span></span> | <span data-ttu-id="2d087-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2d087-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d087-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d087-134">Header</span></span><br/> | <dl> <span data-ttu-id="2d087-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d087-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d087-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d087-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d087-137">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="2d087-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
