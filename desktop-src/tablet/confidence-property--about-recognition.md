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
# <a name="confidence-property-about-recognition"></a>Proprietà confidenza \[ sul riconoscimento\]

Per ottenere un livello di confidenza per ogni risultato del riconoscimento, è possibile ottenere la proprietà [**confidenza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) dell'oggetto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) o la proprietà [**confidenza**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) dell'oggetto [**movimento**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) . Il livello di confidenza è un numero che indica il livello di confidenza per ogni risultato di riconoscimento alternativo restituito dal riconoscimento per un segmento di riconoscimento corrispondente.

La confidenza viene restituita come bassa, media o alta. L'applicazione utilizza questi risultati per:

-   Indicare all'utente che esistono più possibilità.
-   Classificare le alternative in base al livello di confidenza.

## <a name="what-affects-confidence"></a>Effetti della sicurezza

Alcuni elementi che rendono difficile il riconoscimento della grafia e influiscono sulla confidenza includono:

-   Difficoltà nella determinazione della segmentazione delle parole

![immagine che mostra la scrittura troppo vicina](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Problemi tra maiuscole e minuscole

![immagine che mostra difficoltà con le versioni manoscritte della parola "case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Stili di scrittura non comuni
-   Punteggiatura isolata

![immagine che mostra le virgolette troppo lontane dal testo](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Caratteri accentati nei riconoscitori inglesi

> [!Note]  
> La valutazione della confidenza è disponibile solo per Stati Uniti inglese e per tutti i riconoscitori di movimento in questa versione. I metodi che forniscono la proprietà confidenza per qualsiasi altro riconoscimento restituiranno **E \_ NOTIMPL**.

 

 

 



