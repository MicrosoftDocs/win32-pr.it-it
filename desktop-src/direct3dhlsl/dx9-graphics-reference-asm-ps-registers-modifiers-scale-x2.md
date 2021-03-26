---
title: Scala del registro di origine x 2
description: Moltiplicare il valore per due prima di utilizzarlo nell'istruzione.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976162"
---
# <a name="source-register-scale-x-2"></a><span data-ttu-id="0f0d3-103">Scala del registro di origine x 2</span><span class="sxs-lookup"><span data-stu-id="0f0d3-103">Source Register Scale x 2</span></span>

<span data-ttu-id="0f0d3-104">Moltiplicare il valore per due prima di utilizzarlo nell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="0f0d3-104">Multiply the value by two before using it in the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f0d3-105">Syntax</span></span>


```
register_x2
```



## <a name="register"></a><span data-ttu-id="0f0d3-106">Registrazione</span><span class="sxs-lookup"><span data-stu-id="0f0d3-106">Register</span></span>

<span data-ttu-id="0f0d3-107">Registro di origine.</span><span class="sxs-lookup"><span data-stu-id="0f0d3-107">Source register.</span></span> <span data-ttu-id="0f0d3-108">Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="0f0d3-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f0d3-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f0d3-109">Remarks</span></span>

<span data-ttu-id="0f0d3-110">Il contenuto del registro non è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="0f0d3-110">The contents of the register are not changed.</span></span> <span data-ttu-id="0f0d3-111">Il modificatore viene applicato solo ai dati letti dal registro.</span><span class="sxs-lookup"><span data-stu-id="0f0d3-111">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="0f0d3-112">Questo modificatore si escludono a vicenda con il [Registro di origine invertito](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), pertanto non può essere applicato allo stesso registro.</span><span class="sxs-lookup"><span data-stu-id="0f0d3-112">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

<span data-ttu-id="0f0d3-113">Questo modificatore è disponibile solo per le istruzioni aritmetiche nella versione 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="0f0d3-113">This modifier is only available to arithmetic instructions in version 1\_4.</span></span>

## <a name="example"></a><span data-ttu-id="0f0d3-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f0d3-114">Example</span></span>

<span data-ttu-id="0f0d3-115">In questo esempio viene campionata una trama, i dati vengono convertiti nell'intervallo compreso tra-1 e + 1 e viene calcolato un prodotto punto.</span><span class="sxs-lookup"><span data-stu-id="0f0d3-115">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a><span data-ttu-id="0f0d3-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f0d3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f0d3-117">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="0f0d3-117">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




