---
description: Un effetto (spesso archiviato in un file con estensione FX) dichiara lo stato della pipeline impostato da un effetto.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Formato effetto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401509"
---
# <a name="effect-format-direct3d-10"></a><span data-ttu-id="0a875-103">Formato effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0a875-103">Effect Format (Direct3D 10)</span></span>

<span data-ttu-id="0a875-104">Un effetto (spesso archiviato in un file con estensione FX) dichiara lo stato della pipeline impostato da un effetto.</span><span class="sxs-lookup"><span data-stu-id="0a875-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="0a875-105">Lo stato dell'effetto può essere suddiviso approssimativamente in tre categorie:</span><span class="sxs-lookup"><span data-stu-id="0a875-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="0a875-106">[Variabili](d3d10-effect-variable-syntax.md), generalmente dichiarate all'inizio di un effetto.</span><span class="sxs-lookup"><span data-stu-id="0a875-106">[Variables](d3d10-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="0a875-107">[Funzioni](d3d10-effect-function-syntax.md), che implementano il codice dello shader, o vengono usate come funzioni di supporto da altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="0a875-107">[Functions](d3d10-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="0a875-108">[Una tecnica](d3d10-effect-technique-syntax.md), che implementa sequenze di rendering usando uno o più passaggi di effetto.</span><span class="sxs-lookup"><span data-stu-id="0a875-108">[A technique](d3d10-effect-technique-syntax.md), which implements rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="0a875-109">Ogni sessione imposta uno o più [gruppi di stati](d3d10-effect-states.md) e chiama funzioni shader.</span><span class="sxs-lookup"><span data-stu-id="0a875-109">Each pass sets one or more [state groups](d3d10-effect-states.md) and calls shader functions.</span></span>

![diagramma delle categorie dello stato degli effetti](images/d3d10-effect-intro.png)

<span data-ttu-id="0a875-111">Il diagramma precedente mostra le categorie dello stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="0a875-111">The preceding diagram shows the categories of effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a875-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a875-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a875-113">Riferimento a effetti</span><span class="sxs-lookup"><span data-stu-id="0a875-113">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



