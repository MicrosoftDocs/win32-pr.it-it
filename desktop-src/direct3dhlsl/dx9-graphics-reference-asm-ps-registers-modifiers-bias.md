---
title: Bias del registro di origine
description: Sottrarre 0,5 da tutti i componenti.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955841"
---
# <a name="source-register-bias"></a><span data-ttu-id="775ad-103">Bias del registro di origine</span><span class="sxs-lookup"><span data-stu-id="775ad-103">Source Register Bias</span></span>

<span data-ttu-id="775ad-104">Sottrarre 0,5 da tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="775ad-104">Subtract 0.5 from all components.</span></span>

## <a name="registers"></a><span data-ttu-id="775ad-105">Registri</span><span class="sxs-lookup"><span data-stu-id="775ad-105">Registers</span></span>

<span data-ttu-id="775ad-106">Registro di origine.</span><span class="sxs-lookup"><span data-stu-id="775ad-106">Source register.</span></span> <span data-ttu-id="775ad-107">Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="775ad-107">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="775ad-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="775ad-108">Remarks</span></span>

<span data-ttu-id="775ad-109">Il contenuto del registro non è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="775ad-109">The contents of the register are not changed.</span></span> <span data-ttu-id="775ad-110">Il modificatore viene applicato solo ai dati letti dal registro.</span><span class="sxs-lookup"><span data-stu-id="775ad-110">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="775ad-111">La distorsione viene applicata a tutti e quattro i canali di colore (RGBA) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="775ad-111">The bias is applied to all four color channels (RGBA) as follows:</span></span>


```
output = (input - 0.5)
```



<span data-ttu-id="775ad-112">L'effetto è quello di modificare i dati compresi nell'intervallo compreso tra 0 e 1 in un intervallo compreso tra-0,5 e 0,5.</span><span class="sxs-lookup"><span data-stu-id="775ad-112">The effect is to modify data that was in the range 0 to 1 to be in the range -0.5 to 0.5.</span></span> <span data-ttu-id="775ad-113">L'applicazione di distorsioni ai dati all'esterno di questo intervallo può produrre risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="775ad-113">Applying bias to data outside this range may produce undefined results.</span></span>

> [!Note]  
> <span data-ttu-id="775ad-114">Questo modificatore si escludono a vicenda con il [Registro di origine invertito](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), pertanto non può essere applicato allo stesso registro.</span><span class="sxs-lookup"><span data-stu-id="775ad-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

 

<span data-ttu-id="775ad-115">Questo modificatore viene utilizzato con le istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="775ad-115">This modifier is for use with the arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="775ad-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="775ad-116">Example</span></span>

<span data-ttu-id="775ad-117">Questo esempio esegue la stessa operazione di D3DTOP \_ ADDSIGNED in DirectX 6,0 e 7,0 più sintassi di trama.</span><span class="sxs-lookup"><span data-stu-id="775ad-117">This example performs the same operation as D3DTOP\_ADDSIGNED in DirectX 6.0 and 7.0 multiple texture syntax.</span></span>


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a><span data-ttu-id="775ad-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="775ad-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="775ad-119">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="775ad-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




