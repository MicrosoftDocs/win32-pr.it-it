---
title: Normalizzazione del testo dei motori di sintesi vocale
description: Normalizzazione del testo dei motori di sintesi vocale
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd195212d52d9107aa8112c156bfd8dd6b33d00d2161bec624d182f0f12f78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347921"
---
# <a name="text-to-speech-engines-text-normalization"></a>Normalizzazione del testo dei motori di sintesi vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

La normalizzazione è il processo di identificazione di numeri, abbreviazioni, acronimi e idiomatici e la loro trasformazione in testo completo in base alle esigenze, in genere in base al contesto della frase.

Ad esempio, usando L&H TruVoice American English TTS Engine, la frase :

Re Giorgio VI dell'Regno Unito è decedato il 6 febbraio 1952.

verrà letto nel **contesto normale** come:

   King King V I of England, died on February 6, february 2.

Ma nel **contesto di posta elettronica**, verrà letto come:

   Re Giorgio, il sesto dell'Italia, è decedito il 6 febbraio, a due anni.

Per informazioni sull'uso del tag **context** speech, vedere la documentazione relativa alla programmazione di Agent Tag di [output vocale di Microsoft Agent.](microsoft-agent-speech-output-tags.md)

 

 




