---
description: Definisce la modalità di Blend supportata.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Enumerazione D3DBLEND (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969320"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="0b279-103">Enumerazione D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="0b279-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="0b279-104">Definisce la modalità di Blend supportata.</span><span class="sxs-lookup"><span data-stu-id="0b279-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b279-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b279-105">Syntax</span></span>


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a><span data-ttu-id="0b279-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="0b279-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0b279-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ zero**</span><span class="sxs-lookup"><span data-stu-id="0b279-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-108">Il fattore di Blend è (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="0b279-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ One**</span><span class="sxs-lookup"><span data-stu-id="0b279-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-110">Il fattore di Blend è (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="0b279-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**\_SRCCOLOR D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-112">Il fattore di Blend è (RS, GS, BS, As).</span><span class="sxs-lookup"><span data-stu-id="0b279-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**\_INVSRCCOLOR D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-114">Il fattore di Blend è (1-RS, 1-GS, 1-BS, 1-As).</span><span class="sxs-lookup"><span data-stu-id="0b279-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**\_SRCALPHA D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-116">Il fattore di Blend è (come, come, come).</span><span class="sxs-lookup"><span data-stu-id="0b279-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**\_INVSRCALPHA D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-118">Il fattore di Blend è (1-As, 1-As, 1-As, 1-As).</span><span class="sxs-lookup"><span data-stu-id="0b279-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**\_DESTALPHA D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-120">Il fattore di Blend è<sub>(a d</sub> <sub>d a d</sub> <sub>a d</sub> <sub>).</sub></span><span class="sxs-lookup"><span data-stu-id="0b279-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**\_INVDESTALPHA D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-122">Il fattore di Blend è (1<sub>-a d 1-</sub> a<sub>d</sub> 1-A<sub>d</sub> 1-a<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0b279-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**\_DESTCOLOR D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-124">Il fattore di Blend è (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0b279-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**\_INVDESTCOLOR D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-126">Il fattore di Blend è (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0b279-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**\_SRCALPHASAT D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-128">Il fattore di Blend è (f, f, f, 1); dove f = min (As, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0b279-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**\_BOTHSRCALPHA D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-130">**Obsoleto**.</span><span class="sxs-lookup"><span data-stu-id="0b279-130">**Obsolete**.</span></span> <span data-ttu-id="0b279-131">A partire da DirectX 6, è possibile ottenere lo stesso risultato impostando i fattori di Blend di origine e di destinazione su D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA in chiamate separate.</span><span class="sxs-lookup"><span data-stu-id="0b279-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="0b279-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**\_BOTHINVSRCALPHA D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-133">**Obsoleto**.</span><span class="sxs-lookup"><span data-stu-id="0b279-133">**Obsolete**.</span></span> <span data-ttu-id="0b279-134">Il fattore di fusione di origine è (1-As, 1-As, 1-As, 1-As) e il fattore di Blend di destinazione è (come, come, As, As viene eseguito l'override della selezione di Blend di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b279-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="0b279-135">Questa modalità di Blend è supportata solo per lo \_ stato di rendering SRCBLEND di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="0b279-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="0b279-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**\_BLENDFACTOR D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-137">Fattore di fusione dei colori costante utilizzato dal Blender del buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="0b279-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="0b279-138">Questa modalità di Blend è supportata solo se D3DPBLENDCAPS \_ BLENDFACTOR è impostato nei membri **SrcBlendCaps** o **DestBlendCaps** di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="0b279-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**\_INVBLENDFACTOR D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-140">Fattore di fusione dei colori costante invertito usato dal Blender del buffer di frame.</span><span class="sxs-lookup"><span data-stu-id="0b279-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="0b279-141">Questa modalità di Blend è supportata solo se il \_ bit BLENDFACTOR di D3DPBLENDCAPS è impostato nei membri **SrcBlendCaps** o **DestBlendCaps** di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="0b279-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="0b279-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**\_SRCCOLOR2 D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-143">Il fattore di Blend è (PSOutColor \[ 1 \] <sub>r</sub>, PSOutColor \[ 1 \] <sub>g</sub>, PSOutColor \[ 1 \] <sub>b</sub>, non usato).</span><span class="sxs-lookup"><span data-stu-id="0b279-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="0b279-144">Vedere [fusione della destinazione di rendering](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="0b279-144">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b279-145">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="0b279-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="0b279-146">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="0b279-146">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b279-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**\_INVSRCCOLOR2 D3DBLEND**</span><span class="sxs-lookup"><span data-stu-id="0b279-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-148">Il fattore di Blend è (1-PSOutColor \[ 1 \] <sub>r</sub>, 1-PSOutColor \[ 1 \] <sub>g</sub>, 1-PSOutColor \[ 1 \] <sub>b</sub>, non usato).</span><span class="sxs-lookup"><span data-stu-id="0b279-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="0b279-149">Vedere [fusione della destinazione di rendering](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="0b279-149">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b279-150">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="0b279-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="0b279-151">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="0b279-151">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b279-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0b279-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0b279-153">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0b279-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0b279-154">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0b279-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0b279-155">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="0b279-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b279-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b279-156">Remarks</span></span>

<span data-ttu-id="0b279-157">Nelle descrizioni dei membri precedenti, i valori RGBA dell'origine e della destinazione sono indicati dagli indici s e d.</span><span class="sxs-lookup"><span data-stu-id="0b279-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="0b279-158">I valori in questo tipo enumerato vengono utilizzati dagli Stati di rendering seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b279-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="0b279-159">\_DESTBLEND D3DRS</span><span class="sxs-lookup"><span data-stu-id="0b279-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="0b279-160">\_SRCBLEND D3DRS</span><span class="sxs-lookup"><span data-stu-id="0b279-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="0b279-161">\_DESTBLENDALPHA D3DRS</span><span class="sxs-lookup"><span data-stu-id="0b279-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="0b279-162">\_SRCBLENDALPHA D3DRS</span><span class="sxs-lookup"><span data-stu-id="0b279-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="0b279-163">Vedere [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="0b279-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="0b279-164">Blend di destinazione di rendering</span><span class="sxs-lookup"><span data-stu-id="0b279-164">Render Target Blending</span></span>

<span data-ttu-id="0b279-165">Direct3D 9Ex ha migliorato le funzionalità di rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="0b279-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="0b279-166">Il rendering di tipi di carattere Clear-Type richiede in genere due passaggi.</span><span class="sxs-lookup"><span data-stu-id="0b279-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="0b279-167">Per eliminare il secondo passaggio, è possibile usare un pixel shader per restituire due colori, che è possibile chiamare PSOutColor \[ 0 \] e PSOutColor \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0b279-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="0b279-168">Il primo colore conterrà i componenti standard 3 Color (RGB).</span><span class="sxs-lookup"><span data-stu-id="0b279-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="0b279-169">Il secondo colore conterrebbe 3 componenti alfa (uno per ogni componente del primo colore).</span><span class="sxs-lookup"><span data-stu-id="0b279-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="0b279-170">Queste nuove modalità di fusione vengono usate solo per il rendering del testo nella prima destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="0b279-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b279-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b279-171">Requirements</span></span>



| <span data-ttu-id="0b279-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b279-172">Requirement</span></span> | <span data-ttu-id="0b279-173">Valore</span><span class="sxs-lookup"><span data-stu-id="0b279-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b279-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b279-174">Header</span></span><br/> | <dl> <span data-ttu-id="0b279-175"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b279-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b279-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b279-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b279-177">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="0b279-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
