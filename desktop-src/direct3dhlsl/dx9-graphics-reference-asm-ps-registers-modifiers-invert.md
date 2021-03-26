---
title: Inverti registro di origine
description: Esegue un calcolo (valore 1) per ogni canale del registro specificato.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976167"
---
# <a name="source-register-invert"></a><span data-ttu-id="69a01-103">Inverti registro di origine</span><span class="sxs-lookup"><span data-stu-id="69a01-103">Source Register Invert</span></span>

<span data-ttu-id="69a01-104">Esegue un calcolo (valore 1) per ogni canale del registro specificato.</span><span class="sxs-lookup"><span data-stu-id="69a01-104">Performs a (1 - value) calculation for each channel of the specified register.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69a01-105">Syntax</span></span>


```
1 - register
```



## <a name="registers"></a><span data-ttu-id="69a01-106">Registri</span><span class="sxs-lookup"><span data-stu-id="69a01-106">Registers</span></span>

<span data-ttu-id="69a01-107">Registro di origine.</span><span class="sxs-lookup"><span data-stu-id="69a01-107">Source Register.</span></span> <span data-ttu-id="69a01-108">Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="69a01-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69a01-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="69a01-109">Remarks</span></span>

<span data-ttu-id="69a01-110">Il contenuto del registro non è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="69a01-110">The contents of the register are not changed.</span></span> <span data-ttu-id="69a01-111">Il modificatore viene applicato solo ai dati letti dal registro.</span><span class="sxs-lookup"><span data-stu-id="69a01-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="69a01-112">L'operazione di inversione viene applicata a tutti e quattro i canali di colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="69a01-112">The invert operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="69a01-113">Questo modificatore può essere utilizzato solo con istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="69a01-113">This modifier can be used only with arithmetic instructions.</span></span> <span data-ttu-id="69a01-114">Inoltre, questo modificatore non può essere combinato con l'altra [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="69a01-114">In addition, this modifier cannot be combined with the other [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="example"></a><span data-ttu-id="69a01-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="69a01-115">Example</span></span>

<span data-ttu-id="69a01-116">Questo esempio USA Inversion per generare il complemento del registro R1.</span><span class="sxs-lookup"><span data-stu-id="69a01-116">This example uses inversion to generate the complement of register r1.</span></span>


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a><span data-ttu-id="69a01-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69a01-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a01-118">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="69a01-118">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




