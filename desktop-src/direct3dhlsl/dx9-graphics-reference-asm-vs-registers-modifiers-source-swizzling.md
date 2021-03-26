---
title: Registro di origine swizzling (HLSL VS Reference)
description: Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo. Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Swizzling non influisce sui dati del registro di origine.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104398324"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a><span data-ttu-id="f9116-105">Registro di origine swizzling (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="f9116-105">Source Register Swizzling (HLSL VS reference)</span></span>

<span data-ttu-id="f9116-106">Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="f9116-106">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span> <span data-ttu-id="f9116-107">Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="f9116-107">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="f9116-108">Swizzling non influisce sui dati del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="f9116-108">Swizzling does not affect the source register data.</span></span>

## <a name="component-swizzling"></a><span data-ttu-id="f9116-109">Swizzling componente</span><span class="sxs-lookup"><span data-stu-id="f9116-109">Component Swizzling</span></span>

<span data-ttu-id="f9116-110">Come illustrato nella tabella seguente, è possibile applicare swizzling ai singoli componenti dei dati del registro di origine (dove sono uno dei registri di input del vertex shader validi [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span><span class="sxs-lookup"><span data-stu-id="f9116-110">As shown in the following table, swizzling can be applied to the individual components of the source register data (where r is one of the valid vertex shader input [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span></span>



| <span data-ttu-id="f9116-111">Modificatore Component</span><span class="sxs-lookup"><span data-stu-id="f9116-111">Component modifier</span></span>                 | <span data-ttu-id="f9116-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9116-112">Description</span></span>    |
|------------------------------------|----------------|
| <span data-ttu-id="f9116-113">r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\]</span><span class="sxs-lookup"><span data-stu-id="f9116-113">r.\[xyzw\]\[xyzw\]\[xyzw\]\[xyzw\]</span></span> | <span data-ttu-id="f9116-114">Swizzle di origine</span><span class="sxs-lookup"><span data-stu-id="f9116-114">Source swizzle</span></span> |



 

-   <span data-ttu-id="f9116-115">Tutti e quattro i componenti vengono sempre copiati.</span><span class="sxs-lookup"><span data-stu-id="f9116-115">All four components are always copied.</span></span> <span data-ttu-id="f9116-116">Se si specificano meno di quattro componenti, l'ultimo componente viene ripetuto (XY indica. XYYY).</span><span class="sxs-lookup"><span data-stu-id="f9116-116">If fewer than four components are specified, the last component is repeated (xy means .xyyy).</span></span> <span data-ttu-id="f9116-117">Se non viene specificato alcun componente, x viene ripetuto (. xxxx).</span><span class="sxs-lookup"><span data-stu-id="f9116-117">If no components are specified, x is repeated (.xxxx).</span></span>
-   <span data-ttu-id="f9116-118">I componenti possono essere visualizzati in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="f9116-118">The components can appear in any order.</span></span> <span data-ttu-id="f9116-119">V0. ywx restituisce V0. ywxx.</span><span class="sxs-lookup"><span data-stu-id="f9116-119">v0.ywx results in v0.ywxx.</span></span>
-   <span data-ttu-id="f9116-120">I componenti RGBA possono essere utilizzati rispettivamente per xyzw (r per x, g per b e così via).</span><span class="sxs-lookup"><span data-stu-id="f9116-120">The rgba components can be used respectively for xyzw (r for x, g for b, etc.).</span></span>
-   <span data-ttu-id="f9116-121">Queste istruzioni implementano il componente singolo del registro di origine swizzles: EXP, EXPP, log, LogP, POW, RCP, RSQ.</span><span class="sxs-lookup"><span data-stu-id="f9116-121">These instructions implement source-register single component swizzles: exp, expp, log, logp, pow, rcp, rsq.</span></span> <span data-ttu-id="f9116-122">Il risultato di queste istruzioni viene copiato in tutti e quattro i componenti del registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f9116-122">The result of these instructions is copied to all four destination register components.</span></span>

<span data-ttu-id="f9116-123">Non è possibile usare swizzling nelle istruzioni [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)e [M4x4-vs](m4x4---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="f9116-123">Swizzling cannot be used on the [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md), and [m4x4 - vs](m4x4---vs.md) instructions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9116-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9116-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9116-125">Modificatori del registro vertex shader</span><span class="sxs-lookup"><span data-stu-id="f9116-125">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




