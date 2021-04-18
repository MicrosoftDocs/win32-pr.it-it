---
description: Una alternativa è una potenziale corrispondenza di parole per un segmento di riconoscimento. Un riconoscimento genera alternative e le basa sulle corrispondenze accettabili dell'input penna o audio rispetto a un dizionario o a un controllo del controllo.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Glifi alternativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305357"
---
# <a name="alternates"></a><span data-ttu-id="642e1-104">Glifi alternativi</span><span class="sxs-lookup"><span data-stu-id="642e1-104">Alternates</span></span>

<span data-ttu-id="642e1-105">Una alternativa è una potenziale corrispondenza di parole per un segmento di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="642e1-105">An alternate is a potential word match for a recognition segment.</span></span> <span data-ttu-id="642e1-106">Un riconoscimento genera alternative e le basa sulle corrispondenze accettabili dell'input penna o audio rispetto a un dizionario o a un controllo del controllo.</span><span class="sxs-lookup"><span data-stu-id="642e1-106">A recognizer generates alternates and bases them on acceptable matches of the ink or audio input against a dictionary or factoid.</span></span>

> [!Note]  
> <span data-ttu-id="642e1-107">La valutazione della confidenza è attualmente disponibile solo per i riconoscitori Microsoft (Stati Uniti) e di movimento.</span><span class="sxs-lookup"><span data-stu-id="642e1-107">Confidence evaluation is currently available only for the Microsoft English (United States) and gesture recognizers.</span></span>

 

<span data-ttu-id="642e1-108">In alcuni casi l'input penna può avere distinzioni ambigue tra i segmenti.</span><span class="sxs-lookup"><span data-stu-id="642e1-108">Sometimes the ink may have ambiguous distinctions between segments.</span></span> <span data-ttu-id="642e1-109">Il riconoscimento confronta questi segmenti con un dizionario di riconoscimento per determinare le possibili corrispondenze.</span><span class="sxs-lookup"><span data-stu-id="642e1-109">The recognizer compares these segments to a recognizer dictionary to determine possible matches.</span></span> <span data-ttu-id="642e1-110">Quando il riconoscimento Confronta i segmenti, gestisce un elenco di possibili corrispondenze alternative e assegna un livello di confidenza a ognuno, selezionando la scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="642e1-110">When the recognizer compares the segments, it maintains a list of possible alternate matches and assigns a confidence level to each one, picking a top choice.</span></span>

> [!Note]  
> <span data-ttu-id="642e1-111">Il riconoscimento non è in grado di fornire alternative per una parte di input penna inferiore a un segmento di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="642e1-111">The recognizer cannot provide alternates for a portion of ink that is smaller than a recognition segment.</span></span>

 

 

 



