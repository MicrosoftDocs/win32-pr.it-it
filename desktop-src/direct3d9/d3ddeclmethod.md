---
description: Definisce il metodo di dichiarazione vertex che è un'operazione predefinita eseguita da mosaico (o qualsiasi routine Geometry procedurale sui dati dei vertici durante la suddivisione a mosaico).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumerazione D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354384"
---
# <a name="d3ddeclmethod-enumeration"></a><span data-ttu-id="109f7-103">Enumerazione D3DDECLMETHOD</span><span class="sxs-lookup"><span data-stu-id="109f7-103">D3DDECLMETHOD enumeration</span></span>

<span data-ttu-id="109f7-104">Definisce il metodo di dichiarazione vertex che è un'operazione predefinita eseguita da mosaico (o qualsiasi routine Geometry procedurale sui dati dei vertici durante la suddivisione a mosaico).</span><span class="sxs-lookup"><span data-stu-id="109f7-104">Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).</span></span>

## <a name="syntax"></a><span data-ttu-id="109f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="109f7-105">Syntax</span></span>


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a><span data-ttu-id="109f7-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="109f7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="109f7-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**\_Impostazione predefinita D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="109f7-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="109f7-108">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="109f7-108">Default value.</span></span> <span data-ttu-id="109f7-109">Mosaico copia i dati dei vertici (dati spline per le patch) così come sono, senza calcoli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="109f7-109">The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations.</span></span> <span data-ttu-id="109f7-110">Quando si usa mosaico, questo elemento è interpolato.</span><span class="sxs-lookup"><span data-stu-id="109f7-110">When the tessellator is used, this element is interpolated.</span></span> <span data-ttu-id="109f7-111">In caso contrario, i dati dei vertici vengono copiati nel registro di input.</span><span class="sxs-lookup"><span data-stu-id="109f7-111">Otherwise vertex data is copied into the input register.</span></span> <span data-ttu-id="109f7-112">Il tipo di input e di output può essere qualsiasi valore, ma è sempre dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="109f7-112">The input and output type can be any value, but are always the same type.</span></span>

</dd> <dt>

<span data-ttu-id="109f7-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ parziali**</span><span class="sxs-lookup"><span data-stu-id="109f7-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD\_PARTIALU**</span></span>
</dt> <dd>

<span data-ttu-id="109f7-114">Calcola la tangente in un punto della patch rettangolo o triangolo nella direzione U.</span><span class="sxs-lookup"><span data-stu-id="109f7-114">Computes the tangent at a point on the rectangle or triangle patch in the U direction.</span></span> <span data-ttu-id="109f7-115">Il tipo di input può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="109f7-115">The input type can be one of the following:</span></span>

-   <span data-ttu-id="109f7-116">\_D3DCOLOR D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-116">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="109f7-117">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-117">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="109f7-118">\_Float4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-118">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="109f7-119">\_SHORT4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-119">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="109f7-120">\_UBYTE4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-120">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="109f7-121">Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="109f7-121">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="109f7-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**\_PARTIALV D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="109f7-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD\_PARTIALV**</span></span>
</dt> <dd>

<span data-ttu-id="109f7-123">Calcola la tangente in un punto della patch rettangolo o triangolo nella direzione V.</span><span class="sxs-lookup"><span data-stu-id="109f7-123">Computes the tangent at a point on the rectangle or triangle patch in the V direction.</span></span> <span data-ttu-id="109f7-124">Il tipo di input può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="109f7-124">The input type can be one of the following:</span></span>

-   <span data-ttu-id="109f7-125">\_D3DCOLOR D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-125">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="109f7-126">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-126">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="109f7-127">\_Float4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-127">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="109f7-128">\_SHORT4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-128">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="109f7-129">\_UBYTE4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-129">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="109f7-130">Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="109f7-130">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="109f7-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**\_CROSSUV D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="109f7-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD\_CROSSUV**</span></span>
</dt> <dd>

<span data-ttu-id="109f7-132">Calcola il normale in un punto della patch rettangolo o triangolo prendendo il prodotto incrociato di due tangenti.</span><span class="sxs-lookup"><span data-stu-id="109f7-132">Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents.</span></span> <span data-ttu-id="109f7-133">Il tipo di input può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="109f7-133">The input type can be one of the following:</span></span>

-   <span data-ttu-id="109f7-134">\_D3DCOLOR D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-134">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="109f7-135">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-135">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="109f7-136">\_Float4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-136">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="109f7-137">\_SHORT4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-137">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="109f7-138">\_UBYTE4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-138">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="109f7-139">Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="109f7-139">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="109f7-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**</span><span class="sxs-lookup"><span data-stu-id="109f7-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="109f7-141">Copiare i valori U, V in un punto della patch rettangolo o triangolo.</span><span class="sxs-lookup"><span data-stu-id="109f7-141">Copy out the U, V values at a point on the rectangle or triangle patch.</span></span> <span data-ttu-id="109f7-142">In questo modo si ottiene un valore float 2D.</span><span class="sxs-lookup"><span data-stu-id="109f7-142">This results in a 2D float.</span></span> <span data-ttu-id="109f7-143">Il tipo di input deve essere impostato su D3DDECLTYPE \_ inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="109f7-143">The input type must be set to D3DDECLTYPE\_UNUSED.</span></span> <span data-ttu-id="109f7-144">Il tipo di dati di output è sempre D3DDECLTYPE \_ FLOAT2.</span><span class="sxs-lookup"><span data-stu-id="109f7-144">The output data type is always D3DDECLTYPE\_FLOAT2.</span></span> <span data-ttu-id="109f7-145">Anche il flusso di input e l'offset sono inutilizzati (ma devono essere impostati su 0).</span><span class="sxs-lookup"><span data-stu-id="109f7-145">The input stream and offset are also unused (but must be set to 0).</span></span>

</dd> <dt>

<span data-ttu-id="109f7-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**\_Ricerca D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="109f7-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD\_LOOKUP**</span></span>
</dt> <dd>

<span data-ttu-id="109f7-147">Cercare una mappa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="109f7-147">Look up a displacement map.</span></span> <span data-ttu-id="109f7-148">Il tipo di input può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="109f7-148">The input type can be one of the following:</span></span>

-   <span data-ttu-id="109f7-149">\_FLOAT2 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-149">D3DDECLTYPE\_FLOAT2</span></span>
-   <span data-ttu-id="109f7-150">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-150">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="109f7-151">\_Float4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="109f7-151">D3DDECLTYPE\_FLOAT4</span></span>

<span data-ttu-id="109f7-152">Solo i componenti con estensione x e y vengono usati per la ricerca della mappa di trama.</span><span class="sxs-lookup"><span data-stu-id="109f7-152">Only the .x and .y components are used for the texture map lookup.</span></span> <span data-ttu-id="109f7-153">Il tipo di output è sempre D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="109f7-153">The output type is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="109f7-154">Il dispositivo deve supportare il mapping di spostamento.</span><span class="sxs-lookup"><span data-stu-id="109f7-154">The device must support displacement mapping.</span></span> <span data-ttu-id="109f7-155">Per ulteriori informazioni sul mapping di spostamento, vedere [mapping di spostamento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="109f7-155">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="109f7-156">Questa costante è supportata solo dalla pipeline programmabile nei dati di N-patch, se N-patch sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="109f7-156">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="109f7-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**\_LOOKUPPRESAMPLED D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="109f7-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD\_LOOKUPPRESAMPLED**</span></span>
</dt> <dd>

<span data-ttu-id="109f7-158">Cercare una mappa di spostamento precampionata.</span><span class="sxs-lookup"><span data-stu-id="109f7-158">Look up a presampled displacement map.</span></span> <span data-ttu-id="109f7-159">Il tipo di input deve essere impostato su D3DDECLTYPE \_ INutilizzato. l'indice del flusso e l'offset del flusso devono essere impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="109f7-159">The input type must be set to D3DDECLTYPE\_UNUSED; the stream index and the stream offset must be set to 0.</span></span> <span data-ttu-id="109f7-160">Il tipo di output per questa operazione è sempre D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="109f7-160">The output type for this operation is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="109f7-161">Il dispositivo deve supportare il mapping di spostamento.</span><span class="sxs-lookup"><span data-stu-id="109f7-161">The device must support displacement mapping.</span></span> <span data-ttu-id="109f7-162">Per ulteriori informazioni sul mapping di spostamento, vedere [mapping di spostamento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="109f7-162">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="109f7-163">Questa costante è supportata solo dalla pipeline programmabile nei dati di N-patch, se N-patch sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="109f7-163">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span> <span data-ttu-id="109f7-164">Questo metodo può essere utilizzato solo con l' \_ esempio D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="109f7-164">This method can be used only with D3DDECLUSAGE\_SAMPLE.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="109f7-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="109f7-165">Remarks</span></span>

<span data-ttu-id="109f7-166">Mosaico esamina il metodo per determinare i dati da calcolare dai dati dei vertici durante il mosaico.</span><span class="sxs-lookup"><span data-stu-id="109f7-166">The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation.</span></span> <span data-ttu-id="109f7-167">I dati mesh devono usare il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="109f7-167">Mesh data should use the default value.</span></span> <span data-ttu-id="109f7-168">Le patch possono usare qualsiasi altro tipo implementato.</span><span class="sxs-lookup"><span data-stu-id="109f7-168">Patches can use any of the other implemented types.</span></span>

<span data-ttu-id="109f7-169">I dati dei vertici vengono dichiarati con una matrice di strutture [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="109f7-169">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="109f7-170">Ogni elemento nella matrice contiene un metodo di dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="109f7-170">Each element in the array contains a vertex declaration method.</span></span>

<span data-ttu-id="109f7-171">Oltre a usare D3DDECLMETHOD \_ default, una mesh normale può usare \_ i metodi di ricerca D3DDECLMETHOD e D3DDECLMETHOD \_ LOOKUPPRESAMPLED quando N-patch è abilitato.</span><span class="sxs-lookup"><span data-stu-id="109f7-171">In addition to using D3DDECLMETHOD\_DEFAULT, a normal mesh can use D3DDECLMETHOD\_LOOKUP and D3DDECLMETHOD\_LOOKUPPRESAMPLED methods when N-patches are enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="109f7-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="109f7-172">Requirements</span></span>



| <span data-ttu-id="109f7-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="109f7-173">Requirement</span></span> | <span data-ttu-id="109f7-174">Valore</span><span class="sxs-lookup"><span data-stu-id="109f7-174">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="109f7-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="109f7-175">Header</span></span><br/> | <dl> <span data-ttu-id="109f7-176"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="109f7-176"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="109f7-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="109f7-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109f7-178">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="109f7-178">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




