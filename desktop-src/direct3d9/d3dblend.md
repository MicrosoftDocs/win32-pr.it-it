---
description: Definisce la modalità di fusione supportata.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Enumerazione D3DBLEND (D3D9Types.h)
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
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343386"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="a2bfd-103">Enumerazione D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="a2bfd-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="a2bfd-104">Definisce la modalità di fusione supportata.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bfd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2bfd-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="a2bfd-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a2bfd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2bfd-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ ZERO**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-108">Il fattore di blend è (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ ONE**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-110">Il fattore di blend è (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-112">Il fattore di blend è (Rs, Gs, Bs, As).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-114">Il fattore di blend è (1 - Rs, 1 - Gs, 1 - Bs, 1 - As).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-116">Il fattore di blend è (As, As, As, As).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-118">Il fattore di blend è ( 1 - As, 1 - As, 1 - As, 1 - As).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-120">Il fattore di blend è (A<sub>d</sub> A<sub>d</sub> A d<sub>A d</sub> A d<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-122">Il fattore di blend è (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A d 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-124">Il fattore di blend è (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-126">Il fattore di blend è (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-128">Il fattore di blend è (f, f, f, 1); dove f = min(As, 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-130">**Obsoleto.**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-130">**Obsolete**.</span></span> <span data-ttu-id="a2bfd-131">A partire da DirectX 6, è possibile ottenere lo stesso effetto impostando i fattori di blend di origine e destinazione su D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA in chiamate separate.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-133">**Obsoleto.**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-133">**Obsolete**.</span></span> <span data-ttu-id="a2bfd-134">Il fattore di blend di origine è (1 - As, 1 - As, 1 - As, 1 - As) e il fattore di blend di destinazione è (As, As, As, As); Viene eseguito l'override della selezione di blend di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="a2bfd-135">Questa modalità di blend è supportata solo per lo stato di rendering D3DRS \_ SRCBLEND.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-137">Fattore di fusione dei colori costante usato dallo blender del buffer di frame.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="a2bfd-138">Questa modalità di blend è supportata solo se D3DPBLENDCAPS BLENDFACTOR è impostato nei membri \_ **SrcBlendCaps** o **DestBlendCaps** di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="a2bfd-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-140">Fattore di fusione dei colori costante invertito usato dal blender frame-buffer.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="a2bfd-141">Questa modalità di blend è supportata solo se il bit D3DPBLENDCAPS BLENDFACTOR è impostato nei membri \_ **SrcBlendCaps** o **DestBlendCaps** di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="a2bfd-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="a2bfd-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-143">Il fattore di fusione è (PSOutColor \[ 1 \] <sub>r,</sub>PSOutColor \[ 1 \] <sub>g,</sub>PSOutColor \[ 1 \] <sub>b,</sub>non usato).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="a2bfd-144">Vedere [Fusione della destinazione di rendering](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-144">See [Render Target Blending](#render-target-blending).</span></span>

<span data-ttu-id="a2bfd-145">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a2bfd-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="a2bfd-146">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-146">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="a2bfd-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-148">Il fattore di blend è (1 - PSOutColor \[ 1 \] <sub>r</sub>, 1 - PSOutColor \[ 1 \] <sub>g,</sub>1 - PSOutColor \[ 1 \] <sub>b</sub>, non usato)).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="a2bfd-149">Vedere [Fusione della destinazione di rendering](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-149">See [Render Target Blending](#render-target-blending).</span></span>


<span data-ttu-id="a2bfd-150">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a2bfd-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="a2bfd-151">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-151">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="a2bfd-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a2bfd-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a2bfd-153">Forza la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a2bfd-154">Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a2bfd-155">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2bfd-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2bfd-156">Remarks</span></span>

<span data-ttu-id="a2bfd-157">Nelle descrizioni dei membri precedenti, i valori RGBA dell'origine e della destinazione sono indicati dagli apici s e d.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="a2bfd-158">I valori in questo tipo enumerato vengono usati dagli stati di rendering seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2bfd-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="a2bfd-159">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="a2bfd-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="a2bfd-160">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="a2bfd-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="a2bfd-161">D3DRS \_ DESTBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="a2bfd-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="a2bfd-162">D3DRS \_ SRCBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="a2bfd-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="a2bfd-163">Vedere [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="a2bfd-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="a2bfd-164">Fusione della destinazione di rendering</span><span class="sxs-lookup"><span data-stu-id="a2bfd-164">Render Target Blending</span></span>

<span data-ttu-id="a2bfd-165">Direct3D 9Ex ha migliorato le funzionalità di rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="a2bfd-166">Il rendering di tipi di carattere non crittografati richiederebbe in genere due passaggi.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="a2bfd-167">Per eliminare il secondo passaggio, è pixel shader possibile usare un'pixel shader per l'output di due colori, che è possibile chiamare PSOutColor \[ 0 \] e PSOutColor \[ \] 1.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="a2bfd-168">Il primo colore conterrà i componenti standard a 3 colori (RGB).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="a2bfd-169">Il secondo colore conterrà 3 componenti alfa (uno per ogni componente del primo colore).</span><span class="sxs-lookup"><span data-stu-id="a2bfd-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="a2bfd-170">Queste nuove modalità di fusione vengono usate solo per il rendering del testo nella prima destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="a2bfd-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2bfd-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2bfd-171">Requirements</span></span>



| <span data-ttu-id="a2bfd-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2bfd-172">Requirement</span></span> | <span data-ttu-id="a2bfd-173">Valore</span><span class="sxs-lookup"><span data-stu-id="a2bfd-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2bfd-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2bfd-174">Header</span></span><br/> | <dl> <span data-ttu-id="a2bfd-175"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="a2bfd-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2bfd-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2bfd-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2bfd-177">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="a2bfd-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
