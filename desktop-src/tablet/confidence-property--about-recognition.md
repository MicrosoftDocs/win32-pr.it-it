---
description: Per ottenere un livello di attendibilità per ogni risultato di riconoscimento, è possibile ottenere la proprietà Confidence dell'oggetto RecognitionAlternate o la proprietà Confidence dell'oggetto Gesture.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: proprietà Confidence [Informazioni sul riconoscimento]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3316e9637fe6dcf820f8412724363a25dab65ce9a291b8c3c70c5bcf9c83bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093049"
---
# <a name="confidence-property-about-recognition"></a>Proprietà Confidence \[ Sul riconoscimento\]

Per ottenere un livello di attendibilità per ogni risultato di riconoscimento, è possibile ottenere la proprietà [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) dell'oggetto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) o la proprietà [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) dell'oggetto [**Gesture.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) Il livello di confidenza è un numero che indica il grado di attendibilità per ogni risultato di riconoscimento alternativo restituito dal riconoscimento per un segmento di riconoscimento corrispondente.

L'attendibilità viene restituita come bassa, media o alta. L'applicazione usa questi risultati per:

-   Indicare all'utente che esistono più possibilità.
-   Classificare le alternative in base al livello di confidenza.

## <a name="what-affects-confidence"></a>Effetti dell'attendibilità

Di seguito sono riportati alcuni aspetti che rendono difficile il riconoscimento della grafia e influiscono sull'attendibilità:

-   Difficoltà di determinazione della segmentazione delle parole

![immagine che mostra la scrittura troppo vicina](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Problemi con i casi

![Immagine che mostra le difficoltà con le versioni scritte a mano della parola "case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Stili di scrittura non comuni
-   Punteggiatura isolata

![Immagine che mostra le virgolette troppo distorsi dal testo](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Caratteri accentati nei riconoscitori in lingua inglese

> [!Note]  
> La valutazione dell'attendibilità è disponibile solo per Stati Uniti inglese e per tutti i riconoscitori di movimenti in questa versione. I metodi che forniscono la proprietà di attendibilità per qualsiasi altro riconoscitore restituiranno **E \_ NOTIMPL.**

 

 

 



