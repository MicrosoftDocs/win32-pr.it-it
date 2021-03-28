---
title: Adattamento con firma del registro di origine
description: Sottrae 0,5 da ogni canale e ridimensiona il risultato per 2,0. Il Nome BX2 deriva da bias e scale-Times-Two, ovvero l'operazione eseguita.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222119"
---
# <a name="source-register-signed-scaling"></a><span data-ttu-id="c3b1f-104">Adattamento con firma del registro di origine</span><span class="sxs-lookup"><span data-stu-id="c3b1f-104">Source Register Signed Scaling</span></span>

<span data-ttu-id="c3b1f-105">Sottrae 0,5 da ogni canale e ridimensiona il risultato per 2,0.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-105">Subtracts 0.5 from each channel and scales the result by 2.0.</span></span> <span data-ttu-id="c3b1f-106">Il Nome BX2 deriva da bias e scale-Times-Two, ovvero l'operazione eseguita.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-106">The name bx2 comes from bias and scale-times-two, which is the operation it performs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b1f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3b1f-107">Syntax</span></span>


```
source register_bx2
```



## <a name="register"></a><span data-ttu-id="c3b1f-108">Registrazione</span><span class="sxs-lookup"><span data-stu-id="c3b1f-108">Register</span></span>

<span data-ttu-id="c3b1f-109">Registro di origine.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-109">Source Register.</span></span> <span data-ttu-id="c3b1f-110">Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="c3b1f-110">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3b1f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3b1f-111">Remarks</span></span>

<span data-ttu-id="c3b1f-112">Questa operazione viene in genere usata per espandere i dati da \[ 0,0 a 1,0 a \] \[ -1,0 a 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="c3b1f-112">This operation is commonly used to expand data from \[0.0 to 1.0\] to \[-1.0 to 1.0\].</span></span> <span data-ttu-id="c3b1f-113">Questo modificatore è progettato per essere utilizzato con le istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-113">This modifier is designed for use with the arithmetic instructions.</span></span> <span data-ttu-id="c3b1f-114">Questo modificatore viene comunemente usato per gli input per l'istruzione del prodotto dot ([DP3-PS](dp3---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="c3b1f-114">This modifier is commonly used on inputs to the dot product instruction ([dp3 - ps](dp3---ps.md)).</span></span> <span data-ttu-id="c3b1f-115">\_L'utilizzo di BX2 su dati non compresi nell'intervallo compreso tra 0 e 1 può produrre risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-115">Using \_bx2 on data outside the range 0 to 1 may produce undefined results.</span></span>

<span data-ttu-id="c3b1f-116">L'operazione di scalabilità con segno viene applicata ai dati letti dal registro prima dell'esecuzione dell'istruzione successiva.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-116">The signed scaling operation is applied to the data read from the register before the next instruction is run.</span></span> <span data-ttu-id="c3b1f-117">L'operazione viene applicata a tutti e quattro i canali di colore (RGBA) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c3b1f-117">The operation is applied to all four color channels (RGBA) as follows:</span></span>


```
y = 2(x - 0.5)
```



<span data-ttu-id="c3b1f-118">Il contenuto del registro non è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-118">The contents of the register are not changed.</span></span> <span data-ttu-id="c3b1f-119">Il modificatore viene applicato solo ai dati letti dal registro.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-119">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="c3b1f-120">Questo modificatore si escludono a vicenda con l' [inversione del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) in modo che non possa essere applicato allo stesso registro.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-120">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="c3b1f-121">Informazioni sulla versione:</span><span class="sxs-lookup"><span data-stu-id="c3b1f-121">Version information:</span></span>

-   <span data-ttu-id="c3b1f-122">Per PS \_ 1 \_ 0 e PS \_ 1 \_ 1, è possibile usare \_ BX2 in qualsiasi registro di origine per le istruzioni di trama nel formato texm3x2 \* e texm3x3 \* .</span><span class="sxs-lookup"><span data-stu-id="c3b1f-122">For ps\_1\_0 and ps\_1\_1, you can use \_bx2 on any source register for texture instructions of the form texm3x2\* and texm3x3\*.</span></span> <span data-ttu-id="c3b1f-123">\_non è possibile usare BX2 in nessuna delle altre istruzioni di trama, ad esempio [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c3b1f-123">\_bx2 cannot be used on any of the other texture instructions such as [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md).</span></span>
-   <span data-ttu-id="c3b1f-124">Per PS \_ 1 \_ 2 e PS \_ 1 \_ 3, è possibile usare \_ BX2 in qualsiasi registro di origine per qualsiasi \* istruzione Tex, eccetto: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) o [texbeml-PS](texbeml---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c3b1f-124">For ps\_1\_2 and ps\_1\_3, you can use \_bx2 on any source register for any tex\* instruction except: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) or [texbeml - ps](texbeml---ps.md).</span></span>

## <a name="example"></a><span data-ttu-id="c3b1f-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="c3b1f-125">Example</span></span>

<span data-ttu-id="c3b1f-126">In questo esempio viene campionata una trama, i dati vengono convertiti nell'intervallo compreso tra-1 e + 1 e viene calcolato un prodotto punto.</span><span class="sxs-lookup"><span data-stu-id="c3b1f-126">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a><span data-ttu-id="c3b1f-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3b1f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3b1f-128">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="c3b1f-128">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




