---
title: Tipi di dati (HLSL)
description: HLSL supporta molti tipi di dati intrinseci diversi. Questa tabella mostra i tipi da usare per definire le variabili di shader.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c4cb8f6fd15db857daa3005c99381d437a5289f6
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129648"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="08820-104">Tipi di dati (HLSL)</span><span class="sxs-lookup"><span data-stu-id="08820-104">Data Types (HLSL)</span></span>

<span data-ttu-id="08820-105">HLSL supporta molti tipi di dati intrinseci diversi.</span><span class="sxs-lookup"><span data-stu-id="08820-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="08820-106">Questa tabella mostra i tipi da usare per definire le variabili di shader.</span><span class="sxs-lookup"><span data-stu-id="08820-106">This table shows which types to use to define shader variables.</span></span>



| <span data-ttu-id="08820-107">Usare questo tipo intrinseco</span><span class="sxs-lookup"><span data-stu-id="08820-107">Use this intrinsic type</span></span>                                                                                                                         | <span data-ttu-id="08820-108">Per definire questa variabile shader</span><span class="sxs-lookup"><span data-stu-id="08820-108">To define this shader variable</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="08820-109">Scalare</span><span class="sxs-lookup"><span data-stu-id="08820-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="08820-110">Scalare a un componente</span><span class="sxs-lookup"><span data-stu-id="08820-110">One-component scalar</span></span>                       |
| <span data-ttu-id="08820-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="08820-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="08820-112">Vettore o matrice a più componenti</span><span class="sxs-lookup"><span data-stu-id="08820-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="08820-113">[Campionatore,](dx-graphics-hlsl-sampler.md) [trama](dx-graphics-hlsl-texture.md) o [buffer](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="08820-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="08820-114">Campionatore, trama o oggetto buffer</span><span class="sxs-lookup"><span data-stu-id="08820-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="08820-115">[Struct](dx-graphics-hlsl-struct.md), [definito dall'utente](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="08820-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="08820-116">Struttura o typedef personalizzato</span><span class="sxs-lookup"><span data-stu-id="08820-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="08820-117">Array</span><span class="sxs-lookup"><span data-stu-id="08820-117">Array</span></span>                                                                                   | <span data-ttu-id="08820-118">Espressioni scalari letterali dichiarate contenenti la maggior parte degli altri tipi</span><span class="sxs-lookup"><span data-stu-id="08820-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="08820-119">Oggetto State</span><span class="sxs-lookup"><span data-stu-id="08820-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="08820-120">Rappresentazioni HLSL di oggetti di stato</span><span class="sxs-lookup"><span data-stu-id="08820-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="08820-121">Per comprendere meglio come usare vettori e matrici in HLSL, è possibile leggere queste informazioni di base sul modo in cui HLSL usa la matematica [per](dx-graphics-hlsl-per-component-math.md) componente.</span><span class="sxs-lookup"><span data-stu-id="08820-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08820-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08820-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08820-123">Variabili (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08820-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




