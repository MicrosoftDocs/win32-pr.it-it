---
description: Prepara un dispositivo per il disegno degli sprite.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'Metodo ID3DXSprite:: begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322973"
---
# <a name="id3dxspritebegin-method"></a><span data-ttu-id="64b7a-103">Metodo ID3DXSprite:: Begin</span><span class="sxs-lookup"><span data-stu-id="64b7a-103">ID3DXSprite::Begin method</span></span>

<span data-ttu-id="64b7a-104">Prepara un dispositivo per il disegno degli sprite.</span><span class="sxs-lookup"><span data-stu-id="64b7a-104">Prepares a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b7a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64b7a-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="64b7a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64b7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b7a-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64b7a-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b7a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64b7a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64b7a-109">Combinazione di zero o più flag che descrivono le opzioni di rendering sprite.</span><span class="sxs-lookup"><span data-stu-id="64b7a-109">Combination of zero or more flags that describe sprite rendering options.</span></span> <span data-ttu-id="64b7a-110">Per questo metodo, i flag validi sono:</span><span class="sxs-lookup"><span data-stu-id="64b7a-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="64b7a-111">\_AlphaBlend D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="64b7a-111">D3DXSPRITE\_ALPHABLEND</span></span>
-   <span data-ttu-id="64b7a-112">\_ \_ TABELLONe D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="64b7a-112">D3DXSPRITE\_\_BILLBOARD</span></span>
-   <span data-ttu-id="64b7a-113">D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE</span><span class="sxs-lookup"><span data-stu-id="64b7a-113">D3DXSPRITE\_DONOTMODIFY\_RENDERSTATE</span></span>
-   <span data-ttu-id="64b7a-114">\_DONOTSAVESTATE D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="64b7a-114">D3DXSPRITE\_DONOTSAVESTATE</span></span>
-   <span data-ttu-id="64b7a-115">\_OBJECTSPACE D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="64b7a-115">D3DXSPRITE\_OBJECTSPACE</span></span>
-   <span data-ttu-id="64b7a-116">\_ \_ Profondità di ordinamento D3DXSPRITE \_ \_ BACKTOFRONT</span><span class="sxs-lookup"><span data-stu-id="64b7a-116">D3DXSPRITE\_\_SORT\_DEPTH\_BACKTOFRONT</span></span>
-   <span data-ttu-id="64b7a-117">\_ \_ Profondità di ordinamento D3DXSPRITE \_ \_ FRONTTOBACK</span><span class="sxs-lookup"><span data-stu-id="64b7a-117">D3DXSPRITE\_\_SORT\_DEPTH\_FRONTTOBACK</span></span>
-   <span data-ttu-id="64b7a-118">\_ \_ Trama di ordinamento D3DXSPRITE \_</span><span class="sxs-lookup"><span data-stu-id="64b7a-118">D3DXSPRITE\_\_SORT\_TEXTURE</span></span>

<span data-ttu-id="64b7a-119">Per una descrizione dei flag e per informazioni su come controllare le trasformazioni di acquisizione dello stato del dispositivo e visualizzazione dispositivi, vedere [D3DXSPRITE](d3dxsprite.md).</span><span class="sxs-lookup"><span data-stu-id="64b7a-119">For a description of the flags and for information on how to control device state capture and device view transforms, see [D3DXSPRITE](d3dxsprite.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b7a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64b7a-120">Return value</span></span>

<span data-ttu-id="64b7a-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64b7a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64b7a-122">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64b7a-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="64b7a-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="64b7a-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b7a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="64b7a-124">Remarks</span></span>

<span data-ttu-id="64b7a-125">Questo metodo deve essere chiamato dall'interno di [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="64b7a-125">This method must be called from inside a [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) .</span></span> <span data-ttu-id="64b7a-126">.</span><span class="sxs-lookup"><span data-stu-id="64b7a-126">.</span></span> <span data-ttu-id="64b7a-127">.</span><span class="sxs-lookup"><span data-stu-id="64b7a-127">.</span></span> <span data-ttu-id="64b7a-128">Sequenza [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="64b7a-128">[**IDirect3DDevice9::EndScene**](/windows/desktop/api) sequence.</span></span> <span data-ttu-id="64b7a-129">Impossibile utilizzare **ID3DXSprite:: Begin** come sostituto di **IDirect3DDevice9:: BeginScene** o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="64b7a-129">**ID3DXSprite::Begin** cannot be used as a substitute for either **IDirect3DDevice9::BeginScene** or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

<span data-ttu-id="64b7a-130">Questo metodo consente di impostare gli Stati seguenti nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64b7a-130">This method will set the following states on the device.</span></span>

<span data-ttu-id="64b7a-131">Stati di rendering:</span><span class="sxs-lookup"><span data-stu-id="64b7a-131">Render States:</span></span>



| <span data-ttu-id="64b7a-132">Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="64b7a-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span></span> | <span data-ttu-id="64b7a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="64b7a-133">Value</span></span>                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b7a-134">\_ALPHABLENDENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-134">D3DRS\_ALPHABLENDENABLE</span></span>                                       | <span data-ttu-id="64b7a-135">true</span><span class="sxs-lookup"><span data-stu-id="64b7a-135">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="64b7a-136">\_ALPHAFUNC D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-136">D3DRS\_ALPHAFUNC</span></span>                                              | <span data-ttu-id="64b7a-137">D3DCMP \_ maggiore</span><span class="sxs-lookup"><span data-stu-id="64b7a-137">D3DCMP\_GREATER</span></span>                                                                                                   |
| <span data-ttu-id="64b7a-138">\_ALPHAREF D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-138">D3DRS\_ALPHAREF</span></span>                                               | <span data-ttu-id="64b7a-139">0x00</span><span class="sxs-lookup"><span data-stu-id="64b7a-139">0x00</span></span>                                                                                                              |
| <span data-ttu-id="64b7a-140">\_ALPHATESTENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-140">D3DRS\_ALPHATESTENABLE</span></span>                                        | <span data-ttu-id="64b7a-141">AlphaCmpCaps</span><span class="sxs-lookup"><span data-stu-id="64b7a-141">AlphaCmpCaps</span></span>                                                                                                      |
| <span data-ttu-id="64b7a-142">\_BLENDOP D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-142">D3DRS\_BLENDOP</span></span>                                                | <span data-ttu-id="64b7a-143">D3DBLENDOP \_ aggiungere</span><span class="sxs-lookup"><span data-stu-id="64b7a-143">D3DBLENDOP\_ADD</span></span>                                                                                                   |
| <span data-ttu-id="64b7a-144">Ritaglio D3DRS \_</span><span class="sxs-lookup"><span data-stu-id="64b7a-144">D3DRS\_CLIPPING</span></span>                                               | <span data-ttu-id="64b7a-145">true</span><span class="sxs-lookup"><span data-stu-id="64b7a-145">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="64b7a-146">\_CLIPPLANEENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-146">D3DRS\_CLIPPLANEENABLE</span></span>                                        | <span data-ttu-id="64b7a-147">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-147">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-148">\_COLORWRITEENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-148">D3DRS\_COLORWRITEENABLE</span></span>                                       | <span data-ttu-id="64b7a-149">D3DCOLORWRITEENABLE \_ alfa \| D3DCOLORWRITEENABLE \_ blu \| D3DCOLORWRITEENABLE \_ verde \| D3DCOLORWRITEENABLE \_ rosso</span><span class="sxs-lookup"><span data-stu-id="64b7a-149">D3DCOLORWRITEENABLE\_ALPHA \| D3DCOLORWRITEENABLE\_BLUE \| D3DCOLORWRITEENABLE\_GREEN \| D3DCOLORWRITEENABLE\_RED</span></span> |
| <span data-ttu-id="64b7a-150">\_CULLMODE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-150">D3DRS\_CULLMODE</span></span>                                               | <span data-ttu-id="64b7a-151">D3DCULL \_ None</span><span class="sxs-lookup"><span data-stu-id="64b7a-151">D3DCULL\_NONE</span></span>                                                                                                     |
| <span data-ttu-id="64b7a-152">\_DESTBLEND D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-152">D3DRS\_DESTBLEND</span></span>                                              | <span data-ttu-id="64b7a-153">\_INVSRCALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="64b7a-153">D3DBLEND\_INVSRCALPHA</span></span>                                                                                             |
| <span data-ttu-id="64b7a-154">\_DIFFUSEMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-154">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>                                  | <span data-ttu-id="64b7a-155">\_COLOR1 D3DMCS</span><span class="sxs-lookup"><span data-stu-id="64b7a-155">D3DMCS\_COLOR1</span></span>                                                                                                    |
| <span data-ttu-id="64b7a-156">\_ENABLEADAPTIVETESSELLATION D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-156">D3DRS\_ENABLEADAPTIVETESSELLATION</span></span>                             | <span data-ttu-id="64b7a-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-157">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-158">\_FillMode D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-158">D3DRS\_FILLMODE</span></span>                                               | <span data-ttu-id="64b7a-159">D3DFILL \_ Solid</span><span class="sxs-lookup"><span data-stu-id="64b7a-159">D3DFILL\_SOLID</span></span>                                                                                                    |
| <span data-ttu-id="64b7a-160">\_FOGENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-160">D3DRS\_FOGENABLE</span></span>                                              | <span data-ttu-id="64b7a-161">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-161">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-162">\_INDEXEDVERTEXBLENDENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-162">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>                               | <span data-ttu-id="64b7a-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-163">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-164">\_Illuminazione D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-164">D3DRS\_LIGHTING</span></span>                                               | <span data-ttu-id="64b7a-165">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-165">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-166">\_RANGEFOGENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-166">D3DRS\_RANGEFOGENABLE</span></span>                                         | <span data-ttu-id="64b7a-167">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-167">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-168">\_SEPARATEALPHABLENDENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-168">D3DRS\_SEPARATEALPHABLENDENABLE</span></span>                               | <span data-ttu-id="64b7a-169">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-169">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-170">\_MODOOMBRA D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-170">D3DRS\_SHADEMODE</span></span>                                              | <span data-ttu-id="64b7a-171">\_Gouraud D3DSHADE</span><span class="sxs-lookup"><span data-stu-id="64b7a-171">D3DSHADE\_GOURAUD</span></span>                                                                                                 |
| <span data-ttu-id="64b7a-172">\_SPECULARENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-172">D3DRS\_SPECULARENABLE</span></span>                                         | <span data-ttu-id="64b7a-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-173">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-174">\_SRCBLEND D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-174">D3DRS\_SRCBLEND</span></span>                                               | <span data-ttu-id="64b7a-175">\_SRCALPHA D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="64b7a-175">D3DBLEND\_SRCALPHA</span></span>                                                                                                |
| <span data-ttu-id="64b7a-176">\_SRGBWRITEENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-176">D3DRS\_SRGBWRITEENABLE</span></span>                                        | <span data-ttu-id="64b7a-177">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-177">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-178">\_STENCILENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-178">D3DRS\_STENCILENABLE</span></span>                                          | <span data-ttu-id="64b7a-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-179">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-180">\_VERTEXBLEND D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-180">D3DRS\_VERTEXBLEND</span></span>                                            | <span data-ttu-id="64b7a-181">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b7a-181">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="64b7a-182">\_WRAP0 D3DRS</span><span class="sxs-lookup"><span data-stu-id="64b7a-182">D3DRS\_WRAP0</span></span>                                                  | <span data-ttu-id="64b7a-183">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-183">0</span></span>                                                                                                                 |



 

<span data-ttu-id="64b7a-184">Stati della fase trama:</span><span class="sxs-lookup"><span data-stu-id="64b7a-184">Texture Stage States:</span></span>



| <span data-ttu-id="64b7a-185">Identificatore fase</span><span class="sxs-lookup"><span data-stu-id="64b7a-185">Stage Identifier</span></span> | <span data-ttu-id="64b7a-186">Tipo ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span><span class="sxs-lookup"><span data-stu-id="64b7a-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span></span> | <span data-ttu-id="64b7a-187">Valore</span><span class="sxs-lookup"><span data-stu-id="64b7a-187">Value</span></span>            |
|------------------|---------------------------------------------------------------------------|------------------|
| <span data-ttu-id="64b7a-188">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-188">0</span></span>                | <span data-ttu-id="64b7a-189">\_ALPHAARG1 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-189">D3DTSS\_ALPHAARG1</span></span>                                                         | <span data-ttu-id="64b7a-190">\_Trama D3DTA</span><span class="sxs-lookup"><span data-stu-id="64b7a-190">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="64b7a-191">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-191">0</span></span>                | <span data-ttu-id="64b7a-192">\_ALPHAARG2 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-192">D3DTSS\_ALPHAARG2</span></span>                                                         | <span data-ttu-id="64b7a-193">D3DTA \_ diffuse</span><span class="sxs-lookup"><span data-stu-id="64b7a-193">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="64b7a-194">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-194">0</span></span>                | <span data-ttu-id="64b7a-195">\_ALPHAOP D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-195">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="64b7a-196">\_Modulazione D3DTOP</span><span class="sxs-lookup"><span data-stu-id="64b7a-196">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="64b7a-197">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-197">0</span></span>                | <span data-ttu-id="64b7a-198">\_COLORARG1 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-198">D3DTSS\_COLORARG1</span></span>                                                         | <span data-ttu-id="64b7a-199">\_Trama D3DTA</span><span class="sxs-lookup"><span data-stu-id="64b7a-199">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="64b7a-200">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-200">0</span></span>                | <span data-ttu-id="64b7a-201">\_COLORARG2 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-201">D3DTSS\_COLORARG2</span></span>                                                         | <span data-ttu-id="64b7a-202">D3DTA \_ diffuse</span><span class="sxs-lookup"><span data-stu-id="64b7a-202">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="64b7a-203">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-203">0</span></span>                | <span data-ttu-id="64b7a-204">\_COLOROP D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-204">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="64b7a-205">\_Modulazione D3DTOP</span><span class="sxs-lookup"><span data-stu-id="64b7a-205">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="64b7a-206">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-206">0</span></span>                | <span data-ttu-id="64b7a-207">\_TEXCOORDINDEX D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-207">D3DTSS\_TEXCOORDINDEX</span></span>                                                     | <span data-ttu-id="64b7a-208">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-208">0</span></span>                |
| <span data-ttu-id="64b7a-209">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-209">0</span></span>                | <span data-ttu-id="64b7a-210">\_TEXTURETRANSFORMFLAGS D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-210">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>                                             | <span data-ttu-id="64b7a-211">\_Disabilitazione D3DTTFF</span><span class="sxs-lookup"><span data-stu-id="64b7a-211">D3DTTFF\_DISABLE</span></span> |
| <span data-ttu-id="64b7a-212">1</span><span class="sxs-lookup"><span data-stu-id="64b7a-212">1</span></span>                | <span data-ttu-id="64b7a-213">\_ALPHAOP D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-213">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="64b7a-214">\_Disabilitazione D3DTOP</span><span class="sxs-lookup"><span data-stu-id="64b7a-214">D3DTOP\_DISABLE</span></span>  |
| <span data-ttu-id="64b7a-215">1</span><span class="sxs-lookup"><span data-stu-id="64b7a-215">1</span></span>                | <span data-ttu-id="64b7a-216">\_COLOROP D3DTSS</span><span class="sxs-lookup"><span data-stu-id="64b7a-216">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="64b7a-217">\_Disabilitazione D3DTOP</span><span class="sxs-lookup"><span data-stu-id="64b7a-217">D3DTOP\_DISABLE</span></span>  |



 

<span data-ttu-id="64b7a-218">Stati campionatore:</span><span class="sxs-lookup"><span data-stu-id="64b7a-218">Sampler States:</span></span>



| <span data-ttu-id="64b7a-219">Indice fase campionatore</span><span class="sxs-lookup"><span data-stu-id="64b7a-219">Sampler Stage Index</span></span> | <span data-ttu-id="64b7a-220">Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="64b7a-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span></span> | <span data-ttu-id="64b7a-221">Valore</span><span class="sxs-lookup"><span data-stu-id="64b7a-221">Value</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b7a-222">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-222">0</span></span>                   | <span data-ttu-id="64b7a-223">\_Indirizzo D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-223">D3DSAMP\_ADDRESSU</span></span>                                               | <span data-ttu-id="64b7a-224">\_Clamp D3DTADDRESS</span><span class="sxs-lookup"><span data-stu-id="64b7a-224">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="64b7a-225">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-225">0</span></span>                   | <span data-ttu-id="64b7a-226">\_ADDRESSV D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-226">D3DSAMP\_ADDRESSV</span></span>                                               | <span data-ttu-id="64b7a-227">\_Clamp D3DTADDRESS</span><span class="sxs-lookup"><span data-stu-id="64b7a-227">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="64b7a-228">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-228">0</span></span>                   | <span data-ttu-id="64b7a-229">\_MAGFILTER D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-229">D3DSAMP\_MAGFILTER</span></span>                                              | <span data-ttu-id="64b7a-230">D3DTEXF \_ anisotropico se TextureFilterCaps include D3DPTFILTERCAPS \_ MAGFANISOTROPIC; in caso contrario, D3DTEXF \_ lineare</span><span class="sxs-lookup"><span data-stu-id="64b7a-230">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MAGFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="64b7a-231">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-231">0</span></span>                   | <span data-ttu-id="64b7a-232">\_MAXMIPLEVEL D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-232">D3DSAMP\_MAXMIPLEVEL</span></span>                                            | <span data-ttu-id="64b7a-233">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-233">0</span></span>                                                                                                              |
| <span data-ttu-id="64b7a-234">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-234">0</span></span>                   | <span data-ttu-id="64b7a-235">\_MAXANISOTROPY D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-235">D3DSAMP\_MAXANISOTROPY</span></span>                                          | <span data-ttu-id="64b7a-236">MaxAnisotropy</span><span class="sxs-lookup"><span data-stu-id="64b7a-236">MaxAnisotropy</span></span>                                                                                                  |
| <span data-ttu-id="64b7a-237">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-237">0</span></span>                   | <span data-ttu-id="64b7a-238">\_MINFILTER D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-238">D3DSAMP\_MINFILTER</span></span>                                              | <span data-ttu-id="64b7a-239">D3DTEXF \_ anisotropico se TextureFilterCaps include D3DPTFILTERCAPS \_ MINFANISOTROPIC; in caso contrario, D3DTEXF \_ lineare</span><span class="sxs-lookup"><span data-stu-id="64b7a-239">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MINFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="64b7a-240">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-240">0</span></span>                   | <span data-ttu-id="64b7a-241">\_MIPFILTER D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-241">D3DSAMP\_MIPFILTER</span></span>                                              | <span data-ttu-id="64b7a-242">D3DTEXF \_ lineare se TextureFilterCaps include D3DPTFILTERCAPS \_ MIPFLINEAR; in caso contrario, punto di D3DTEXF \_</span><span class="sxs-lookup"><span data-stu-id="64b7a-242">D3DTEXF\_LINEAR if TextureFilterCaps includes D3DPTFILTERCAPS\_MIPFLINEAR; otherwise D3DTEXF\_POINT</span></span>            |
| <span data-ttu-id="64b7a-243">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-243">0</span></span>                   | <span data-ttu-id="64b7a-244">\_MIPMAPLODBIAS D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-244">D3DSAMP\_MIPMAPLODBIAS</span></span>                                          | <span data-ttu-id="64b7a-245">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-245">0</span></span>                                                                                                              |
| <span data-ttu-id="64b7a-246">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-246">0</span></span>                   | <span data-ttu-id="64b7a-247">\_SRGBTEXTURE D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="64b7a-247">D3DSAMP\_SRGBTEXTURE</span></span>                                            | <span data-ttu-id="64b7a-248">0</span><span class="sxs-lookup"><span data-stu-id="64b7a-248">0</span></span>                                                                                                              |



 

> [!Note]  
> <span data-ttu-id="64b7a-249">Questo metodo Disabilita le N-patch.</span><span class="sxs-lookup"><span data-stu-id="64b7a-249">This method disables N-patches.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64b7a-250">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64b7a-250">Requirements</span></span>



| <span data-ttu-id="64b7a-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b7a-251">Requirement</span></span> | <span data-ttu-id="64b7a-252">Valore</span><span class="sxs-lookup"><span data-stu-id="64b7a-252">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64b7a-253">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64b7a-253">Header</span></span><br/>  | <dl> <span data-ttu-id="64b7a-254"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b7a-254"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="64b7a-255">Libreria</span><span class="sxs-lookup"><span data-stu-id="64b7a-255">Library</span></span><br/> | <dl> <span data-ttu-id="64b7a-256"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64b7a-256"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64b7a-257">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64b7a-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b7a-258">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="64b7a-258">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="64b7a-259">D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="64b7a-259">D3DXSPRITE</span></span>](d3dxsprite.md)
</dt> </dl>

 

 
