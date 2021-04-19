---
description: Un segmento di riconoscimento è l'unità di input penna di base che un riconoscimento utilizza internamente per produrre un risultato di riconoscimento per un oggetto Ink specifico.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segmenti di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317913"
---
# <a name="recognition-segments"></a><span data-ttu-id="458fb-103">Segmenti di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="458fb-103">Recognition Segments</span></span>

<span data-ttu-id="458fb-104">Un segmento di riconoscimento è l'unità di input penna di base che un riconoscimento utilizza internamente per produrre un risultato di riconoscimento per un oggetto Ink specifico.</span><span class="sxs-lookup"><span data-stu-id="458fb-104">A recognition segment is the basic ink unit that a recognizer uses internally to produce a recognition result for a particular Ink object.</span></span> <span data-ttu-id="458fb-105">Un segmento di riconoscimento è una raccolta di tratti di input penna.</span><span class="sxs-lookup"><span data-stu-id="458fb-105">A recognition segment is a collection of ink strokes.</span></span> <span data-ttu-id="458fb-106">Ad esempio, un riconoscitore in grado di riconoscere la grafia corsiva in lingua inglese potrebbe usare una parola come segmento di riconoscimento di base.</span><span class="sxs-lookup"><span data-stu-id="458fb-106">For example, a recognizer that is capable of recognizing English cursive handwriting might use a word as the basic recognition segment.</span></span>

<span data-ttu-id="458fb-107">Altri riconoscitori possono usare parti di parole composite come segmenti di base.</span><span class="sxs-lookup"><span data-stu-id="458fb-107">Other recognizers may use parts of composite words as basic segments.</span></span> <span data-ttu-id="458fb-108">In spagnolo, ad esempio, le parole brevi sono comunemente combinate per fornire parole composite più lunghe.</span><span class="sxs-lookup"><span data-stu-id="458fb-108">For example, in Spanish, short words are commonly combined to provide longer composite words.</span></span> <span data-ttu-id="458fb-109">"Damelo" è una parola spagnola composta da tre parole "da me lo" (Dammi), ma viene scritta come una singola parola.</span><span class="sxs-lookup"><span data-stu-id="458fb-109">"Damelo" is a Spanish word that is composed of three words "da me lo" (give me that), but it is written as a single word.</span></span> <span data-ttu-id="458fb-110">Un riconoscitore spagnolo potrebbe riconoscere ogni sottoparola come segmento.</span><span class="sxs-lookup"><span data-stu-id="458fb-110">A Spanish recognizer could recognize each subword as a segment.</span></span>

<span data-ttu-id="458fb-111">Un riconoscitore può trovare diversi modi per suddividere un esempio di input penna in segmenti di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="458fb-111">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="458fb-112">Poiché l'ambiguità è richiesta per riconoscere l'input previsto dall'utente, il riconoscimento può restituire molte corrispondenze alternative.</span><span class="sxs-lookup"><span data-stu-id="458fb-112">Because ambiguity is involved in recognizing the user's intended input, the recognizer can return many alternate matches.</span></span>

<span data-ttu-id="458fb-113">Per ulteriori informazioni sulle alternative, vedere [alternates](alternates.md).</span><span class="sxs-lookup"><span data-stu-id="458fb-113">For more information about alternates, see [Alternates](alternates.md).</span></span>

 

 



