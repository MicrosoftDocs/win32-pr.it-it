---
description: Gli Stati del campionatore definiscono le operazioni di campionamento della trama, ad esempio l'indirizzamento della trama e
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Enumerazione D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322440"
---
# <a name="d3dsamplerstatetype-enumeration"></a><span data-ttu-id="41688-103">Enumerazione D3DSAMPLERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="41688-103">D3DSAMPLERSTATETYPE enumeration</span></span>

<span data-ttu-id="41688-104">Gli Stati del campionatore definiscono le operazioni di campionamento della trama, ad esempio l'indirizzamento della trama e</span><span class="sxs-lookup"><span data-stu-id="41688-104">Sampler states define texture sampling operations such as texture addressing and texture filtering.</span></span> <span data-ttu-id="41688-105">Alcuni Stati del campionatore configurano l'elaborazione dei vertici e alcune impostazioni di elaborazione dei pixel.</span><span class="sxs-lookup"><span data-stu-id="41688-105">Some sampler states set-up vertex processing, and some set-up pixel processing.</span></span> <span data-ttu-id="41688-106">Gli Stati del campionatore possono essere salvati e ripristinati usando stateblocks (vedere lo stato [di salvataggio e ripristino del blocco di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="41688-106">Sampler states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="41688-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41688-107">Syntax</span></span>


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="41688-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="41688-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="41688-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**\_Indirizzo D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP\_ADDRESSU**</span></span>
</dt> <dd>

<span data-ttu-id="41688-110">Modalità di indirizzamento della trama per la coordinata u.</span><span class="sxs-lookup"><span data-stu-id="41688-110">Texture-address mode for the u coordinate.</span></span> <span data-ttu-id="41688-111">Il valore predefinito è D3DTADDRESS \_ wrap.</span><span class="sxs-lookup"><span data-stu-id="41688-111">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="41688-112">Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="41688-112">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="41688-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**\_ADDRESSV D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP\_ADDRESSV**</span></span>
</dt> <dd>

<span data-ttu-id="41688-114">Modalità di indirizzo della trama per la coordinata v.</span><span class="sxs-lookup"><span data-stu-id="41688-114">Texture-address mode for the v coordinate.</span></span> <span data-ttu-id="41688-115">Il valore predefinito è D3DTADDRESS \_ wrap.</span><span class="sxs-lookup"><span data-stu-id="41688-115">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="41688-116">Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="41688-116">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="41688-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**\_ADDRESSW D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP\_ADDRESSW**</span></span>
</dt> <dd>

<span data-ttu-id="41688-118">Modalità di indirizzamento della trama per la coordinata w.</span><span class="sxs-lookup"><span data-stu-id="41688-118">Texture-address mode for the w coordinate.</span></span> <span data-ttu-id="41688-119">Il valore predefinito è D3DTADDRESS \_ wrap.</span><span class="sxs-lookup"><span data-stu-id="41688-119">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="41688-120">Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="41688-120">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="41688-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**\_BorderColor D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP\_BORDERCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="41688-122">Colore del bordo o tipo [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="41688-122">Border color or type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="41688-123">Il colore predefinito è 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="41688-123">The default color is 0x00000000.</span></span>

</dd> <dt>

<span data-ttu-id="41688-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**\_MAGFILTER D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP\_MAGFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="41688-125">Filtro di ingrandimento di tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="41688-125">Magnification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="41688-126">Il valore predefinito è D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="41688-126">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="41688-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**\_MINFILTER D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP\_MINFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="41688-128">Filtro minification di tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="41688-128">Minification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="41688-129">Il valore predefinito è D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="41688-129">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="41688-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**\_MIPFILTER D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP\_MIPFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="41688-131">Filtro mipmap da utilizzare durante minification.</span><span class="sxs-lookup"><span data-stu-id="41688-131">Mipmap filter to use during minification.</span></span> <span data-ttu-id="41688-132">Vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="41688-132">See [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="41688-133">Il valore predefinito è D3DTEXF \_ None.</span><span class="sxs-lookup"><span data-stu-id="41688-133">The default value is D3DTEXF\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="41688-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**\_MIPMAPLODBIAS D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP\_MIPMAPLODBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="41688-135">Distorsione del livello di dettaglio del mipmap.</span><span class="sxs-lookup"><span data-stu-id="41688-135">Mipmap level-of-detail bias.</span></span> <span data-ttu-id="41688-136">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="41688-136">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="41688-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**\_MAXMIPLEVEL D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP\_MAXMIPLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="41688-138">Indice del livello di dettaglio della mappa più grande da usare.</span><span class="sxs-lookup"><span data-stu-id="41688-138">level-of-detail index of largest map to use.</span></span> <span data-ttu-id="41688-139">I valori sono compresi tra 0 e (n-1), dove 0 è il più grande.</span><span class="sxs-lookup"><span data-stu-id="41688-139">Values range from 0 to (n - 1) where 0 is the largest.</span></span> <span data-ttu-id="41688-140">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="41688-140">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="41688-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**\_MAXANISOTROPY D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP\_MAXANISOTROPY**</span></span>
</dt> <dd>

<span data-ttu-id="41688-142">Anisotropia massima DWORD.</span><span class="sxs-lookup"><span data-stu-id="41688-142">DWORD maximum anisotropy.</span></span> <span data-ttu-id="41688-143">I valori sono compresi tra 1 e il valore specificato nel membro **MaxAnisotropy** della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="41688-143">Values range from 1 to the value that is specified in the **MaxAnisotropy** member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="41688-144">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="41688-144">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="41688-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**\_SRGBTEXTURE D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP\_SRGBTEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="41688-146">Valore di correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="41688-146">Gamma correction value.</span></span> <span data-ttu-id="41688-147">Il valore predefinito è 0, che indica che la gamma è 1,0 e non è richiesta alcuna correzione.</span><span class="sxs-lookup"><span data-stu-id="41688-147">The default value is 0, which means gamma is 1.0 and no correction is required.</span></span> <span data-ttu-id="41688-148">In caso contrario, questo valore indica che il campionatore deve presupporre gamma di 2,2 sul contenuto e convertirlo in lineare (gamma 1,0) prima di presentarlo alla pixel shader.</span><span class="sxs-lookup"><span data-stu-id="41688-148">Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="41688-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**\_ELEMENTINDEX D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP\_ELEMENTINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="41688-150">Quando una trama a più elementi viene assegnata al campionatore, indica l'indice dell'elemento da usare.</span><span class="sxs-lookup"><span data-stu-id="41688-150">When a multielement texture is assigned to the sampler, this indicates which element index to use.</span></span> <span data-ttu-id="41688-151">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="41688-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="41688-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**\_DMAPOFFSET D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="41688-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP\_DMAPOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="41688-153">Offset del vertice nella mappa di spostamento precampionata.</span><span class="sxs-lookup"><span data-stu-id="41688-153">Vertex offset in the presampled displacement map.</span></span> <span data-ttu-id="41688-154">Si tratta di una costante utilizzata da mosaico, il cui valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="41688-154">This is a constant used by the tessellator, its default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="41688-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="41688-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="41688-156">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="41688-156">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="41688-157">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="41688-157">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="41688-158">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="41688-158">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41688-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41688-159">Requirements</span></span>



| <span data-ttu-id="41688-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="41688-160">Requirement</span></span> | <span data-ttu-id="41688-161">Valore</span><span class="sxs-lookup"><span data-stu-id="41688-161">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41688-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41688-162">Header</span></span><br/> | <dl> <span data-ttu-id="41688-163"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="41688-163"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41688-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41688-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41688-165">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="41688-165">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
