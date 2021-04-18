---
title: Normalizzazione del testo nei motori di sintesi vocale
description: Normalizzazione del testo nei motori di sintesi vocale
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298217"
---
# <a name="text-to-speech-engines-text-normalization"></a>Normalizzazione del testo nei motori di sintesi vocale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

La normalizzazione è il processo di identificazione di numeri, abbreviazioni, acronimi e idiomatics e di trasformarli in testo completo, in base alle esigenze, in genere in base al contesto della frase.

Ad esempio, usando il motore di sintesi vocale L&H TruVoice American English, la frase:

Il re Giorgio VI d'Inghilterra è morto il 6 febbraio 1952.

verrà letto nel **contesto normale** come:

   King Giorgio V I di England, è morto il 6 febbraio 19 52.

Tuttavia, nel **contesto del messaggio di posta elettronica** verrà letto come:

   Re Giorgio il sesto d'Inghilterra, morto il sesto febbraio 19 52.

Per informazioni sull'uso del tag di riconoscimento vocale del **contesto** , vedere la documentazione di programmazione dell'agente tag di output per la [sintesi vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

 




