---
title: Negazione registro di origine
description: Esegue una negazione (y-x) su tutti i componenti del registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044604"
---
# <a name="source-register-negate"></a><span data-ttu-id="741de-103">Negazione registro di origine</span><span class="sxs-lookup"><span data-stu-id="741de-103">Source Register Negate</span></span>

<span data-ttu-id="741de-104">Esegue una negazione (y =-x) su tutti i componenti del registro.</span><span class="sxs-lookup"><span data-stu-id="741de-104">Performs a negate (y = -x), on all register components.</span></span>

## <a name="syntax"></a><span data-ttu-id="741de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="741de-105">Syntax</span></span>


```
- register
```



## <a name="registers"></a><span data-ttu-id="741de-106">Registri</span><span class="sxs-lookup"><span data-stu-id="741de-106">Registers</span></span>

<span data-ttu-id="741de-107">Registro di origine.</span><span class="sxs-lookup"><span data-stu-id="741de-107">Source Register.</span></span> <span data-ttu-id="741de-108">Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="741de-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="741de-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="741de-109">Remarks</span></span>

<span data-ttu-id="741de-110">Il contenuto del registro non è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="741de-110">The contents of the register are not changed.</span></span> <span data-ttu-id="741de-111">Il modificatore viene applicato solo ai dati letti dal registro.</span><span class="sxs-lookup"><span data-stu-id="741de-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="741de-112">L'operazione di negazione viene applicata a tutti e quattro i canali di colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="741de-112">The negate operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="741de-113">Questa operazione viene eseguita dopo tutti gli altri modificatori presenti nello stesso argomento.</span><span class="sxs-lookup"><span data-stu-id="741de-113">This operation is performed after any other modifiers present on the same argument.</span></span>

<span data-ttu-id="741de-114">Questo modificatore si escludono a vicenda con l' [inversione del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) in modo che non possa essere applicato allo stesso registro.</span><span class="sxs-lookup"><span data-stu-id="741de-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="741de-115">Questo modificatore viene utilizzato solo con istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="741de-115">This modifier is for use only with arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="741de-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="741de-116">Example</span></span>

<span data-ttu-id="741de-117">Nell'esempio seguente viene illustrato come utilizzare questo modificatore.</span><span class="sxs-lookup"><span data-stu-id="741de-117">The following example shows how to use this modifier.</span></span>


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a><span data-ttu-id="741de-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="741de-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="741de-119">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="741de-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




