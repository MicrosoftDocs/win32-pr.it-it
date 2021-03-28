---
title: Registro colori di output
description: I registri di output del colore pixel shader (oC \) sono registri di sola scrittura che restituiscono risultati a più destinazioni di rendering.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399520"
---
# <a name="output-color-register"></a><span data-ttu-id="2cd81-103">Registro colori di output</span><span class="sxs-lookup"><span data-stu-id="2cd81-103">Output Color Register</span></span>

<span data-ttu-id="2cd81-104">I registri di output del colore di pixel shader (oC #) sono registri di sola scrittura che restituiscono risultati a più destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="2cd81-104">The pixel shader color output registers (oC#) are write-only registers that output results to multiple render targets.</span></span>

<span data-ttu-id="2cd81-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cd81-105">Syntax</span></span>



| <span data-ttu-id="2cd81-106">oC #</span><span class="sxs-lookup"><span data-stu-id="2cd81-106">oC#</span></span> |
|------|



 

<span data-ttu-id="2cd81-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="2cd81-107">Where:</span></span>



| <span data-ttu-id="2cd81-108">Nome</span><span class="sxs-lookup"><span data-stu-id="2cd81-108">Name</span></span> | <span data-ttu-id="2cd81-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cd81-109">Description</span></span>       |
|------|-------------------|
| <span data-ttu-id="2cd81-110">oC0</span><span class="sxs-lookup"><span data-stu-id="2cd81-110">oC0</span></span>  | <span data-ttu-id="2cd81-111">destinazione di rendering \# 0</span><span class="sxs-lookup"><span data-stu-id="2cd81-111">render target \#0</span></span> |
| <span data-ttu-id="2cd81-112">oC1</span><span class="sxs-lookup"><span data-stu-id="2cd81-112">oC1</span></span>  | <span data-ttu-id="2cd81-113">destinazione di rendering \# 1</span><span class="sxs-lookup"><span data-stu-id="2cd81-113">render target \#1</span></span> |
| <span data-ttu-id="2cd81-114">oC2</span><span class="sxs-lookup"><span data-stu-id="2cd81-114">oC2</span></span>  | <span data-ttu-id="2cd81-115">destinazione di rendering \# 2</span><span class="sxs-lookup"><span data-stu-id="2cd81-115">render target \#2</span></span> |
| <span data-ttu-id="2cd81-116">oC3</span><span class="sxs-lookup"><span data-stu-id="2cd81-116">oC3</span></span>  | <span data-ttu-id="2cd81-117">destinazione di rendering \# 3</span><span class="sxs-lookup"><span data-stu-id="2cd81-117">render target \#3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2cd81-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cd81-118">Remarks</span></span>

-   <span data-ttu-id="2cd81-119">Se oCn è scritto ma non esiste alcuna destinazione di rendering corrispondente, la scrittura in oCn viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="2cd81-119">If oCn is written but there is no corresponding render target, then this write to oCn is ignored.</span></span>
-   <span data-ttu-id="2cd81-120">Gli Stati di rendering D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 e D3DRS COLORWRITEENABLE3 \_ determinano i componenti di oCn che vengono infine scritti nella destinazione di rendering (dopo Blend, se applicabile).</span><span class="sxs-lookup"><span data-stu-id="2cd81-120">The render states D3DRS\_COLORWRITEENABLE, D3DRS\_COLORWRITEENABLE1, D3DRS\_COLORWRITEENABLE2 and D3DRS\_COLORWRITEENABLE3 determine which components of oCn ultimately get written to the render target (after blend, if applicable).</span></span> <span data-ttu-id="2cd81-121">Se lo shader scrive alcuni ma non tutti i componenti definiti dagli \_ Stati di rendering COLORWRITEENABLE di D3DRS \* per un registro oCn specificato, i canali non scritti producono valori non definiti nella destinazione di rendering corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2cd81-121">If the shader writes some but not all of the components defined by the D3DRS\_COLORWRITEENABLE\* render states for a given oCn register, then the unwritten channels produce undefined values in the corresponding render target.</span></span> <span data-ttu-id="2cd81-122">Se non viene scritto alcun componente di un oCn, la destinazione di rendering corrispondente non deve essere aggiornata (come indicato in precedenza), quindi gli Stati di \_ rendering D3DRS COLORWRITEENABLE non \* si applicano.</span><span class="sxs-lookup"><span data-stu-id="2cd81-122">If none of the components of an oCn are written, the corresponding render target must not be updated at all (as stated above), so the D3DRS\_COLORWRITEENABLE\* render states do not apply.</span></span>

### <a name="shader-model-2-restrictions"></a><span data-ttu-id="2cd81-123">Restrizioni del modello di shader 2</span><span class="sxs-lookup"><span data-stu-id="2cd81-123">Shader Model 2 Restrictions</span></span>

-   <span data-ttu-id="2cd81-124">oCn può essere scritto solo con l'istruzione [MOV-PS](mov---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd81-124">oCn can only be written with the [mov - ps](mov---ps.md) instruction.</span></span>
-   <span data-ttu-id="2cd81-125">oC0 deve essere sempre scritto nello shader.</span><span class="sxs-lookup"><span data-stu-id="2cd81-125">oC0 must be always written in the shader.</span></span>
-   <span data-ttu-id="2cd81-126">Non sono consentiti swizzle di origine (eccetto. xyzw = default swizzle) o modificatore di origine durante la scrittura in qualsiasi oCn.</span><span class="sxs-lookup"><span data-stu-id="2cd81-126">No source swizzle (except .xyzw = default swizzle) or source modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="2cd81-127">Non sono consentite maschere di scrittura di destinazione (eccetto. xyzw = default mask) o il modificatore di istruzione durante la scrittura in qualsiasi oCn.</span><span class="sxs-lookup"><span data-stu-id="2cd81-127">No destination write mask (except .xyzw = default mask) or instruction modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="2cd81-128">Se viene scritto oCn, è necessario scrivere anche oC0-oCn-1.</span><span class="sxs-lookup"><span data-stu-id="2cd81-128">If oCn is written, then oC0 - oCn-1 must also be written.</span></span> <span data-ttu-id="2cd81-129">Ad esempio, per scrivere in oC2, è necessario scrivere anche in oC0 e oC1.</span><span class="sxs-lookup"><span data-stu-id="2cd81-129">For example, to write to oC2, you must also write to oC0 and oC1.</span></span>
-   <span data-ttu-id="2cd81-130">È consentita al massimo una scrittura in qualsiasi numero oC per shader.</span><span class="sxs-lookup"><span data-stu-id="2cd81-130">At most one write to any oC# per shader is allowed.</span></span>
-   <span data-ttu-id="2cd81-131">Per PS \_ 2 \_ x e PS \_ 3 \_ 0, non è possibile scrivere nei registri OC # e od, \# all'interno del controllo di flusso dinamico o predicazione (le Scritture in OC # all'interno del controllo di flusso statico sono belle).</span><span class="sxs-lookup"><span data-stu-id="2cd81-131">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>

### <a name="shader-model-3-restrictions"></a><span data-ttu-id="2cd81-132">Restrizioni del modello di shader 3</span><span class="sxs-lookup"><span data-stu-id="2cd81-132">Shader Model 3 Restrictions</span></span>

-   <span data-ttu-id="2cd81-133">Per PS \_ 3 \_ 0, i registri di output OC # e od \# possono essere scritti un numero qualsiasi di volte.</span><span class="sxs-lookup"><span data-stu-id="2cd81-133">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="2cd81-134">L'output del pixel shader deriva dal contenuto dei registri di output alla fine dell'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="2cd81-134">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="2cd81-135">Se non si verifica una scrittura in un registro di output, probabilmente a causa del controllo di flusso o se lo shader non lo scrive, anche il renderTarget corrispondente non viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="2cd81-135">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding rendertarget is also not updated.</span></span> <span data-ttu-id="2cd81-136">Se viene scritto un subset dei canali in un registro di output, i valori non definiti verranno scritti nei canali rimanenti.</span><span class="sxs-lookup"><span data-stu-id="2cd81-136">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="2cd81-137">Per PS \_ 3 \_ 0, i registri di OC # possono essere scritti con qualsiasi writemasks.</span><span class="sxs-lookup"><span data-stu-id="2cd81-137">For ps\_3\_0, the oC# registers can be written with any writemasks.</span></span>
-   <span data-ttu-id="2cd81-138">Per PS \_ 2 \_ x e PS \_ 3 \_ 0, non è possibile scrivere nei registri OC # e od, \# all'interno del controllo di flusso dinamico o predicazione (le Scritture in OC # all'interno del controllo di flusso statico sono belle).</span><span class="sxs-lookup"><span data-stu-id="2cd81-138">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>
-   <span data-ttu-id="2cd81-139">Non è possibile eseguire alcun calcolo sfumato (o operazioni che richiamano in modo implicito i calcoli delle sfumature, ad esempio [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) all'interno delle istruzioni di controllo di flusso le cui condizioni di diramazione variano in base alle primitive (ad esempio, istruzioni di controllo dinamico del flusso).</span><span class="sxs-lookup"><span data-stu-id="2cd81-139">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="2cd81-140">L'istruzione predicazione non è considerata il controllo dinamico del flusso.</span><span class="sxs-lookup"><span data-stu-id="2cd81-140">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cd81-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2cd81-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd81-142">Registri</span><span class="sxs-lookup"><span data-stu-id="2cd81-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="2cd81-143">Più destinazioni di rendering (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2cd81-143">Multiple Render Targets (Direct3D 9)</span></span>](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 