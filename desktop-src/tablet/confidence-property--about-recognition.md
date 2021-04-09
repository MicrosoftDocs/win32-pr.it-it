---
description: Per ottenere un livello di confidenza per ogni risultato del riconoscimento, è possibile ottenere la proprietà confidenza dell'oggetto RecognitionAlternate o la proprietà confidenza dell'oggetto movimento.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Proprietà confidenza [informazioni sul riconoscimento]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878561"
---
# <a name="confidence-property-about-recognition"></a><span data-ttu-id="cdb07-103">Proprietà confidenza \[ sul riconoscimento\]</span><span class="sxs-lookup"><span data-stu-id="cdb07-103">Confidence Property \[About Recognition\]</span></span>

<span data-ttu-id="cdb07-104">Per ottenere un livello di confidenza per ogni risultato del riconoscimento, è possibile ottenere la proprietà [**confidenza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) dell'oggetto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) o la proprietà [**confidenza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) dell'oggetto [**movimento**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .</span><span class="sxs-lookup"><span data-stu-id="cdb07-104">To obtain a level of confidence for each recognition result, you can get either the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) property of the [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object or the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) property of the [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object.</span></span> <span data-ttu-id="cdb07-105">Il livello di confidenza è un numero che indica il livello di confidenza per ogni risultato di riconoscimento alternativo restituito dal riconoscimento per un segmento di riconoscimento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="cdb07-105">The confidence level is a number that indicates the degree of confidence for each alternate recognition result that the recognizer returns for a corresponding recognition segment.</span></span>

<span data-ttu-id="cdb07-106">La confidenza viene restituita come bassa, media o alta.</span><span class="sxs-lookup"><span data-stu-id="cdb07-106">Confidence is returned as low, average, or high.</span></span> <span data-ttu-id="cdb07-107">L'applicazione utilizza questi risultati per:</span><span class="sxs-lookup"><span data-stu-id="cdb07-107">The application uses these results to:</span></span>

-   <span data-ttu-id="cdb07-108">Indicare all'utente che esistono più possibilità.</span><span class="sxs-lookup"><span data-stu-id="cdb07-108">Indicate to the user that multiple possibilities exist.</span></span>
-   <span data-ttu-id="cdb07-109">Classificare le alternative in base al livello di confidenza.</span><span class="sxs-lookup"><span data-stu-id="cdb07-109">Rank the alternates by confidence level.</span></span>

## <a name="what-affects-confidence"></a><span data-ttu-id="cdb07-110">Effetti della sicurezza</span><span class="sxs-lookup"><span data-stu-id="cdb07-110">What Affects Confidence</span></span>

<span data-ttu-id="cdb07-111">Alcuni elementi che rendono difficile il riconoscimento della grafia e influiscono sulla confidenza includono:</span><span class="sxs-lookup"><span data-stu-id="cdb07-111">Some of the things that make handwriting recognition difficult and affect confidence include:</span></span>

-   <span data-ttu-id="cdb07-112">Difficoltà nella determinazione della segmentazione delle parole</span><span class="sxs-lookup"><span data-stu-id="cdb07-112">Difficulty determining word segmentation</span></span>

![immagine che mostra la scrittura troppo vicina](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   <span data-ttu-id="cdb07-114">Problemi tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="cdb07-114">Case difficulties</span></span>

![immagine che mostra difficoltà con le versioni manoscritte della parola "case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   <span data-ttu-id="cdb07-116">Stili di scrittura non comuni</span><span class="sxs-lookup"><span data-stu-id="cdb07-116">Uncommon writing styles</span></span>
-   <span data-ttu-id="cdb07-117">Punteggiatura isolata</span><span class="sxs-lookup"><span data-stu-id="cdb07-117">Isolated punctuation</span></span>

![immagine che mostra le virgolette troppo lontane dal testo](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   <span data-ttu-id="cdb07-119">Caratteri accentati nei riconoscitori inglesi</span><span class="sxs-lookup"><span data-stu-id="cdb07-119">Accented characters in English recognizers</span></span>

> [!Note]  
> <span data-ttu-id="cdb07-120">La valutazione della confidenza è disponibile solo per Stati Uniti inglese e per tutti i riconoscitori di movimento in questa versione.</span><span class="sxs-lookup"><span data-stu-id="cdb07-120">Confidence evaluation is available only for United States English and all gesture recognizers in this release.</span></span> <span data-ttu-id="cdb07-121">I metodi che forniscono la proprietà confidenza per qualsiasi altro riconoscimento restituiranno **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="cdb07-121">Methods that provide the confidence property for any other recognizer will return **E\_NOTIMPL**.</span></span>

 

 

 



