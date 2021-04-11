---
description: Definisce un set di proprietà di illuminazione.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Struttura D3DLIGHT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235073"
---
# <a name="d3dlight9-structure"></a><span data-ttu-id="90172-103">Struttura D3DLIGHT9</span><span class="sxs-lookup"><span data-stu-id="90172-103">D3DLIGHT9 structure</span></span>

<span data-ttu-id="90172-104">Definisce un set di proprietà di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="90172-104">Defines a set of lighting properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90172-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90172-105">Syntax</span></span>


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a><span data-ttu-id="90172-106">Members</span><span class="sxs-lookup"><span data-stu-id="90172-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="90172-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="90172-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="90172-108">Tipo: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**</span><span class="sxs-lookup"><span data-stu-id="90172-108">Type: **[**D3DLIGHTTYPE**](./d3dlighttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90172-109">Tipo della sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="90172-109">Type of the light source.</span></span> <span data-ttu-id="90172-110">Questo valore è uno dei membri del tipo enumerato [**D3DLIGHTTYPE**](./d3dlighttype.md) .</span><span class="sxs-lookup"><span data-stu-id="90172-110">This value is one of the members of the [**D3DLIGHTTYPE**](./d3dlighttype.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="90172-111">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="90172-111">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="90172-112">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="90172-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90172-113">Colore diffuso emesso dalla luce.</span><span class="sxs-lookup"><span data-stu-id="90172-113">Diffuse color emitted by the light.</span></span> <span data-ttu-id="90172-114">Questo membro è una struttura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="90172-114">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90172-115">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="90172-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="90172-116">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="90172-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90172-117">Colore speculare emesso dalla luce.</span><span class="sxs-lookup"><span data-stu-id="90172-117">Specular color emitted by the light.</span></span> <span data-ttu-id="90172-118">Questo membro è una struttura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="90172-118">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90172-119">**Di ambiente**</span><span class="sxs-lookup"><span data-stu-id="90172-119">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="90172-120">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="90172-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90172-121">Colore di ambiente emesso dalla luce.</span><span class="sxs-lookup"><span data-stu-id="90172-121">Ambient color emitted by the light.</span></span> <span data-ttu-id="90172-122">Questo membro è una struttura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="90172-122">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90172-123">**Position**</span><span class="sxs-lookup"><span data-stu-id="90172-123">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="90172-124">Tipo: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="90172-124">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90172-125">Posizione della luce nello spazio globale, specificata da una struttura [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="90172-125">Position of the light in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="90172-126">Questo membro non ha significato per le luci direzionali e in questo caso viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="90172-126">This member has no meaning for directional lights and is ignored in that case.</span></span>

</dd> <dt>

<span data-ttu-id="90172-127">**Direzione**</span><span class="sxs-lookup"><span data-stu-id="90172-127">**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="90172-128">Tipo: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="90172-128">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90172-129">Direzione della luce che punta allo spazio globale, specificata da una struttura [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="90172-129">Direction that the light is pointing in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="90172-130">Questo membro ha un significato solo per direzionali e Spotlight.</span><span class="sxs-lookup"><span data-stu-id="90172-130">This member has meaning only for directional and spotlights.</span></span> <span data-ttu-id="90172-131">Non è necessario normalizzare questo vettore, ma deve avere una lunghezza diversa da zero.</span><span class="sxs-lookup"><span data-stu-id="90172-131">This vector need not be normalized, but it should have a nonzero length.</span></span>

</dd> <dt>

<span data-ttu-id="90172-132">**Range**</span><span class="sxs-lookup"><span data-stu-id="90172-132">**Range**</span></span>
</dt> <dd>

<span data-ttu-id="90172-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90172-133">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="90172-134">Distanza oltre la quale la luce non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="90172-134">Distance beyond which the light has no effect.</span></span> <span data-ttu-id="90172-135">Il valore massimo consentito per questo membro è la radice quadrata di FLT \_ max.</span><span class="sxs-lookup"><span data-stu-id="90172-135">The maximum allowable value for this member is the square root of FLT\_MAX.</span></span> <span data-ttu-id="90172-136">Questo membro non influisce sulle luci direzionali.</span><span class="sxs-lookup"><span data-stu-id="90172-136">This member does not affect directional lights.</span></span>

</dd> <dt>

<span data-ttu-id="90172-137">**Falloff**</span><span class="sxs-lookup"><span data-stu-id="90172-137">**Falloff**</span></span>
</dt> <dd>

<span data-ttu-id="90172-138">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90172-138">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="90172-139">Diminuisce l'illuminazione tra il cono interno di un punto di Spotlight (l'angolo specificato da Theta) e il bordo esterno del cono esterno (l'angolo specificato da Phi).</span><span class="sxs-lookup"><span data-stu-id="90172-139">Decrease in illumination between a spotlight's inner cone (the angle specified by Theta) and the outer edge of the outer cone (the angle specified by Phi).</span></span>

<span data-ttu-id="90172-140">L'effetto del decadimento sull'illuminazione è sottile.</span><span class="sxs-lookup"><span data-stu-id="90172-140">The effect of falloff on the lighting is subtle.</span></span> <span data-ttu-id="90172-141">Inoltre, una lieve riduzione delle prestazioni è dovuta al data shaping della curva di interruzione.</span><span class="sxs-lookup"><span data-stu-id="90172-141">Furthermore, a small performance penalty is incurred by shaping the falloff curve.</span></span> <span data-ttu-id="90172-142">Per questi motivi, la maggior parte degli sviluppatori imposta questo valore su 1,0.</span><span class="sxs-lookup"><span data-stu-id="90172-142">For these reasons, most developers set this value to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="90172-143">**Attenuation0**</span><span class="sxs-lookup"><span data-stu-id="90172-143">**Attenuation0**</span></span>
</dt> <dd>

<span data-ttu-id="90172-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90172-144">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="90172-145">Valore che specifica il modo in cui l'intensità di luce viene modificata rispetto alla distanza.</span><span class="sxs-lookup"><span data-stu-id="90172-145">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="90172-146">I valori di attenuazione vengono ignorati per le luci direzionali.</span><span class="sxs-lookup"><span data-stu-id="90172-146">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="90172-147">Questo membro rappresenta una costante di attenuazione.</span><span class="sxs-lookup"><span data-stu-id="90172-147">This member represents an attenuation constant.</span></span> <span data-ttu-id="90172-148">Per informazioni sull'attenuazione, vedere [Proprietà chiare (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="90172-148">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="90172-149">I valori validi per questo membro variano da 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="90172-149">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="90172-150">Per le luci non direzionali, tutti e tre i valori di attenuazione non devono essere impostati su 0,0 nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="90172-150">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="90172-151">**Attenuation1**</span><span class="sxs-lookup"><span data-stu-id="90172-151">**Attenuation1**</span></span>
</dt> <dd>

<span data-ttu-id="90172-152">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90172-152">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="90172-153">Valore che specifica il modo in cui l'intensità di luce viene modificata rispetto alla distanza.</span><span class="sxs-lookup"><span data-stu-id="90172-153">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="90172-154">I valori di attenuazione vengono ignorati per le luci direzionali.</span><span class="sxs-lookup"><span data-stu-id="90172-154">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="90172-155">Questo membro rappresenta una costante di attenuazione.</span><span class="sxs-lookup"><span data-stu-id="90172-155">This member represents an attenuation constant.</span></span> <span data-ttu-id="90172-156">Per informazioni sull'attenuazione, vedere [Proprietà chiare (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="90172-156">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="90172-157">I valori validi per questo membro variano da 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="90172-157">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="90172-158">Per le luci non direzionali, tutti e tre i valori di attenuazione non devono essere impostati su 0,0 nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="90172-158">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="90172-159">**Attenuation2**</span><span class="sxs-lookup"><span data-stu-id="90172-159">**Attenuation2**</span></span>
</dt> <dd>

<span data-ttu-id="90172-160">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90172-160">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="90172-161">Valore che specifica il modo in cui l'intensità di luce viene modificata rispetto alla distanza.</span><span class="sxs-lookup"><span data-stu-id="90172-161">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="90172-162">I valori di attenuazione vengono ignorati per le luci direzionali.</span><span class="sxs-lookup"><span data-stu-id="90172-162">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="90172-163">Questo membro rappresenta una costante di attenuazione.</span><span class="sxs-lookup"><span data-stu-id="90172-163">This member represents an attenuation constant.</span></span> <span data-ttu-id="90172-164">Per informazioni sull'attenuazione, vedere [Proprietà chiare (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="90172-164">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="90172-165">I valori validi per questo membro variano da 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="90172-165">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="90172-166">Per le luci non direzionali, tutti e tre i valori di attenuazione non devono essere impostati su 0,0 nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="90172-166">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="90172-167">**Theta**</span><span class="sxs-lookup"><span data-stu-id="90172-167">**Theta**</span></span>
</dt> <dd>

<span data-ttu-id="90172-168">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90172-168">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="90172-169">Angolo, in radianti, del cono interno di un Spotlight, ovvero il cono in evidenza completamente illuminato.</span><span class="sxs-lookup"><span data-stu-id="90172-169">Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone.</span></span> <span data-ttu-id="90172-170">Questo valore deve essere compreso nell'intervallo compreso tra 0 e il valore specificato da Phi.</span><span class="sxs-lookup"><span data-stu-id="90172-170">This value must be in the range from 0 through the value specified by Phi.</span></span>

</dd> <dt>

<span data-ttu-id="90172-171">**Phi**</span><span class="sxs-lookup"><span data-stu-id="90172-171">**Phi**</span></span>
</dt> <dd>

<span data-ttu-id="90172-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90172-172">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="90172-173">Angolo, in radianti, che definisce il bordo esterno del cono esterno del faretto.</span><span class="sxs-lookup"><span data-stu-id="90172-173">Angle, in radians, defining the outer edge of the spotlight's outer cone.</span></span> <span data-ttu-id="90172-174">I punti esterni a questo cono non sono illuminati dal faretto.</span><span class="sxs-lookup"><span data-stu-id="90172-174">Points outside this cone are not lit by the spotlight.</span></span> <span data-ttu-id="90172-175">Questo valore deve essere compreso tra 0 e pi.</span><span class="sxs-lookup"><span data-stu-id="90172-175">This value must be between 0 and pi.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90172-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90172-176">Requirements</span></span>



| <span data-ttu-id="90172-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="90172-177">Requirement</span></span> | <span data-ttu-id="90172-178">Valore</span><span class="sxs-lookup"><span data-stu-id="90172-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90172-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90172-179">Header</span></span><br/> | <dl> <span data-ttu-id="90172-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="90172-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90172-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90172-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90172-182">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="90172-182">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="90172-183">**Getlight**</span><span class="sxs-lookup"><span data-stu-id="90172-183">**GetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[<span data-ttu-id="90172-184">**Chiaro**</span><span class="sxs-lookup"><span data-stu-id="90172-184">**SetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
