---
description: Un riconoscitore può trovare diversi modi per suddividere un esempio di input penna in segmenti di riconoscimento. Per questo motivo, il numero di alternative di riconoscimento può essere scaglionato, anche per un piccolo esempio di input penna.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmenti di input penna e alternative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049461"
---
# <a name="ink-segments-and-alternates"></a><span data-ttu-id="a650e-104">Segmenti di input penna e alternative</span><span class="sxs-lookup"><span data-stu-id="a650e-104">Ink Segments and Alternates</span></span>

<span data-ttu-id="a650e-105">Un riconoscitore può trovare diversi modi per suddividere un esempio di input penna in segmenti di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="a650e-105">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="a650e-106">Per questo motivo, il numero di alternative di riconoscimento può essere scaglionato, anche per un piccolo esempio di input penna.</span><span class="sxs-lookup"><span data-stu-id="a650e-106">Because of this, the number of recognition alternates may be staggering, even for a small ink sample.</span></span>

<span data-ttu-id="a650e-107">Ad esempio, "t o g e t h e r" possono produrre i risultati seguenti:</span><span class="sxs-lookup"><span data-stu-id="a650e-107">For example, "t o g e t h e r" can yield the following results:</span></span>

-   <span data-ttu-id="a650e-108">"per ottenerlo" (più alternative per ogni parola)</span><span class="sxs-lookup"><span data-stu-id="a650e-108">"to get her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="a650e-109">"da raccogliere" (più alternative per ogni parola)</span><span class="sxs-lookup"><span data-stu-id="a650e-109">"to gather" (plus alternates for each word)</span></span>
-   <span data-ttu-id="a650e-110">"tog ether" (più alternative per ogni parola)</span><span class="sxs-lookup"><span data-stu-id="a650e-110">"tog ether" (plus alternates for each word)</span></span>
-   <span data-ttu-id="a650e-111">"tog" (più alternative per ogni parola)</span><span class="sxs-lookup"><span data-stu-id="a650e-111">"tog at her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="a650e-112">"insieme" (più alternative per la parola)</span><span class="sxs-lookup"><span data-stu-id="a650e-112">"together" (plus alternates for the word)</span></span>

<span data-ttu-id="a650e-113">L'oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) supporta l'archiviazione efficiente di risultati di riconoscimento completi all'interno dell'oggetto [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="a650e-113">The [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object supports efficient storage of full recognition results within the [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="a650e-114">L'oggetto **Ink** esegue il mapping delle alternative di riconoscimento ai tratti nell'oggetto **Ink** e può anche contenere altre informazioni, ad esempio la posizione della linea di base, gli indici di riga e gli intervalli di lingua.</span><span class="sxs-lookup"><span data-stu-id="a650e-114">The **Ink** object maps the recognition alternates to the strokes in the **Ink** object and may also contain other information such as baseline position, line indices, and language ranges.</span></span>

 

 



