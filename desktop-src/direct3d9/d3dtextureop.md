---
description: Definisce operazioni di combinazione di trame per fase.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Enumerazione D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354514"
---
# <a name="d3dtextureop-enumeration"></a><span data-ttu-id="a2295-103">Enumerazione D3DTEXTUREOP</span><span class="sxs-lookup"><span data-stu-id="a2295-103">D3DTEXTUREOP enumeration</span></span>

<span data-ttu-id="a2295-104">Definisce operazioni di combinazione di trame per fase.</span><span class="sxs-lookup"><span data-stu-id="a2295-104">Defines per-stage texture-blending operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2295-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2295-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a><span data-ttu-id="a2295-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a2295-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2295-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**\_Disabilitazione D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-108">Disabilita l'output di questa fase di trama e tutte le fasi con un indice superiore.</span><span class="sxs-lookup"><span data-stu-id="a2295-108">Disables output from this texture stage and all stages with a higher index.</span></span> <span data-ttu-id="a2295-109">Per disabilitare il mapping della trama, impostarlo come operazione di colore per la prima fase della trama (fase 0).</span><span class="sxs-lookup"><span data-stu-id="a2295-109">To disable texture mapping, set this as the color operation for the first texture stage (stage 0).</span></span> <span data-ttu-id="a2295-110">Non è possibile disabilitare le operazioni Alpha quando sono abilitate le operazioni sui colori.</span><span class="sxs-lookup"><span data-stu-id="a2295-110">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="a2295-111">L'impostazione dell'operazione Alpha su D3DTOP \_ Disabilita quando è abilitata la fusione dei colori causa un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="a2295-111">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

</dd> <dt>

<span data-ttu-id="a2295-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**\_SELECTARG1 D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP\_SELECTARG1**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-113">Usare il primo colore o l'argomento alfa della fase di trama, senza modifiche, come output.</span><span class="sxs-lookup"><span data-stu-id="a2295-113">Use this texture stage's first color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="a2295-114">Questa operazione influiscono sull'argomento color se usato con lo \_ stato della fase della trama COLOROP di D3DTSS e l'argomento Alpha se usato con D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="a2295-114">This operation affects the color argument when used with the D3DTSS\_COLOROP texture-stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![equazione di questo argomento (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span data-ttu-id="a2295-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**\_SELECTARG2 D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP\_SELECTARG2**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-117">Usare il secondo colore o l'argomento alfa della fase della trama, senza modifiche, come output.</span><span class="sxs-lookup"><span data-stu-id="a2295-117">Use this texture stage's second color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="a2295-118">Questa operazione influiscono sull'argomento color se usato con lo \_ stato della fase della trama COLOROP di D3DTSS e l'argomento Alpha se usato con D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="a2295-118">This operation affects the color argument when used with the D3DTSS\_COLOROP texture stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![equazione di questo argomento (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span data-ttu-id="a2295-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**\_Modulazione D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP\_MODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-121">Moltiplicare i componenti degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="a2295-121">Multiply the components of the arguments.</span></span>

![equazione dell'operazione di modulazione (s (RGBA) = arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span data-ttu-id="a2295-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**\_MODULATE2X D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP\_MODULATE2X**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-124">Moltiplicare i componenti degli argomenti e spostare i prodotti fino a un bit a sinistra (moltiplicando in modo efficace per 2) per schiarire.</span><span class="sxs-lookup"><span data-stu-id="a2295-124">Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening.</span></span>

![equazione dell'operazione modulate2X (s (RGBA) = (arg1 x ARG 2), quindi Shift Left 1)](images/topfrm4.png)

</dd> <dt>

<span data-ttu-id="a2295-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**\_MODULATE4X D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP\_MODULATE4X**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-127">Moltiplicare i componenti degli argomenti e spostare i prodotti verso sinistra a 2 bit (moltiplicando in modo efficace per 4) per schiarire.</span><span class="sxs-lookup"><span data-stu-id="a2295-127">Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening.</span></span>

![equazione dell'operazione Modulate4X (s (RGBA) = (arg1 x ARG 2), quindi Shift Left 2)](images/topfrm5.png)

</dd> <dt>

<span data-ttu-id="a2295-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ aggiungere**</span><span class="sxs-lookup"><span data-stu-id="a2295-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-130">Aggiungere i componenti degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="a2295-130">Add the components of the arguments.</span></span>

![equazione dell'operazione di aggiunta (s (RGBA) = arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span data-ttu-id="a2295-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**\_ADDSIGNED D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP\_ADDSIGNED**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-133">Aggiungere i componenti degli argomenti con una deviazione-0,5, rendendo l'intervallo di valori effettivo compreso tra-0,5 e 0,5.</span><span class="sxs-lookup"><span data-stu-id="a2295-133">Add the components of the arguments with a - 0.5 bias, making the effective range of values from - 0.5 through 0.5.</span></span>

![equazione dell'operazione di aggiunta firmata (s (RGBA) = arg1 + ARG 2-0,5)](images/topfrm7.png)

</dd> <dt>

<span data-ttu-id="a2295-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**\_ADDSIGNED2X D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP\_ADDSIGNED2X**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-136">Aggiungere i componenti degli argomenti con la distorsione-0,5 e spostare i prodotti sul bit a sinistra.</span><span class="sxs-lookup"><span data-stu-id="a2295-136">Add the components of the arguments with a - 0.5 bias, and shift the products to the left 1 bit.</span></span>

![equazione dell'operazione di aggiunta di un 2x firmato ((s (RGBA) = arg1 + ARG 2-0,5), quindi MAIUSC a sinistra 1)](images/topfrm8.png)

</dd> <dt>

<span data-ttu-id="a2295-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**\_Sottrazione D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-139">Sottrarre i componenti del secondo argomento da quelli del primo argomento.</span><span class="sxs-lookup"><span data-stu-id="a2295-139">Subtract the components of the second argument from those of the first argument.</span></span>

![equazione dell'operazione di sottrazione (s (RGBA) = arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span data-ttu-id="a2295-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**\_ADDSMOOTH D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP\_ADDSMOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-142">Aggiungere il primo e il secondo argomento; quindi sottrarre il prodotto dalla somma.</span><span class="sxs-lookup"><span data-stu-id="a2295-142">Add the first and second arguments; then subtract their product from the sum.</span></span>

![equazione dell'aggiunta di operazioni Smooth (s (RGBA) = arg1 + ARG 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span data-ttu-id="a2295-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**\_BLENDDIFFUSEALPHA D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP\_BLENDDIFFUSEALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-145">Combina in modo lineare questa fase della trama, usando l'alfa interpolato da ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="a2295-145">Linearly blend this texture stage, using the interpolated alpha from each vertex.</span></span>

![equazione delle operazioni Alpha Diffusion Blend (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="a2295-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**\_BLENDTEXTUREALPHA D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP\_BLENDTEXTUREALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-148">Combina in modo lineare questa fase della trama, usando l'alfa dalla trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="a2295-148">Linearly blend this texture stage, using the alpha from this stage's texture.</span></span>

![equazione dell'operazione Alpha trama di Blend (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="a2295-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**\_BLENDFACTORALPHA D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP\_BLENDFACTORALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-151">Combina in modo lineare questa fase della trama, usando un set di alfa scalari con lo \_ stato di rendering TEXTUREFACTOR di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="a2295-151">Linearly blend this texture stage, using a scalar alpha set with the D3DRS\_TEXTUREFACTOR render state.</span></span>

![equazione del fattore di fusione Alpha Operation (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="a2295-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**\_BLENDTEXTUREALPHAPM D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP\_BLENDTEXTUREALPHAPM**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-154">Combina in modo lineare una fase di trama che utilizza un valore alfa premoltiplicato.</span><span class="sxs-lookup"><span data-stu-id="a2295-154">Linearly blend a texture stage that uses a premultiplied alpha.</span></span>

![equazione della trama di Blend Alpha PM Operation (s (RGBA) = arg1 + ARG 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span data-ttu-id="a2295-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**\_BLENDCURRENTALPHA D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP\_BLENDCURRENTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-157">Combina in modo lineare questa fase della trama, usando l'alfa tratto dalla fase di trama precedente.</span><span class="sxs-lookup"><span data-stu-id="a2295-157">Linearly blend this texture stage, using the alpha taken from the previous texture stage.</span></span>

![equazione dell'operazione Alpha corrente di Blend (s (RGBA) = arg1 x Alpha + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="a2295-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**\_PREmodulazione D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP\_PREMODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-160">\_La PREmodulazione D3DTOP è impostata nella fase n.</span><span class="sxs-lookup"><span data-stu-id="a2295-160">D3DTOP\_PREMODULATE is set in stage n.</span></span> <span data-ttu-id="a2295-161">L'output della fase n è arg1.</span><span class="sxs-lookup"><span data-stu-id="a2295-161">The output of stage n is arg1.</span></span> <span data-ttu-id="a2295-162">Inoltre, se è presente una trama nella fase n + 1, qualsiasi D3DTA \_ corrente nella fase n + 1 viene premoltiplicato per trama nella fase n + 1.</span><span class="sxs-lookup"><span data-stu-id="a2295-162">Additionally, if there is a texture in stage n + 1, any D3DTA\_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.</span></span>

</dd> <dt>

<span data-ttu-id="a2295-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a2295-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP\_MODULATEALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-164">Modulare il colore del secondo argomento, usando l'alfa del primo argomento; Aggiungere quindi il risultato all'argomento 1.</span><span class="sxs-lookup"><span data-stu-id="a2295-164">Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one.</span></span> <span data-ttu-id="a2295-165">Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="a2295-165">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equazione dell'operazione Alpha di modulazione del colore (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB)](images/topfrm13.png)

</dd> <dt>

<span data-ttu-id="a2295-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2295-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP\_MODULATECOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-168">Modulare gli argomenti; quindi aggiungere l'alfa del primo argomento.</span><span class="sxs-lookup"><span data-stu-id="a2295-168">Modulate the arguments; then add the alpha of the first argument.</span></span> <span data-ttu-id="a2295-169">Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="a2295-169">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equazione dell'operazione di aggiunta del colore Alpha modulate (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span data-ttu-id="a2295-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a2295-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP\_MODULATEINVALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-172">Simile a D3DTOP \_ MODULATEALPHA \_ ADDCOLOR, ma usare l'inverso dell'alfa del primo argomento.</span><span class="sxs-lookup"><span data-stu-id="a2295-172">Similar to D3DTOP\_MODULATEALPHA\_ADDCOLOR, but use the inverse of the alpha of the first argument.</span></span> <span data-ttu-id="a2295-173">Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="a2295-173">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equazione del colore di aggiunta modulazione dell'operazione inversa Alpha (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span data-ttu-id="a2295-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2295-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP\_MODULATEINVCOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-176">Simile a D3DTOP \_ MODULATECOLOR \_ ADDALPHA, ma usare l'inverso del colore del primo argomento.</span><span class="sxs-lookup"><span data-stu-id="a2295-176">Similar to D3DTOP\_MODULATECOLOR\_ADDALPHA, but use the inverse of the color of the first argument.</span></span> <span data-ttu-id="a2295-177">Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="a2295-177">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equazione dell'operazione di aggiunta del colore inverso Alpha modulazione (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span data-ttu-id="a2295-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**\_BUMPENVMAP D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP\_BUMPENVMAP**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-180">Eseguire il mapping dei riscontri per pixel, usando la mappa dell'ambiente nella fase di trama successiva, senza luminanza.</span><span class="sxs-lookup"><span data-stu-id="a2295-180">Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance.</span></span> <span data-ttu-id="a2295-181">Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="a2295-181">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="a2295-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**\_BUMPENVMAPLUMINANCE D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP\_BUMPENVMAPLUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-183">Eseguire il mapping dei riscontri per pixel, usando la mappa dell'ambiente nella fase di trama successiva, con luminanza.</span><span class="sxs-lookup"><span data-stu-id="a2295-183">Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance.</span></span> <span data-ttu-id="a2295-184">Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="a2295-184">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="a2295-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**\_DOTPRODUCT3 D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP\_DOTPRODUCT3**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-186">Modulare i componenti di ogni argomento come componenti firmati, aggiungere i relativi prodotti; quindi replicare la somma in tutti i canali di colore, incluso Alpha.</span><span class="sxs-lookup"><span data-stu-id="a2295-186">Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha.</span></span> <span data-ttu-id="a2295-187">Questa operazione è supportata per le operazioni di colore e alfa.</span><span class="sxs-lookup"><span data-stu-id="a2295-187">This operation is supported for color and alpha operations.</span></span>

![equazione del prodotto 3 operazione (s (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b)](images/topfrm17.png)

<span data-ttu-id="a2295-189">In DirectX 6 e DirectX 7, le operazioni di multitrama gli input precedenti sono tutte spostate verso la metà (y = x-0,5) prima dell'utilizzo per simulare i dati firmati e il risultato scalare viene automaticamente fissato ai valori positivi e viene replicato in tutti e tre i canali di output.</span><span class="sxs-lookup"><span data-stu-id="a2295-189">In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels.</span></span> <span data-ttu-id="a2295-190">Si noti inoltre che, come operazione di colore, questo non aggiorna l'Alpha aggiorna solo i componenti RGB.</span><span class="sxs-lookup"><span data-stu-id="a2295-190">Also, note that as a color operation this does not updated the alpha it just updates the RGB components.</span></span>

<span data-ttu-id="a2295-191">Tuttavia, nello shader DirectX 8,1 è possibile specificare che l'output venga indirizzato ai componenti. RGB o. a o a entrambi (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a2295-191">However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default).</span></span> <span data-ttu-id="a2295-192">È anche possibile specificare un'operazione scalare separata sul canale alfa.</span><span class="sxs-lookup"><span data-stu-id="a2295-192">You can also specify a separate scalar operation on the alpha channel.</span></span>

</dd> <dt>

<span data-ttu-id="a2295-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**\_MULTIPLYADD D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP\_MULTIPLYADD**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-194">Esegue un'operazione di accumulo di moltiplicazione.</span><span class="sxs-lookup"><span data-stu-id="a2295-194">Performs a multiply-accumulate operation.</span></span> <span data-ttu-id="a2295-195">Accetta gli ultimi due argomenti, li moltiplica insieme, li aggiunge all'argomento di input/origine rimanente e li inserisce nel risultato.</span><span class="sxs-lookup"><span data-stu-id="a2295-195">It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result.</span></span>

<span data-ttu-id="a2295-196">S<sub>RGBA</sub> = arg1 + arg2 \* Arg3</span><span class="sxs-lookup"><span data-stu-id="a2295-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span></span>

</dd> <dt>

<span data-ttu-id="a2295-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**\_LERP D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="a2295-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP\_LERP**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-198">Esegue l'interpolazione lineare tra il secondo e il terzo argomento di origine in base a una proporzione specificata nel primo argomento di origine.</span><span class="sxs-lookup"><span data-stu-id="a2295-198">Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.</span></span>

<span data-ttu-id="a2295-199">S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* arg3.</span><span class="sxs-lookup"><span data-stu-id="a2295-199">S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.</span></span>

</dd> <dt>

<span data-ttu-id="a2295-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a2295-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a2295-201">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a2295-201">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a2295-202">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a2295-202">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a2295-203">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a2295-203">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2295-204">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2295-204">Remarks</span></span>

<span data-ttu-id="a2295-205">I membri di questo tipo vengono usati quando si impostano le operazioni color o Alpha usando i \_ valori D3DTSS COLOROP o D3DTSS \_ ALPHAOP con il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="a2295-205">The members of this type are used when setting color or alpha operations by using the D3DTSS\_COLOROP or D3DTSS\_ALPHAOP values with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span>

<span data-ttu-id="a2295-206">Nelle formule precedenti, S<sub>RGBA</sub> è il colore RGBA prodotto da un'operazione di trama, mentre arg1, arg2 e arg3 rappresentano il colore RGBA completo degli argomenti della trama.</span><span class="sxs-lookup"><span data-stu-id="a2295-206">In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments.</span></span> <span data-ttu-id="a2295-207">I singoli componenti di un argomento vengono visualizzati con pedici.</span><span class="sxs-lookup"><span data-stu-id="a2295-207">Individual components of an argument are shown with subscripts.</span></span> <span data-ttu-id="a2295-208">Ad esempio, il componente alfa per l'argomento 1 verrebbe visualizzato come arg1<sub>A</sub>.</span><span class="sxs-lookup"><span data-stu-id="a2295-208">For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2295-209">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2295-209">Requirements</span></span>



| <span data-ttu-id="a2295-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2295-210">Requirement</span></span> | <span data-ttu-id="a2295-211">Valore</span><span class="sxs-lookup"><span data-stu-id="a2295-211">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2295-212">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2295-212">Header</span></span><br/> | <dl> <span data-ttu-id="a2295-213"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2295-213"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2295-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2295-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2295-215">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="a2295-215">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a2295-216">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a2295-216">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
