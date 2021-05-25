---
description: Gli stati di rendering definiscono gli stati di configurazione per tutti i tipi di elaborazione di vertici e pixel.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumerazione D3DRENDERSTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343066"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="748d5-103">Enumerazione D3DRENDERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="748d5-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="748d5-104">Gli stati di rendering definiscono gli stati di configurazione per tutti i tipi di elaborazione di vertici e pixel.</span><span class="sxs-lookup"><span data-stu-id="748d5-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="748d5-105">Alcuni stati di rendering configurano l'elaborazione dei vertici e altri configurano l'elaborazione dei pixel (vedere Stati di rendering [(Direct3D 9)](render-states.md)).</span><span class="sxs-lookup"><span data-stu-id="748d5-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="748d5-106">Gli stati di rendering possono essere salvati e ripristinati usando blocchi di stato (vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="748d5-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="748d5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="748d5-107">Syntax</span></span>


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="748d5-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="748d5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="748d5-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-110">Stato di buffering di profondità come membro del [**tipo enumerato D3DZBUFFERTYPE.**](./d3dzbuffertype.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="748d5-111">Impostare questo stato su D3DZB TRUE per abilitare il \_ buffering z, D3DZB USEW per abilitare \_ il w-buffering o D3DZB FALSE per disabilitare il buffering di \_ profondità.</span><span class="sxs-lookup"><span data-stu-id="748d5-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="748d5-112">Il valore predefinito per questo stato di rendering è D3DZB TRUE se è stato creato un depth stencil insieme alla catena di scambio impostando il membro \_ EnableAutoDepthStencil della struttura [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) su **TRUE** e D3DZB FALSE in caso \_ contrario.</span><span class="sxs-lookup"><span data-stu-id="748d5-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**</span><span class="sxs-lookup"><span data-stu-id="748d5-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-114">Uno o più membri del [**tipo enumerato D3DFILLMODE.**](./d3dfillmode.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="748d5-115">Il valore predefinito è D3DFILL \_ SOLID.</span><span class="sxs-lookup"><span data-stu-id="748d5-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**</span><span class="sxs-lookup"><span data-stu-id="748d5-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-117">Uno o più membri del [**tipo enumerato D3DSHADEMODE.**](./d3dshademode.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="748d5-118">Il valore predefinito è D3DSHADE \_ GOURAUD.</span><span class="sxs-lookup"><span data-stu-id="748d5-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-120">**TRUE** per consentire all'applicazione di scrivere nel buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="748d5-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="748d5-121">Il valore predefinito è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-121">The default value is **TRUE**.</span></span> <span data-ttu-id="748d5-122">Questo membro consente a un'applicazione di impedire al sistema di aggiornare il buffer di profondità con nuovi valori di profondità.</span><span class="sxs-lookup"><span data-stu-id="748d5-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="748d5-123">Se **FALSE,** i confronti di profondità vengono comunque eseguono in base allo stato di rendering D3DRS ZFUNC, presupponendo che sia in corso il buffering della profondità, ma i valori di profondità non vengono scritti \_ nel buffer.</span><span class="sxs-lookup"><span data-stu-id="748d5-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-125">**TRUE per** abilitare il test alfa per pixel.</span><span class="sxs-lookup"><span data-stu-id="748d5-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="748d5-126">Se il test viene superato, il pixel viene elaborato dal buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="748d5-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="748d5-127">In caso contrario, tutta l'elaborazione del buffer dei frame viene ignorata per il pixel.</span><span class="sxs-lookup"><span data-stu-id="748d5-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="748d5-128">Il test viene eseguito confrontando il valore alfa in ingresso con il valore alfa di riferimento, usando la funzione di confronto fornita dallo stato di rendering D3DRS \_ ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="748d5-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="748d5-129">Il valore alfa di riferimento è determinato dal valore impostato per D3DRS \_ ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="748d5-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="748d5-130">Per altre informazioni, vedere [Alpha Testing State (Direct3D 9) (Stato di test alfa - Direct3D 9).](alpha-testing-state.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="748d5-131">Il valore predefinito di questo parametro è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**</span><span class="sxs-lookup"><span data-stu-id="748d5-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-133">Il valore predefinito è **TRUE,** che consente di disegnare l'ultimo pixel di una linea.</span><span class="sxs-lookup"><span data-stu-id="748d5-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="748d5-134">Per impedire il disegno dell'ultimo pixel, impostare questo valore su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="748d5-135">Per altre informazioni, vedere [Stato contorno e riempimento (Direct3D 9).](outline-and-fill-state.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**</span><span class="sxs-lookup"><span data-stu-id="748d5-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-137">Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="748d5-138">Il valore predefinito è D3DBLEND \_ ONE.</span><span class="sxs-lookup"><span data-stu-id="748d5-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**</span><span class="sxs-lookup"><span data-stu-id="748d5-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-140">Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="748d5-141">Il valore predefinito è D3DBLEND \_ ZERO.</span><span class="sxs-lookup"><span data-stu-id="748d5-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**</span><span class="sxs-lookup"><span data-stu-id="748d5-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-143">Specifica come vengono espulsi i triangoli rivolti verso il retro, se non del tutto.</span><span class="sxs-lookup"><span data-stu-id="748d5-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="748d5-144">Può essere impostato su un membro del [**tipo enumerato D3DCULL.**](./d3dcull.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="748d5-145">Il valore predefinito è D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="748d5-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**</span><span class="sxs-lookup"><span data-stu-id="748d5-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-147">Membro del tipo [**enumerato D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="748d5-148">Il valore predefinito è D3DCMP \_ LESSEQUAL.</span><span class="sxs-lookup"><span data-stu-id="748d5-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="748d5-149">Questo membro consente a un'applicazione di accettare o rifiutare un pixel, in base alla distanza dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="748d5-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="748d5-150">Il valore di profondità del pixel viene confrontato con il valore depth-buffer.</span><span class="sxs-lookup"><span data-stu-id="748d5-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="748d5-151">Se il valore di profondità del pixel supera la funzione di confronto, viene scritto il pixel.</span><span class="sxs-lookup"><span data-stu-id="748d5-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="748d5-152">Il valore di profondità viene scritto nel buffer di profondità solo se lo stato di rendering è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="748d5-153">I rasterizzatori software e molti acceleratori hardware funzionano più velocemente se il test di profondità ha esito negativo, perché non è necessario filtrare e modulare la trama se il pixel non verrà sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="748d5-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**</span><span class="sxs-lookup"><span data-stu-id="748d5-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-155">Valore che specifica un valore alfa di riferimento rispetto al quale vengono testati i pixel quando è abilitato il test alfa.</span><span class="sxs-lookup"><span data-stu-id="748d5-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="748d5-156">Si tratta di un valore a 8 bit inserito negli 8 bit bassi del valore dello stato di rendering DWORD.</span><span class="sxs-lookup"><span data-stu-id="748d5-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="748d5-157">I valori possono variare da 0x00000000 a 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="748d5-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="748d5-158">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**</span><span class="sxs-lookup"><span data-stu-id="748d5-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-160">Membro del tipo [**enumerato D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="748d5-161">Il valore predefinito è D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="748d5-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="748d5-162">Questo membro consente a un'applicazione di accettare o rifiutare un pixel, in base al relativo valore alfa.</span><span class="sxs-lookup"><span data-stu-id="748d5-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-164">**TRUE** per abilitare il dithering.</span><span class="sxs-lookup"><span data-stu-id="748d5-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="748d5-165">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-167">**TRUE** per abilitare la trasparenza con alpha blended.</span><span class="sxs-lookup"><span data-stu-id="748d5-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="748d5-168">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="748d5-169">Il tipo di fusione alfa è determinato dagli stati di rendering D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="748d5-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-171">**TRUE per** abilitare la fusione.</span><span class="sxs-lookup"><span data-stu-id="748d5-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="748d5-172">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-172">The default value is **FALSE**.</span></span> <span data-ttu-id="748d5-173">Per altre informazioni sull'uso della fusione blending, vedere [La combinazione di sfumature.](fog.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-175">**TRUE per** abilitare le evidenziazioni speculari.</span><span class="sxs-lookup"><span data-stu-id="748d5-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="748d5-176">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="748d5-177">Le evidenziazioni speculari vengono calcolate come se ogni vertice nell'oggetto acceso fosse all'origine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="748d5-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="748d5-178">In questo modo vengono restituiti i risultati previsti, purché l'oggetto sia modellato intorno all'origine e la distanza dalla luce all'oggetto sia relativamente grande.</span><span class="sxs-lookup"><span data-stu-id="748d5-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="748d5-179">In altri casi, i risultati sono indefiniti.</span><span class="sxs-lookup"><span data-stu-id="748d5-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="748d5-180">Quando questo membro è impostato su **TRUE,** il colore speculare viene aggiunto al colore di base dopo la propagazione della trama ma prima della fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="748d5-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRSCOLOR \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-182">Valore il cui tipo è [**D3DCOLOR.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="748d5-183">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-183">The default value is 0.</span></span> <span data-ttu-id="748d5-184">Per altre informazioni sul colore dei colori, vedere [Color Color (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ OSANNATABLEMODE**</span><span class="sxs-lookup"><span data-stu-id="748d5-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-186">Formula della nebbia da usare per la nebbia in pixel.</span><span class="sxs-lookup"><span data-stu-id="748d5-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="748d5-187">Impostare su uno dei membri del [**tipo enumerato D3DFOGMODE.**](./d3dfogmode.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="748d5-188">Il valore predefinito è D3DFOG \_ NONE.</span><span class="sxs-lookup"><span data-stu-id="748d5-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="748d5-189">Per altre informazioni sulla nebbia dei pixel, vedere [Pixel Fog (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**</span><span class="sxs-lookup"><span data-stu-id="748d5-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-191">Profondità alla quale iniziano gli effetti della sfumatura di pixel o vertici per la modalità nebbia lineare.</span><span class="sxs-lookup"><span data-stu-id="748d5-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="748d5-192">Il valore predefinito è 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-192">The default value is 0.0f.</span></span> <span data-ttu-id="748d5-193">La profondità viene specificata nello spazio mondo per la nebbia dei vertici e nello spazio del dispositivo \[ 0.0, 1.0 o nello spazio mondo per la nebbia \] dei pixel.</span><span class="sxs-lookup"><span data-stu-id="748d5-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="748d5-194">Per la nebbia dei pixel, questi valori si verificano nello spazio del dispositivo quando il sistema usa z per i calcoli della nebbia e lo spazio mondiale quando il sistema usa la nebbia relativa agli occhi (w-nebbia).</span><span class="sxs-lookup"><span data-stu-id="748d5-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="748d5-195">Per altre informazioni, vedere [Parametri di nebbia (Direct3D 9)](fog-parameters.md) e Profondità relativa agli occhi rispetto [a Z.](pixel-fog.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="748d5-196">I valori per questo stato di rendering sono valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="748d5-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="748d5-197">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="748d5-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ OSANNA**</span><span class="sxs-lookup"><span data-stu-id="748d5-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-199">Profondità alla quale terminano gli effetti di sfumatura di pixel o vertici per la modalità nebbia lineare.</span><span class="sxs-lookup"><span data-stu-id="748d5-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="748d5-200">Il valore predefinito è 1,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-200">The default value is 1.0f.</span></span> <span data-ttu-id="748d5-201">La profondità viene specificata nello spazio mondo per la nebbia dei vertici e nello spazio del dispositivo \[ 0.0, 1.0 o nello spazio mondo per la nebbia \] dei pixel.</span><span class="sxs-lookup"><span data-stu-id="748d5-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="748d5-202">Per la nebbia dei pixel, questi valori si verificano nello spazio del dispositivo quando il sistema usa z per i calcoli della nebbia e nello spazio mondiale quando il sistema usa la nebbia relativa agli occhi (w-nebbia).</span><span class="sxs-lookup"><span data-stu-id="748d5-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="748d5-203">Per altre informazioni, vedere [Parametri di nebbia (Direct3D 9)](fog-parameters.md) e Profondità relativa agli occhi rispetto [a Z.](pixel-fog.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="748d5-204">I valori per questo stato di rendering sono valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="748d5-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="748d5-205">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="748d5-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**\_D3DRSDENSITY**</span><span class="sxs-lookup"><span data-stu-id="748d5-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-207">Densità di densità di pixel o vertice usata nelle modalità esponenziali di exp (D3DFOG \_ EXP e D3DFOG \_ EXP2).</span><span class="sxs-lookup"><span data-stu-id="748d5-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="748d5-208">I valori di densità validi sono da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="748d5-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="748d5-209">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="748d5-209">The default value is 1.0.</span></span> <span data-ttu-id="748d5-210">Per altre informazioni, vedere [Parameters (Direct3D 9) .](fog-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="748d5-211">I valori per questo stato di rendering sono valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="748d5-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="748d5-212">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="748d5-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-214">**TRUE per** abilitare il vertice basato su intervalli.</span><span class="sxs-lookup"><span data-stu-id="748d5-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="748d5-215">Il valore predefinito è **FALSE,** nel qual caso il sistema usa un oggetto basato sulla profondità.</span><span class="sxs-lookup"><span data-stu-id="748d5-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="748d5-216">Nel caso di un oggetto basato su intervalli, la distanza di un oggetto dal visualizzatore viene usata per calcolare gli effetti dell'effetto, non la profondità dell'oggetto (ovvero la coordinata z) nella scena.</span><span class="sxs-lookup"><span data-stu-id="748d5-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="748d5-217">Nel caso di un'applicazione basata su intervalli, tutti i metodi dell'intervallo funzionano come di consueto, ad eccezione del fatto che usano l'intervallo anziché la profondità nei calcoli.</span><span class="sxs-lookup"><span data-stu-id="748d5-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="748d5-218">L'intervallo è il fattore corretto da usare per i calcoli dei tempi di calcolo, ma la profondità viene in genere usata perché l'intervallo richiede molto tempo e la profondità è in genere già disponibile.</span><span class="sxs-lookup"><span data-stu-id="748d5-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="748d5-219">L'uso della profondità per calcolare il visore ha l'effetto indesiderato di modificare l'intensità degli oggetti periferici quando l'occhio del visualizzatore si sposta. In questo caso, la profondità cambia e l'intervallo rimane costante.</span><span class="sxs-lookup"><span data-stu-id="748d5-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="748d5-220">Poiché attualmente nessun hardware supporta l'intervallo basato su intervalli per pixel, la correzione dell'intervallo è disponibile solo per vertexrere.</span><span class="sxs-lookup"><span data-stu-id="748d5-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="748d5-221">Per altre informazioni, vedere [VertexBie (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**STENCIL \_ D3DRSABILITA**</span><span class="sxs-lookup"><span data-stu-id="748d5-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-223">**TRUE** per abilitare lo stencil o **FALSE per** disabilitare lo stencil.</span><span class="sxs-lookup"><span data-stu-id="748d5-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="748d5-224">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-224">The default value is **FALSE**.</span></span> <span data-ttu-id="748d5-225">Per altre informazioni, vedere [Stencil Buffer Techniques (Direct3D 9) (Tecniche del buffer degli stencil ( Direct3D 9)](stencil-buffer-techniques.md)).</span><span class="sxs-lookup"><span data-stu-id="748d5-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="748d5-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-227">Operazione di stencil da eseguire se il test di stencil ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="748d5-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="748d5-228">I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="748d5-229">Il valore predefinito è D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="748d5-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="748d5-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-231">Operazione di stencil da eseguire se il test di stencil supera e il test di profondità (z-test) ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="748d5-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="748d5-232">I valori sono del [**tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="748d5-233">Il valore predefinito è D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="748d5-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="748d5-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-235">Operazione di stencil da eseguire se vengono superati sia lo stencil che i test di profondità (z).</span><span class="sxs-lookup"><span data-stu-id="748d5-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="748d5-236">I valori sono del [**tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="748d5-237">Il valore predefinito è D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="748d5-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="748d5-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-239">Funzione di confronto per il test di stencil.</span><span class="sxs-lookup"><span data-stu-id="748d5-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="748d5-240">I valori sono del [**tipo enumerato D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="748d5-241">Il valore predefinito è D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="748d5-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="748d5-242">La funzione di confronto viene usata per confrontare il valore di riferimento con una voce del buffer di stencil.</span><span class="sxs-lookup"><span data-stu-id="748d5-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="748d5-243">Questo confronto si applica solo ai bit nel valore di riferimento e nella voce del buffer di stencil impostati nella maschera di stencil (impostata dallo stato di rendering D3DRS \_ STENCILMASK).</span><span class="sxs-lookup"><span data-stu-id="748d5-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="748d5-244">Se **TRUE,** il test dello stencil viene superato.</span><span class="sxs-lookup"><span data-stu-id="748d5-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**</span><span class="sxs-lookup"><span data-stu-id="748d5-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-246">Valore di riferimento int per il test dello stencil.</span><span class="sxs-lookup"><span data-stu-id="748d5-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="748d5-247">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**</span><span class="sxs-lookup"><span data-stu-id="748d5-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-249">Maschera applicata al valore di riferimento e a ogni voce del buffer degli stencil per determinare i bit significativi per il test dello stencil.</span><span class="sxs-lookup"><span data-stu-id="748d5-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="748d5-250">La maschera predefinita è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="748d5-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**STENCIL \_ D3DRSWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="748d5-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-252">Maschera di scrittura applicata ai valori scritti nel buffer degli stencil.</span><span class="sxs-lookup"><span data-stu-id="748d5-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="748d5-253">La maschera predefinita è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="748d5-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**</span><span class="sxs-lookup"><span data-stu-id="748d5-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-255">Colore usato per la fusione di più trame con l'argomento di fusione della trama D3DTA TFACTOR o l'operazione di fusione della trama \_ D3DTOP \_ BLENDFACTORALPHA.</span><span class="sxs-lookup"><span data-stu-id="748d5-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="748d5-256">Il valore associato è una [**variabile D3DCOLOR.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="748d5-257">Il valore predefinito è bianco opaco (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="748d5-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="748d5-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-259">Comportamento di wrapping della trama per più set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="748d5-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="748d5-260">I valori validi per questo stato di rendering possono essere qualsiasi combinazione dei flag \_ D3DWRAPCOORD 0 (o D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (o D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (o D3DWRAP W) e \_ D3DWRAPCOORD \_ 3.</span><span class="sxs-lookup"><span data-stu-id="748d5-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="748d5-261">In questo modo il sistema esegue il wrapping nella direzione della prima, seconda, terza e quarta dimensione, a volte definita come direzioni s, t, r e q, per una determinata trama.</span><span class="sxs-lookup"><span data-stu-id="748d5-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="748d5-262">Il valore predefinito per questo stato di rendering è 0 (il ritorno a capo è disabilitato in tutte le direzioni).</span><span class="sxs-lookup"><span data-stu-id="748d5-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="748d5-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-264">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="748d5-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-266">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**WRAP D3DRS3 \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-268">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="748d5-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-270">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**WRAP D3DRS5 \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-272">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**WRAP D3DRS6 \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-274">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**WRAP D3DRS7 \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-276">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**RITAGLIO \_ D3DRS**</span><span class="sxs-lookup"><span data-stu-id="748d5-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-278">**TRUE** per abilitare il ritaglio primitivo da Direct3D o **FALSE** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="748d5-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="748d5-279">Il valore predefinito è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**ILLUMINAZIONE \_ D3DRS**</span><span class="sxs-lookup"><span data-stu-id="748d5-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-281">**TRUE** per abilitare l'illuminazione Direct3D o **FALSE** per disabilitarla.</span><span class="sxs-lookup"><span data-stu-id="748d5-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="748d5-282">Il valore predefinito è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-282">The default value is **TRUE**.</span></span> <span data-ttu-id="748d5-283">Vengono accesi correttamente solo i vertici che includono una normale vertice. I vertici che non contengono un normale utilizzano un prodotto punto 0 in tutti i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**AMBIENTE D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-285">Colore della luce ambientale.</span><span class="sxs-lookup"><span data-stu-id="748d5-285">Ambient light color.</span></span> <span data-ttu-id="748d5-286">Questo valore è di tipo [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="748d5-287">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ EVERTEXMODE**</span><span class="sxs-lookup"><span data-stu-id="748d5-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-289">Formula del vertice da usare per il vertice.</span><span class="sxs-lookup"><span data-stu-id="748d5-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="748d5-290">Impostare su un membro del [**tipo enumerato D3DFOGMODE.**](./d3dfogmode.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="748d5-291">Il valore predefinito è D3DFOG \_ NONE.</span><span class="sxs-lookup"><span data-stu-id="748d5-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**</span><span class="sxs-lookup"><span data-stu-id="748d5-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-293">**TRUE** per abilitare il colore per vertice o **FALSE** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="748d5-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="748d5-294">Il valore predefinito è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-294">The default value is **TRUE**.</span></span> <span data-ttu-id="748d5-295">L'abilitazione del colore per vertice consente al sistema di includere il colore definito per i singoli vertici nei calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="748d5-296">Per altre informazioni, vedere gli stati di rendering seguenti:</span><span class="sxs-lookup"><span data-stu-id="748d5-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="748d5-297">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="748d5-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="748d5-298">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="748d5-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="748d5-299">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="748d5-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="748d5-300">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="748d5-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="748d5-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**</span><span class="sxs-lookup"><span data-stu-id="748d5-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-302">**TRUE** per abilitare le evidenziazioni speculari relative alla fotocamera o **FALSE per** usare le evidenziazioni speculari ortogonali.</span><span class="sxs-lookup"><span data-stu-id="748d5-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="748d5-303">Il valore predefinito è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-303">The default value is **TRUE**.</span></span> <span data-ttu-id="748d5-304">Le applicazioni che usano la proiezione ortogonale devono specificare **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**</span><span class="sxs-lookup"><span data-stu-id="748d5-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-306">**TRUE** per abilitare la normalizzazione automatica delle normali dei vertici o **FALSE** per disabilitarla.</span><span class="sxs-lookup"><span data-stu-id="748d5-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="748d5-307">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-307">The default value is **FALSE**.</span></span> <span data-ttu-id="748d5-308">Se si abilita questa funzionalità, il sistema normalizza le normali vertici per i vertici dopo averli trasformati nello spazio della fotocamera, operazione che può richiedere molto tempo a livello di calcolo.</span><span class="sxs-lookup"><span data-stu-id="748d5-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="748d5-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-310">Origine colore diffusa per i calcoli dell'illuminazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="748d5-311">I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="748d5-312">Il valore predefinito è D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="748d5-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="748d5-313">Il valore per questo stato di rendering viene usato solo se lo stato di rendering D3DRS \_ COLORVERTEX è impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="748d5-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-315">Origine di colore speculare per i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="748d5-316">I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="748d5-317">Il valore predefinito è D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="748d5-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="748d5-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-319">Origine dei colori di ambiente per i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="748d5-320">I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="748d5-321">Il valore predefinito è D3DMCS \_ MATERIAL.</span><span class="sxs-lookup"><span data-stu-id="748d5-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="748d5-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-323">Origine del colore emissiva per i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="748d5-324">I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="748d5-325">Il valore predefinito è D3DMCS \_ MATERIAL.</span><span class="sxs-lookup"><span data-stu-id="748d5-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**</span><span class="sxs-lookup"><span data-stu-id="748d5-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-327">Numero di matrici da usare per eseguire la fusione geometrica, se presente.</span><span class="sxs-lookup"><span data-stu-id="748d5-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="748d5-328">I valori validi sono membri del [**tipo enumerato D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="748d5-329">Il valore predefinito è D3DVBF \_ DISABLE.</span><span class="sxs-lookup"><span data-stu-id="748d5-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-331">Abilita o disabilita i piani di ritaglio definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="748d5-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="748d5-332">I valori validi sono qualsiasi DWORD in cui lo stato di ogni bit (impostato o non impostato) attiva o disattiva lo stato di attivazione di un piano di ritaglio corrispondente definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="748d5-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="748d5-333">Il bit meno significativo (bit 0) controlla il primo piano di ritaglio in corrispondenza dell'indice 0 e i bit successivi controllano l'attivazione dei piani di ritaglio in corrispondenza degli indici superiori.</span><span class="sxs-lookup"><span data-stu-id="748d5-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="748d5-334">Se è impostato un bit, il sistema applica il piano di ritaglio appropriato durante il rendering della scena.</span><span class="sxs-lookup"><span data-stu-id="748d5-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="748d5-335">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-335">The default value is 0.</span></span>

<span data-ttu-id="748d5-336">Le macro [**D3DCLIPPLANEn**](d3dclipplanen.md) sono definite per offrire un modo pratico per abilitare i piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="748d5-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**</span><span class="sxs-lookup"><span data-stu-id="748d5-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-338">Valore float che specifica le dimensioni da usare per il calcolo delle dimensioni dei punti nei casi in cui la dimensione del punto non è specificata per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="748d5-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="748d5-339">Questo valore non viene usato quando il vertice contiene dimensioni in punti.</span><span class="sxs-lookup"><span data-stu-id="748d5-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="748d5-340">Questo valore è in unità di spazio dello schermo se D3DRS \_ POINTSCALEENABLE è **FALSE;** in caso contrario, questo valore è in unità di spazio del mondo.</span><span class="sxs-lookup"><span data-stu-id="748d5-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="748d5-341">Il valore predefinito è il valore restituito da un driver.</span><span class="sxs-lookup"><span data-stu-id="748d5-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="748d5-342">Se un driver restituisce 0 o 1, il valore predefinito è 64, che consente l'emulazione delle dimensioni dei punti software.</span><span class="sxs-lookup"><span data-stu-id="748d5-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="748d5-343">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="748d5-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ MIN**</span><span class="sxs-lookup"><span data-stu-id="748d5-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-345">Valore float che specifica la dimensione minima delle primitive di punti.</span><span class="sxs-lookup"><span data-stu-id="748d5-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="748d5-346">Le primitive punto vengono imposte su queste dimensioni durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="748d5-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="748d5-347">L'impostazione di questa proprietà su valori inferiori a 1,0 comporta l'eliminazione dei punti quando il punto non copre un centro pixel e l'antialiasing viene disabilitato o sottoposto a rendering con intensità ridotta quando è abilitato l'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="748d5-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="748d5-348">Il valore predefinito è 1,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-348">The default value is 1.0f.</span></span> <span data-ttu-id="748d5-349">L'intervallo per questo valore è maggiore o uguale a 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="748d5-350">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="748d5-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**PUNTI \_ D3DRSPRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-352">valore bool.</span><span class="sxs-lookup"><span data-stu-id="748d5-352">bool value.</span></span> <span data-ttu-id="748d5-353">Se **TRUE,** le coordinate di trama delle primitive di punto vengono impostate in modo che le trame complete siano mappate su ogni punto.</span><span class="sxs-lookup"><span data-stu-id="748d5-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="748d5-354">Quando **FALSE,** le coordinate della trama dei vertici vengono usate per l'intero punto.</span><span class="sxs-lookup"><span data-stu-id="748d5-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="748d5-355">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-355">The default value is **FALSE**.</span></span> <span data-ttu-id="748d5-356">È possibile ottenere punti a pixel singolo in stile DirectX 7 impostando D3DRS \_ POINTSCALEENABLE su **FALSE** e D3DRS \_ POINTSIZE su 1.0, che sono i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="748d5-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-358">Valore bool che controlla il calcolo delle dimensioni per le primitive di punti.</span><span class="sxs-lookup"><span data-stu-id="748d5-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="748d5-359">Quando **TRUE,** le dimensioni del punto vengono interpretate come un valore dello spazio della fotocamera e vengono ridimensionate dalla funzione distance e dal ridimensionamento dell'asse y del viewport al viewport per calcolare le dimensioni finali del punto dello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="748d5-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="748d5-360">Quando **FALSE,** le dimensioni in punti vengono interpretate come spazio sullo schermo e usate direttamente.</span><span class="sxs-lookup"><span data-stu-id="748d5-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="748d5-361">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**</span><span class="sxs-lookup"><span data-stu-id="748d5-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-363">Valore float che controlla l'attenuazione delle dimensioni basata sulla distanza per le primitive di punto.</span><span class="sxs-lookup"><span data-stu-id="748d5-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="748d5-364">Attivo solo quando D3DRS \_ POINTSCALEENABLE è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="748d5-365">Il valore predefinito è 1,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-365">The default value is 1.0f.</span></span> <span data-ttu-id="748d5-366">L'intervallo per questo valore è maggiore o uguale a 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="748d5-367">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="748d5-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**</span><span class="sxs-lookup"><span data-stu-id="748d5-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-369">Valore float che controlla l'attenuazione delle dimensioni in base alla distanza per le primitive punto.</span><span class="sxs-lookup"><span data-stu-id="748d5-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="748d5-370">Attiva solo quando D3DRS \_ POINTSCALEENABLE è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="748d5-371">Il valore predefinito è 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-371">The default value is 0.0f.</span></span> <span data-ttu-id="748d5-372">L'intervallo per questo valore è maggiore o uguale a 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="748d5-373">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="748d5-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**</span><span class="sxs-lookup"><span data-stu-id="748d5-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-375">Valore float che controlla l'attenuazione delle dimensioni in base alla distanza per le primitive punto.</span><span class="sxs-lookup"><span data-stu-id="748d5-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="748d5-376">Attiva solo quando D3DRS \_ POINTSCALEENABLE è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="748d5-377">Il valore predefinito è 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-377">The default value is 0.0f.</span></span> <span data-ttu-id="748d5-378">L'intervallo per questo valore è maggiore o uguale a 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="748d5-379">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="748d5-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**</span><span class="sxs-lookup"><span data-stu-id="748d5-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-381">Valore bool che determina il modo in cui vengono calcolati i singoli campioni quando si usa un buffer di destinazione di rendering multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="748d5-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="748d5-382">Se impostato su **TRUE,** vengono calcolati più campioni in modo che l'anti-aliasing della scena completa sia eseguito tramite il campionamento in posizioni di campionamento diverse per ogni campione multiplo.</span><span class="sxs-lookup"><span data-stu-id="748d5-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="748d5-383">Se impostato su **FALSE,** tutti i campioni multipli vengono scritti con lo stesso valore di campione, campionato al centro del pixel, che consente il rendering non antialias in un buffer multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="748d5-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="748d5-384">Questo stato di rendering non ha alcun effetto quando si esegue il rendering in un singolo buffer di esempio.</span><span class="sxs-lookup"><span data-stu-id="748d5-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="748d5-385">Il valore predefinito è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**</span><span class="sxs-lookup"><span data-stu-id="748d5-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-387">Ogni bit di questa maschera, a partire dal bit meno significativo (LSB), controlla la modifica di uno degli esempi in una destinazione di rendering multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="748d5-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="748d5-388">Pertanto, per una destinazione di rendering di 8 campioni, il byte basso contiene le otto operazioni di scrittura abilitate per ognuno degli otto campioni.</span><span class="sxs-lookup"><span data-stu-id="748d5-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="748d5-389">Questo stato di rendering non ha alcun effetto quando viene eseguito il rendering in un singolo buffer di esempio.</span><span class="sxs-lookup"><span data-stu-id="748d5-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="748d5-390">Il valore predefinito è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="748d5-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="748d5-391">Questo stato di rendering consente l'uso di un buffer multicampione come buffer di accumulo, eseguendo il rendering multipass della geometria in cui ogni passaggio aggiorna un subset di esempi.</span><span class="sxs-lookup"><span data-stu-id="748d5-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="748d5-392">Se sono presenti n campioni multicampionati e k abilitati, l'intensità risultante dell'immagine sottoposta a rendering deve essere k/n.</span><span class="sxs-lookup"><span data-stu-id="748d5-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="748d5-393">Ogni componente RGB di ogni pixel viene fattoriato da k/n.</span><span class="sxs-lookup"><span data-stu-id="748d5-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-395">Imposta un valore che indica se i bordi delle patch useranno la tessellazione in stile float.</span><span class="sxs-lookup"><span data-stu-id="748d5-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="748d5-396">I valori possibili sono definiti dal [**tipo enumerato D3DPATCHEDGESTYLE.**](./d3dpatchedgestyle.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="748d5-397">Il valore predefinito è D3DPATCHEDGE \_ DISCRETE.</span><span class="sxs-lookup"><span data-stu-id="748d5-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**</span><span class="sxs-lookup"><span data-stu-id="748d5-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-399">Impostare solo per il debug del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="748d5-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="748d5-400">I valori possibili sono definiti dal [**tipo enumerato D3DDEBUGMONITORTOKENS.**](./d3ddebugmonitortokens.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="748d5-401">Si noti che se d3DRS DEBUGMONITORTOKEN è impostato, la chiamata viene considerata come passaggio \_ di un token al monitoraggio di debug.</span><span class="sxs-lookup"><span data-stu-id="748d5-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="748d5-402">Se, ad esempio, dopo aver passato D3DDMT ENABLE o \_ D3DDMT DISABLE a \_ D3DRS DEBUGMONITORTOKEN, vengono passati altri valori di token, lo stato (abilitato o disabilitato) del monitoraggio di debug continuerà a essere \_ persistente.</span><span class="sxs-lookup"><span data-stu-id="748d5-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="748d5-403">Questo stato è utile solo per le build di debug.</span><span class="sxs-lookup"><span data-stu-id="748d5-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="748d5-404">Per impostazione predefinita, il monitoraggio del debug è D3DDMT \_ ENABLE.</span><span class="sxs-lookup"><span data-stu-id="748d5-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="748d5-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-406">Valore float che specifica le dimensioni massime fino a cui verranno ancoraggio gli sprite di punti.</span><span class="sxs-lookup"><span data-stu-id="748d5-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="748d5-407">Il valore deve essere minore o uguale al membro MaxPointSize di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) e maggiore o uguale a D3DRS \_ POINTSIZE \_ MIN.</span><span class="sxs-lookup"><span data-stu-id="748d5-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="748d5-408">Il valore predefinito è 64.0.</span><span class="sxs-lookup"><span data-stu-id="748d5-408">The default value is 64.0.</span></span> <span data-ttu-id="748d5-409">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="748d5-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-411">Valore bool che abilita o disabilita la fusione dei vertici indicizzati.</span><span class="sxs-lookup"><span data-stu-id="748d5-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="748d5-412">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-412">The default value is **FALSE**.</span></span> <span data-ttu-id="748d5-413">Se impostato su **TRUE,** la fusione dei vertici indicizzata è abilitata.</span><span class="sxs-lookup"><span data-stu-id="748d5-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="748d5-414">Se impostata **su FALSE,** la fusione dei vertici indicizzata è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="748d5-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="748d5-415">Se questo stato di rendering è abilitato, l'utente deve passare gli indici di matrice come DWORD di tipo packedcon ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="748d5-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="748d5-416">Quando lo stato di rendering è disabilitato e la fusione dei vertici viene abilitata tramite lo stato VERTEXBLEND D3DRS, equivale a disporre di indici matrice \_ 0, 1, 2, 3 in ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="748d5-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-418">Valore UINT che abilita una scrittura per canale per il buffer dei colori di destinazione del rendering.</span><span class="sxs-lookup"><span data-stu-id="748d5-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="748d5-419">Un bit impostato determina l'aggiornamento del canale colori durante il rendering 3D.</span><span class="sxs-lookup"><span data-stu-id="748d5-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="748d5-420">Un bit chiaro fa in modo che il canale di colore non sia interessato.</span><span class="sxs-lookup"><span data-stu-id="748d5-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="748d5-421">Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS COLORWRITEENABLE è impostato nel membro \_ PrimitiveMiscCaps della [**struttura D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="748d5-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="748d5-422">Questo stato di rendering non influisce sull'operazione di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="748d5-423">Il valore predefinito è 0x0000000F.</span><span class="sxs-lookup"><span data-stu-id="748d5-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="748d5-424">I valori validi per questo stato di rendering possono essere qualsiasi combinazione dei flag D3DCOLORWRITEENABLE \_ ALPHA, D3DCOLORWRITEENABLE \_ BLUE, D3DCOLORWRITEENABLE GREEN o \_ D3DCOLORWRITEENABLE \_ RED.</span><span class="sxs-lookup"><span data-stu-id="748d5-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**</span><span class="sxs-lookup"><span data-stu-id="748d5-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-426">Valore float che controlla il fattore di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="748d5-427">Il valore predefinito è 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-427">The default value is 0.0f.</span></span> <span data-ttu-id="748d5-428">Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="748d5-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**</span><span class="sxs-lookup"><span data-stu-id="748d5-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-430">Valore utilizzato per selezionare l'operazione aritmetica applicata quando lo stato di rendering della fusione alfa, D3DRS \_ ALPHABLENDENABLE, è impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="748d5-431">I valori validi sono definiti dal [**tipo enumerato D3DBLENDOP.**](./d3dblendop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="748d5-432">Il valore predefinito è D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="748d5-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="748d5-433">Se la funzionalità del dispositivo D3DPMISCCAPS BLENDOP non è supportata, viene eseguito \_ D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="748d5-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**</span><span class="sxs-lookup"><span data-stu-id="748d5-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-435">Grado di interpolazione posizione N-patch.</span><span class="sxs-lookup"><span data-stu-id="748d5-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="748d5-436">I valori possono essere D3DDEGREE \_ CUBIC (impostazione predefinita) o D3DDEGREE \_ LINEAR.</span><span class="sxs-lookup"><span data-stu-id="748d5-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="748d5-437">Per altre informazioni, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**</span><span class="sxs-lookup"><span data-stu-id="748d5-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-439">Grado di interpolazione normale con patch a N.</span><span class="sxs-lookup"><span data-stu-id="748d5-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="748d5-440">I valori possono essere D3DDEGREE \_ LINEAR (impostazione predefinita) o D3DDEGREE \_ QUADRATIC.</span><span class="sxs-lookup"><span data-stu-id="748d5-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="748d5-441">Per altre informazioni, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-443">**TRUE** per abilitare il test della forbice e **FALSE** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="748d5-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="748d5-444">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="748d5-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-446">Usato per determinare la quantità di distorsione che può essere applicata alle primitive co-planari per ridurre lo z-fighting.</span><span class="sxs-lookup"><span data-stu-id="748d5-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="748d5-447">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-447">The default value is 0.</span></span>

<span data-ttu-id="748d5-448">bias = (max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="748d5-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="748d5-449">dove max è l'inclinazione massima della profondità del triangolo sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="748d5-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-451">**TRUE** per abilitare l'anti-aliasing delle righe, **FALSE per** disabilitare l'anti-aliasing di riga.</span><span class="sxs-lookup"><span data-stu-id="748d5-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="748d5-452">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="748d5-453">Quando si esegue il rendering in una destinazione di rendering multicampionamento, D3DRS ANTIALIASEDLINEENABLE viene ignorato e viene eseguito il rendering di tutte le \_ righe con alias.</span><span class="sxs-lookup"><span data-stu-id="748d5-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="748d5-454">Usare [**ID3DXLine per**](id3dxline.md) il rendering di linee con antialias in una destinazione di rendering multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="748d5-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="748d5-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-456">Livello minimo a più livelli.</span><span class="sxs-lookup"><span data-stu-id="748d5-456">Minimum tessellation level.</span></span> <span data-ttu-id="748d5-457">Il valore predefinito è 1,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-457">The default value is 1.0f.</span></span> <span data-ttu-id="748d5-458">Vedere [Tessellation (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="748d5-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-460">Livello massimo a tessellazione.</span><span class="sxs-lookup"><span data-stu-id="748d5-460">Maximum tessellation level.</span></span> <span data-ttu-id="748d5-461">Il valore predefinito è 1,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-461">The default value is 1.0f.</span></span> <span data-ttu-id="748d5-462">Vedere [Tessellation (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**</span><span class="sxs-lookup"><span data-stu-id="748d5-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-464">Quantità da a tessellare adattivamente, nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="748d5-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="748d5-465">Il valore predefinito è 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-465">Default value is 0.0f.</span></span> <span data-ttu-id="748d5-466">Vedere [a tessellazione adattiva.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**</span><span class="sxs-lookup"><span data-stu-id="748d5-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-468">Quantità da a tessellare adattivamente, nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="748d5-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="748d5-469">Il valore predefinito è 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-469">Default value is 0.0f.</span></span> <span data-ttu-id="748d5-470">Vedere [a \_ tessellazione adattiva.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**</span><span class="sxs-lookup"><span data-stu-id="748d5-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-472">Quantità da a tessellare adattivamente, nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="748d5-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="748d5-473">Il valore predefinito è 1,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-473">Default value is 1.0f.</span></span> <span data-ttu-id="748d5-474">Vedere [a \_ tessellazione adattiva.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**</span><span class="sxs-lookup"><span data-stu-id="748d5-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-476">Quantità da a tessellare in modo adattivo, nella direzione w.</span><span class="sxs-lookup"><span data-stu-id="748d5-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="748d5-477">Il valore predefinito è 0,0f.</span><span class="sxs-lookup"><span data-stu-id="748d5-477">Default value is 0.0f.</span></span> <span data-ttu-id="748d5-478">Vedere [a \_ tessellazione adattiva.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**</span><span class="sxs-lookup"><span data-stu-id="748d5-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-480">**TRUE** per abilitare la tessellazione adattiva, **FALSE** per disabilitarla.</span><span class="sxs-lookup"><span data-stu-id="748d5-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="748d5-481">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-481">The default value is **FALSE**.</span></span> <span data-ttu-id="748d5-482">Vedere [a \_ tessellazione adattiva.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**</span><span class="sxs-lookup"><span data-stu-id="748d5-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-484">**TRUE** abilita lo stencil su due lati, **FALSE** lo disabilita.</span><span class="sxs-lookup"><span data-stu-id="748d5-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="748d5-485">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-485">The default value is **FALSE**.</span></span> <span data-ttu-id="748d5-486">L'applicazione deve impostare D3DRS \_ CULLMODE su D3DCULL NONE per abilitare la \_ modalità di stencil a due lati.</span><span class="sxs-lookup"><span data-stu-id="748d5-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="748d5-487">Se l'ordine di avvolgimento del triangolo è in senso orario, verranno usate le operazioni D3DRS \_ \* STENCIL.</span><span class="sxs-lookup"><span data-stu-id="748d5-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="748d5-488">Se l'ordine di avvolgimento è in senso antiorario, verranno usate le operazioni \_ CCW STENCIL D3DRS. \_ \*</span><span class="sxs-lookup"><span data-stu-id="748d5-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="748d5-489">Per verificare se lo stencil a due lati è supportato, controllare il membro StencilCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per D3DSTENCILCAPS \_ TWOSIDED.</span><span class="sxs-lookup"><span data-stu-id="748d5-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="748d5-490">Vedere anche [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**STENCIL \_ CCW D3DRSFAIL \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-492">Operazione stencil da eseguire se il test dello stencil CCW ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="748d5-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="748d5-493">I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="748d5-494">Il valore predefinito è D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="748d5-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**\_STENCIL CCW D3DRSZFAIL \_**</span><span class="sxs-lookup"><span data-stu-id="748d5-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-496">Operazione stencil da eseguire se il test dello stencil CCW ha esito positivo e z-test ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="748d5-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="748d5-497">I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="748d5-498">Il valore predefinito è D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="748d5-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="748d5-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-500">Operazione stencil da eseguire se vengono superati sia lo stencil CCW che i test z.</span><span class="sxs-lookup"><span data-stu-id="748d5-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="748d5-501">I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="748d5-502">Il valore predefinito è D3DSTENCILOP \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="748d5-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="748d5-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-504">Funzione di confronto.</span><span class="sxs-lookup"><span data-stu-id="748d5-504">The comparison function.</span></span> <span data-ttu-id="748d5-505">Il test degli stencil CCW viene superato se ((ref & mask) funzione stencil (stencil & mask)) è **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="748d5-506">I valori derivano [**dal tipo enumerato D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="748d5-507">Il valore predefinito è D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="748d5-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="748d5-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-509">Valori ColorWriteEnable aggiuntivi per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="748d5-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="748d5-510">Vedere D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="748d5-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="748d5-511">Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS INDEPENDENTWRITEMASKS è impostato nel membro \_ PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="748d5-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="748d5-512">Il valore predefinito è 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="748d5-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="748d5-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-514">Valori ColorWriteEnable aggiuntivi per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="748d5-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="748d5-515">Vedere D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="748d5-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="748d5-516">Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS INDEPENDENTWRITEMASKS è impostato nel membro \_ PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="748d5-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="748d5-517">Il valore predefinito è 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="748d5-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="748d5-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-519">Valori ColorWriteEnable aggiuntivi per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="748d5-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="748d5-520">Vedere D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="748d5-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="748d5-521">Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS INDEPENDENTWRITEMASKS è impostato nel membro \_ PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="748d5-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="748d5-522">Il valore predefinito è 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="748d5-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="748d5-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-524">[**D3DCOLOR usato**](d3dcolor.md) per un fattore di blend costante durante la fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="748d5-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="748d5-525">Questa funzionalità è disponibile se il bit di funzionalità D3DPBLENDCAPS BLENDFACTOR è impostato nel membro \_ SrcBlendCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o nel membro DestBlendCaps di **D3DCAPS9.**</span><span class="sxs-lookup"><span data-stu-id="748d5-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="748d5-526">Vedere [**D3DRENDERSTATETYPE**]().</span><span class="sxs-lookup"><span data-stu-id="748d5-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="748d5-527">Il valore predefinito è 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="748d5-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-529">Abilitare le scritture della destinazione di rendering per la correzione gamma in sRGB.</span><span class="sxs-lookup"><span data-stu-id="748d5-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="748d5-530">Il formato deve esporre D3DUSAGE \_ SRGBWRITE.</span><span class="sxs-lookup"><span data-stu-id="748d5-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="748d5-531">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="748d5-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-533">Valore a virgola mobile utilizzato per il confronto dei valori di profondità.</span><span class="sxs-lookup"><span data-stu-id="748d5-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="748d5-534">Vedere [Distorsione della profondità (Direct3D 9).](depth-bias.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="748d5-535">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="748d5-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="748d5-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-537">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="748d5-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-539">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="748d5-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-541">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="748d5-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-543">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="748d5-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-545">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="748d5-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-547">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="748d5-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-549">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="748d5-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-551">Vedere D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="748d5-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="748d5-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-553">**TRUE** abilita la modalità di fusione separata per il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="748d5-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="748d5-554">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="748d5-555">Se impostato su **FALSE,** i fattori di fusione della destinazione di rendering e le operazioni applicate al valore alfa devono essere uguali a quelli definiti per il colore.</span><span class="sxs-lookup"><span data-stu-id="748d5-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="748d5-556">Questa modalità viene effettivamente impostata come hardwired su **FALSE** nelle implementazioni che non impostano il limite D3DPMISCCAPS \_ SEPARATEALPHABLEND.</span><span class="sxs-lookup"><span data-stu-id="748d5-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="748d5-557">Vedere [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="748d5-558">Il tipo di fusione alfa separata è determinato dagli stati di rendering D3DRS \_ SRCBLENDALPHA e D3DRS \_ DESTBLENDALPHA.</span><span class="sxs-lookup"><span data-stu-id="748d5-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="748d5-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-560">Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="748d5-561">Questo valore viene ignorato a meno che D3DRS \_ SEPARATEALPHABLENDENABLE non sia **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="748d5-562">Il valore predefinito è D3DBLEND \_ ONE.</span><span class="sxs-lookup"><span data-stu-id="748d5-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="748d5-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-564">Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="748d5-565">Questo valore viene ignorato a meno che D3DRS \_ SEPARATEALPHABLENDENABLE non sia **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="748d5-566">Il valore predefinito è D3DBLEND \_ ZERO.</span><span class="sxs-lookup"><span data-stu-id="748d5-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="748d5-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**</span><span class="sxs-lookup"><span data-stu-id="748d5-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-568">Valore utilizzato per selezionare l'operazione aritmetica applicata alla fusione alfa separata quando lo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE, è impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="748d5-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="748d5-569">I valori validi sono definiti dal [**tipo enumerato D3DBLENDOP.**](./d3dblendop.md)</span><span class="sxs-lookup"><span data-stu-id="748d5-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="748d5-570">Il valore predefinito è D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="748d5-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="748d5-571">Se la funzionalità del dispositivo D3DPMISCCAPS BLENDOP non è supportata, viene eseguito \_ D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="748d5-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="748d5-572">Vedere [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="748d5-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="748d5-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="748d5-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="748d5-574">Forza la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="748d5-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="748d5-575">Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="748d5-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="748d5-576">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="748d5-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="748d5-577">Commenti</span><span class="sxs-lookup"><span data-stu-id="748d5-577">Remarks</span></span>



| <span data-ttu-id="748d5-578">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="748d5-578">Render states</span></span>        |   <span data-ttu-id="748d5-579">Campionatore di trama</span><span class="sxs-lookup"><span data-stu-id="748d5-579">Texture sampler</span></span>                 |
|----------------------|--------------------|
| <span data-ttu-id="748d5-580">ps \_ 1 \_ 1 a ps \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="748d5-580">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="748d5-581">4 campionatori di trama</span><span class="sxs-lookup"><span data-stu-id="748d5-581">4 texture samplers</span></span> |



 

<span data-ttu-id="748d5-582">Direct3D definisce la costante WRAPBIAS D3DRENDERSTATE per consentire alle applicazioni di abilitare o disabilitare il wrapping delle trame, in base all'intero in base zero di un set di coordinate di trama (anziché usare in modo esplicito uno dei valori di stato \_ WRAP n D3DRS). \_</span><span class="sxs-lookup"><span data-stu-id="748d5-582">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="748d5-583">Aggiungere il valore D3DRENDERSTATE WRAPBIAS all'indice in base zero di un set di coordinate di trama per calcolare il valore WRAP n D3DRS corrispondente a tale indice, come illustrato nell'esempio \_ \_ seguente.</span><span class="sxs-lookup"><span data-stu-id="748d5-583">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="748d5-584">Requisiti</span><span class="sxs-lookup"><span data-stu-id="748d5-584">Requirements</span></span>



| <span data-ttu-id="748d5-585">Requisito</span><span class="sxs-lookup"><span data-stu-id="748d5-585">Requirement</span></span> | <span data-ttu-id="748d5-586">Valore</span><span class="sxs-lookup"><span data-stu-id="748d5-586">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="748d5-587">Intestazione</span><span class="sxs-lookup"><span data-stu-id="748d5-587">Header</span></span><br/> | <dl> <span data-ttu-id="748d5-588"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="748d5-588"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="748d5-589">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="748d5-589">See also</span></span>

<dl> <dt>

[<span data-ttu-id="748d5-590">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="748d5-590">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="748d5-591">**IDirect3DDevice9::GetRenderState**</span><span class="sxs-lookup"><span data-stu-id="748d5-591">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="748d5-592">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="748d5-592">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
