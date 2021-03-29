---
title: '\_ \_ modificatori del registro di origine PS 1 4 per texld, texcrd'
description: Due istruzioni per l'indirizzo di trama di pixel shader versione 1 \_ 4, texld-PS \_ 1 \_ 4 e texcrd-PS, hanno una sintassi personalizzata.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "104117257"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a><span data-ttu-id="880ea-103">\_ \_ modificatori del registro di origine PS 1 4 per texld, texcrd</span><span class="sxs-lookup"><span data-stu-id="880ea-103">ps\_1\_4 source register modifiers for texld, texcrd</span></span>

<span data-ttu-id="880ea-104">Due istruzioni per l'indirizzo di trama di pixel shader versione 1 \_ 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) e [texcrd-PS](texcrd---ps.md), hanno una sintassi personalizzata.</span><span class="sxs-lookup"><span data-stu-id="880ea-104">Two pixel shader version 1\_4 texture address instructions, [texld - ps\_1\_4](texld---ps-1-4.md) and [texcrd - ps](texcrd---ps.md), have custom syntax.</span></span> <span data-ttu-id="880ea-105">Queste istruzioni supportano il set di modificatori del registro di origine, i selettori del registro di origine e le maschere di scrittura del registro di destinazione, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="880ea-105">These instructions support their own set of source register modifiers, source register selectors, and destination-register write masks, as shown here.</span></span>

## <a name="source-register-modifiers-for-texld-and-texcrd"></a><span data-ttu-id="880ea-106">Modificatori del registro di origine per texld e texcrd</span><span class="sxs-lookup"><span data-stu-id="880ea-106">Source Register Modifiers for texld and texcrd</span></span>

<span data-ttu-id="880ea-107">Questi modificatori forniscono una funzionalità di divisione proiezioni dividendo i valori x e y in base ai valori z o w.</span><span class="sxs-lookup"><span data-stu-id="880ea-107">These modifiers provide projective divide functionality by dividing the x and y values by either the z or w values.</span></span>



| <span data-ttu-id="880ea-108">Modificatori del registro di origine</span><span class="sxs-lookup"><span data-stu-id="880ea-108">Source register modifiers</span></span> | <span data-ttu-id="880ea-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="880ea-109">Description</span></span>                | <span data-ttu-id="880ea-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="880ea-110">Syntax</span></span>       |
|---------------------------|----------------------------|--------------|
| <span data-ttu-id="880ea-111">\_DZ</span><span class="sxs-lookup"><span data-stu-id="880ea-111">\_dz</span></span>                      | <span data-ttu-id="880ea-112">Dividere i componenti x, y per z</span><span class="sxs-lookup"><span data-stu-id="880ea-112">Divide x,y components by z</span></span> | <span data-ttu-id="880ea-113">Registra \_ DZ</span><span class="sxs-lookup"><span data-stu-id="880ea-113">register\_dz</span></span> |
| <span data-ttu-id="880ea-114">\_db</span><span class="sxs-lookup"><span data-stu-id="880ea-114">\_db</span></span>                      | <span data-ttu-id="880ea-115">Dividere i componenti x, y per z</span><span class="sxs-lookup"><span data-stu-id="880ea-115">Divide x,y components by z</span></span> | <span data-ttu-id="880ea-116">Registra \_ database</span><span class="sxs-lookup"><span data-stu-id="880ea-116">register\_db</span></span> |
| <span data-ttu-id="880ea-117">\_dw</span><span class="sxs-lookup"><span data-stu-id="880ea-117">\_dw</span></span>                      | <span data-ttu-id="880ea-118">Dividere i componenti x, y per w</span><span class="sxs-lookup"><span data-stu-id="880ea-118">Divide x,y components by w</span></span> | <span data-ttu-id="880ea-119">Registra \_ DW</span><span class="sxs-lookup"><span data-stu-id="880ea-119">register\_dw</span></span> |
| <span data-ttu-id="880ea-120">\_da</span><span class="sxs-lookup"><span data-stu-id="880ea-120">\_da</span></span>                      | <span data-ttu-id="880ea-121">Dividere i componenti x, y per w</span><span class="sxs-lookup"><span data-stu-id="880ea-121">Divide x,y components by w</span></span> | <span data-ttu-id="880ea-122">Registra \_ da</span><span class="sxs-lookup"><span data-stu-id="880ea-122">register\_da</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="880ea-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="880ea-123">Remarks</span></span>

<span data-ttu-id="880ea-124">Il \_ \_ modificatore DZ o DB esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="880ea-124">The \_dz or \_db modifier does the following:</span></span>


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



<span data-ttu-id="880ea-125">Il \_ \_ modificatore DW o da esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="880ea-125">The \_dw or \_da modifier does the following:</span></span>


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a><span data-ttu-id="880ea-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="880ea-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="880ea-127">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="880ea-127">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




