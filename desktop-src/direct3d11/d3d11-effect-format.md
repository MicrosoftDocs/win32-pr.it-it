---
title: Formato effetto (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Altre informazioni su: formato effetto (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225628"
---
# <a name="effect-format-direct3d-11"></a><span data-ttu-id="784ba-103">Formato effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="784ba-103">Effect Format (Direct3D 11)</span></span>

<span data-ttu-id="784ba-104">Un effetto (spesso archiviato in un file con estensione FX) dichiara lo stato della pipeline impostato da un effetto.</span><span class="sxs-lookup"><span data-stu-id="784ba-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="784ba-105">Lo stato dell'effetto può essere suddiviso approssimativamente in tre categorie:</span><span class="sxs-lookup"><span data-stu-id="784ba-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="784ba-106">[Variabili](d3d11-effect-variable-syntax.md), generalmente dichiarate all'inizio di un effetto.</span><span class="sxs-lookup"><span data-stu-id="784ba-106">[Variables](d3d11-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="784ba-107">[Funzioni](d3d11-effect-function-syntax.md), che implementano il codice dello shader, o vengono usate come funzioni di supporto da altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="784ba-107">[Functions](d3d11-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="784ba-108">[Tecniche](d3d11-effect-technique-syntax.md), che possono essere disposte in gruppi di effetti e implementare sequenze di rendering usando uno o più passaggi di effetto.</span><span class="sxs-lookup"><span data-stu-id="784ba-108">[Techniques](d3d11-effect-technique-syntax.md), which can be arranged in effect groups, and implement rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="784ba-109">Ogni sessione imposta uno o più [gruppi di stati](d3d11-effect-states.md) e chiama funzioni shader.</span><span class="sxs-lookup"><span data-stu-id="784ba-109">Each pass sets one or more [state groups](d3d11-effect-states.md) and calls shader functions.</span></span>

![diagramma delle categorie di dichiarazioni per gli effetti, incluse le variabili nella parte superiore, funzioni al centro e tecniche nella parte inferiore](images/d3d10-effect-intro.png)

<span data-ttu-id="784ba-111">Il diagramma precedente mostra le categorie dello stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="784ba-111">The preceding diagram shows the categories of effect state.</span></span>

<span data-ttu-id="784ba-112">La definizione del formato binario effetto si trova nel file binario \\ EffectBinaryFormat. h nel codice sorgente degli effetti.</span><span class="sxs-lookup"><span data-stu-id="784ba-112">The definition of the effect binary format can be found in Binary\\EffectBinaryFormat.h in the effects source code.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="784ba-113">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="784ba-113">In this section</span></span>



| <span data-ttu-id="784ba-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="784ba-114">Topic</span></span>                                                                   | <span data-ttu-id="784ba-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="784ba-115">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="784ba-116">Sintassi della variabile Effect</span><span class="sxs-lookup"><span data-stu-id="784ba-116">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)<br/>   | <span data-ttu-id="784ba-117">Una variabile Effect viene dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="784ba-117">An effect variable is declared with the syntax described in this section.</span></span><br/>                                 |
| [<span data-ttu-id="784ba-118">Sintassi dell'annotazione</span><span class="sxs-lookup"><span data-stu-id="784ba-118">Annotation Syntax</span></span>](d3d11-effect-annotation-syntax.md)<br/>      | <span data-ttu-id="784ba-119">Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="784ba-119">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span><br/> |
| [<span data-ttu-id="784ba-120">Sintassi della funzione Effect</span><span class="sxs-lookup"><span data-stu-id="784ba-120">Effect Function Syntax</span></span>](d3d11-effect-function-syntax.md)<br/>   | <span data-ttu-id="784ba-121">Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="784ba-121">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span><br/>          |
| [<span data-ttu-id="784ba-122">Sintassi della tecnica degli effetti</span><span class="sxs-lookup"><span data-stu-id="784ba-122">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)<br/> | <span data-ttu-id="784ba-123">Una tecnica degli effetti viene dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="784ba-123">An effect technique is declared with the syntax described in this section.</span></span><br/>                                |
| [<span data-ttu-id="784ba-124">Gruppi di stati effetti</span><span class="sxs-lookup"><span data-stu-id="784ba-124">Effect State Groups</span></span>](d3d11-effect-states.md)<br/>               | <span data-ttu-id="784ba-125">Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.</span><span class="sxs-lookup"><span data-stu-id="784ba-125">Effect states are name value pairs in the form of an expression.</span></span><br/>                                          |
| [<span data-ttu-id="784ba-126">Sintassi del gruppo di effetti</span><span class="sxs-lookup"><span data-stu-id="784ba-126">Effect Group Syntax</span></span>](d3d11-effect-group-syntax.md)<br/>         | <span data-ttu-id="784ba-127">Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="784ba-127">An effect group is declared with the syntax described in this section.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="784ba-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="784ba-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="784ba-129">Riferimento agli effetti 11</span><span class="sxs-lookup"><span data-stu-id="784ba-129">Effects 11 Reference</span></span>](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





