---
title: USA variazione naturale
description: USA variazione naturale
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116757"
---
# <a name="use-natural-variation"></a><span data-ttu-id="263d5-103">USA variazione naturale</span><span class="sxs-lookup"><span data-stu-id="263d5-103">Use Natural Variation</span></span>

<span data-ttu-id="263d5-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="263d5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="263d5-105">Sebbene la coerenza della presentazione nell'interfaccia convenzionale dell'applicazione, ad esempio i menu e le finestre di dialogo, renda l'interfaccia più prevedibile, variare l'animazione e l'output parlato nell'interfaccia del carattere.</span><span class="sxs-lookup"><span data-stu-id="263d5-105">While consistency of presentation in your application's conventional interface, such as menus and dialog boxes, makes the interface more predictable, vary the animation and spoken output in the character's interface.</span></span> <span data-ttu-id="263d5-106">La variazione appropriata delle risposte del carattere fornisce un'interfaccia più naturale.</span><span class="sxs-lookup"><span data-stu-id="263d5-106">Appropriately varying the character's responses provides a more natural interface.</span></span> <span data-ttu-id="263d5-107">Se un carattere indirizza sempre l'utente esattamente allo stesso modo; Se ad esempio si dicono sempre le stesse parole, l'utente può prendere in considerazione il carattere noioso, disinteressato o addirittura rude.</span><span class="sxs-lookup"><span data-stu-id="263d5-107">If a character always addresses the user exactly the same way; for example, always saying the same words, the user is likely to consider the character boring, disinterested, or even rude.</span></span> <span data-ttu-id="263d5-108">La comunicazione umana raramente comporta una ripetizione precisa.</span><span class="sxs-lookup"><span data-stu-id="263d5-108">Human communication rarely involves precise repetition.</span></span> <span data-ttu-id="263d5-109">Anche quando si ripete qualcosa in una situazione simile, è possibile modificare il wording, i movimenti o l'espressione facciale.</span><span class="sxs-lookup"><span data-stu-id="263d5-109">Even when repeating something in a similar situation, we may change wording, gestures, or facial expression.</span></span>

<span data-ttu-id="263d5-110">Microsoft Agent consente di compilare alcune varianti per un carattere.</span><span class="sxs-lookup"><span data-stu-id="263d5-110">Microsoft Agent enables you to build in some variation for a character.</span></span> <span data-ttu-id="263d5-111">Quando si definiscono le animazioni di un carattere, è possibile usare le probabilità di diramazione in qualsiasi frame di animazione per modificare un'animazione durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="263d5-111">When defining a character's animations, you can use branching probabilities on any animation frame to change an animation when it plays.</span></span> <span data-ttu-id="263d5-112">È anche possibile assegnare più animazioni a ogni stato.</span><span class="sxs-lookup"><span data-stu-id="263d5-112">You can also assign multiple animations to each state.</span></span> <span data-ttu-id="263d5-113">Microsoft Agent sceglie in modo casuale una delle animazioni assegnate ogni volta che viene avviato uno stato.</span><span class="sxs-lookup"><span data-stu-id="263d5-113">Microsoft Agent randomly chooses one of the assigned animations each time it initiates a state.</span></span> <span data-ttu-id="263d5-114">Per l'output vocale, è anche possibile includere caratteri barra verticale nel testo di output per variare automaticamente il testo parlato.</span><span class="sxs-lookup"><span data-stu-id="263d5-114">For speech output, you can also include vertical bar characters in your output text to automatically vary the text spoken.</span></span> <span data-ttu-id="263d5-115">Microsoft Agent, ad esempio, selezionerà in modo casuale una delle istruzioni seguenti quando si elabora questo testo come parte del metodo [**Speak**](speak-method.md) :</span><span class="sxs-lookup"><span data-stu-id="263d5-115">For example, Microsoft Agent will randomly select one of the following statements when processing this text as part of the [**Speak**](speak-method.md) method:</span></span>

<span data-ttu-id="263d5-116">"Posso dire. \| Posso dirlo. \| Posso pronunciare un altro elemento ".</span><span class="sxs-lookup"><span data-stu-id="263d5-116">"I can say this.\|I can say that.\|I can say something else."</span></span>

 

 




