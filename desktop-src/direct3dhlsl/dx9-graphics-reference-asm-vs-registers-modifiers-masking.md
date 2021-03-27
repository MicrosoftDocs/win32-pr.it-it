---
title: Mascheramento del registro di destinazione
description: La maschera specifica quali componenti del registro di destinazione verranno aggiornati con il risultato di un'istruzione. I registri di trama includono un set di regole e registri non di trama hanno un altro set di regole.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396406"
---
# <a name="destination-register-masking"></a><span data-ttu-id="877a7-104">Mascheramento del registro di destinazione</span><span class="sxs-lookup"><span data-stu-id="877a7-104">Destination Register Masking</span></span>

<span data-ttu-id="877a7-105">La maschera specifica quali componenti del registro di destinazione verranno aggiornati con il risultato di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="877a7-105">Masking specifies which components of the destination register will be updated with the result of an instruction.</span></span> <span data-ttu-id="877a7-106">I registri di trama includono un set di regole e registri non di trama hanno un altro set di regole.</span><span class="sxs-lookup"><span data-stu-id="877a7-106">Texture registers have one set of rules and nontexture registers have another set of rules.</span></span>

-   <span data-ttu-id="877a7-107">Guida \_ di \_ riferimento \_ alla grafica di DX9 ASM e \_ \_ registri \_ modificatori \_ -questa sezione contiene le regole per l'applicazione delle maschere ai registri di destinazione.</span><span class="sxs-lookup"><span data-stu-id="877a7-107">dx9\_graphics\_reference\_asm\_vs\_registers\_modifiers\_masking - This section contains rules for applying masks to destination registers.</span></span>
-   <span data-ttu-id="877a7-108">\_Maschere registro trama \_ : i registri di trama hanno alcune regole univoche.</span><span class="sxs-lookup"><span data-stu-id="877a7-108">Texture\_Register\_Masks - Texture registers have some unique rules.</span></span>

## <a name="destination-register-masking"></a><span data-ttu-id="877a7-109">Mascheramento del registro di destinazione</span><span class="sxs-lookup"><span data-stu-id="877a7-109">Destination Register Masking</span></span>

<span data-ttu-id="877a7-110">Come illustrato nella tabella seguente, la maschera (dove è uno dei [registri](dx9-graphics-reference-asm-vs-registers.md)di vertex shader di vertex shader validi) può essere applicata ai singoli componenti dei dati vettoriali.</span><span class="sxs-lookup"><span data-stu-id="877a7-110">As shown in the following table, masking (where r is one of the valid vertex shader [Vertex Shader Registers](dx9-graphics-reference-asm-vs-registers.md)) can be applied to the individual components of the vector data.</span></span>



| <span data-ttu-id="877a7-111">Modificatore Component</span><span class="sxs-lookup"><span data-stu-id="877a7-111">Component modifier</span></span> | <span data-ttu-id="877a7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="877a7-112">Description</span></span>      |
|--------------------|------------------|
| <span data-ttu-id="877a7-113">r. {x} {y} {z} {w}</span><span class="sxs-lookup"><span data-stu-id="877a7-113">r.{x}{y}{z}{w}</span></span>     | <span data-ttu-id="877a7-114">Maschera di destinazione</span><span class="sxs-lookup"><span data-stu-id="877a7-114">Destination mask</span></span> |



 

-   <span data-ttu-id="877a7-115">In generale, specificare le maschere di scrittura del registro di destinazione è uno stile di codifica valido.</span><span class="sxs-lookup"><span data-stu-id="877a7-115">In general, specifying destination register write masks is good coding style.</span></span> <span data-ttu-id="877a7-116">Semplifica la lettura e la gestione del codice.</span><span class="sxs-lookup"><span data-stu-id="877a7-116">It makes code easier to read and maintain.</span></span>
-   <span data-ttu-id="877a7-117">È possibile specificare qualsiasi combinazione di componenti (incluso None) a condizione che x preceda y, y preceda z e z preceda w.</span><span class="sxs-lookup"><span data-stu-id="877a7-117">Any combination of components may be specified (including none) as long as x precedes y, y precedes z, and z precedes w.</span></span>
-   <span data-ttu-id="877a7-118">I registri di output opz e oFog devono usare solo una maschera.</span><span class="sxs-lookup"><span data-stu-id="877a7-118">The oPts and oFog output registers must use only one mask.</span></span>
-   <span data-ttu-id="877a7-119">Per alcune istruzioni è necessario che il registro di destinazione usi una singola maschera di scrittura: EXP, EXPP, log, LogP, POW, RCP e rsq.</span><span class="sxs-lookup"><span data-stu-id="877a7-119">Certain instructions require the destination register to use a single write mask: exp, expp, log, logp, pow, rcp, and rsq.</span></span>
-   <span data-ttu-id="877a7-120">Nella versione 1,0, l'istruzione FRC richiede una delle combinazioni di maschere seguenti:. x o. y o. XY.</span><span class="sxs-lookup"><span data-stu-id="877a7-120">In version 1.0, the frc instruction required one of the following mask combinations: .x or .y or .xy.</span></span> <span data-ttu-id="877a7-121">La versione 2,0 non presenta alcuna restrizione mask.</span><span class="sxs-lookup"><span data-stu-id="877a7-121">Version 2.0 has no mask restriction.</span></span>
-   <span data-ttu-id="877a7-122">SinCos richiede una delle combinazioni di maschere seguenti:. x o. y o. xyz.</span><span class="sxs-lookup"><span data-stu-id="877a7-122">sincos requires one of the following mask combinations: .x or .y or .xyz.</span></span>
-   <span data-ttu-id="877a7-123">M3X2 richiede la maschera di scrittura. XY.</span><span class="sxs-lookup"><span data-stu-id="877a7-123">m3x2 requires the .xy write mask.</span></span>
-   <span data-ttu-id="877a7-124">M3X3 e m4x3 richiedono la maschera di scrittura. xyz.</span><span class="sxs-lookup"><span data-stu-id="877a7-124">m3x3 and m4x3 require the .xyz write mask.</span></span>
-   <span data-ttu-id="877a7-125">M3x4 e M4x4 richiedono la maschera di scrittura. xyz o la maschera di scrittura predefinita (xyzw).</span><span class="sxs-lookup"><span data-stu-id="877a7-125">m3x4 and m4x4 require either the .xyz write mask or the default write mask (xyzw).</span></span>

## <a name="texture-register-masks"></a><span data-ttu-id="877a7-126">Maschere registro trama</span><span class="sxs-lookup"><span data-stu-id="877a7-126">Texture Register Masks</span></span>

<span data-ttu-id="877a7-127">Le regole di convalida per l'utilizzo di modificatori sui registri delle coordinate di trama sono più strette rispetto alle regole di convalida per altri registri.</span><span class="sxs-lookup"><span data-stu-id="877a7-127">The validation rules for using modifiers on texture coordinate registers are tighter than the validation rules for other registers.</span></span>

-   <span data-ttu-id="877a7-128">Se viene scritto oTn, è necessario scrivere anche tutti i registri precedenti (oTn-1 ~ oT0).</span><span class="sxs-lookup"><span data-stu-id="877a7-128">If oTn is written, all previous registers (oTn-1 ~ oT0) have to be written as well.</span></span>
-   <span data-ttu-id="877a7-129">La maschera di scrittura "combinata" per qualsiasi \# Registro OT deve essere esattamente una delle seguenti:</span><span class="sxs-lookup"><span data-stu-id="877a7-129">The "combined" write mask for any oT\# register must be exactly one of the following:</span></span>
    -   <span data-ttu-id="877a7-130">.x</span><span class="sxs-lookup"><span data-stu-id="877a7-130">.x</span></span>
    -   <span data-ttu-id="877a7-131">. XY</span><span class="sxs-lookup"><span data-stu-id="877a7-131">.xy</span></span>
    -   <span data-ttu-id="877a7-132">. xyz</span><span class="sxs-lookup"><span data-stu-id="877a7-132">.xyz</span></span>
    -   <span data-ttu-id="877a7-133">. xyzw (che equivale a non usare alcun modificatore di componente)</span><span class="sxs-lookup"><span data-stu-id="877a7-133">.xyzw (which is equivalent to not using any component modifiers)</span></span>

<span data-ttu-id="877a7-134">Ad esempio, un vertex shader può restituire i registri di trama in istruzioni separate.</span><span class="sxs-lookup"><span data-stu-id="877a7-134">For example, a vertex shader can output to texture registers in separate instructions.</span></span>


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



<span data-ttu-id="877a7-135">In alternativa, le istruzioni possono essere combinate.</span><span class="sxs-lookup"><span data-stu-id="877a7-135">Or, the instructions can be combined.</span></span>


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



<span data-ttu-id="877a7-136">Queste restrizioni si applicano solo ai registri delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="877a7-136">These restrictions apply only to the texture coordinate registers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="877a7-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="877a7-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877a7-138">Modificatori del registro vertex shader</span><span class="sxs-lookup"><span data-stu-id="877a7-138">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




