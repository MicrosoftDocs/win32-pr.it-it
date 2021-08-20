---
description: Descrizione \_ della costante LOCALE ICONSTRUCTEDLOCALE
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 26d54ce55393f54d56f521231e257a8b0692758f8e6c830a890d81c8f82e8422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809639"
---
# <a name="locale_iconstructedlocale"></a>ICONA \_ DELLE IMPOSTAZIONI LOCALISTRUCTEDLOCALE

Identificatore da richiedere se le impostazioni locali sono impostazioni locali "costruite". L'uso di questo LCTYPE è sconsigliato.

Identifica le impostazioni locali per cui Windows molti non hanno informazioni complete e deve "costruire" informazioni in fase di esecuzione. In genere le informazioni fornite da LOCALE_ICONSTRUCTEDLOCALE sono di uso limitato, Windows fornirà la quantità di dati disponibile per tutte le impostazioni locali. Pertanto, l'uso di questo LCTYPE è sconsigliato.


| Valore | Significato                 |
|-------|-------------------------|
| 0     | Non costruito         |
| 1     | Impostazioni locali costruite |


Un esempio potrebbe essere una richiesta per "de-US" o il tedesco nel Stati Uniti. NLS userà i dati in lingua tedesca che può trovare e Stati Uniti'area geografica che può trovare. 

Questo potrebbe non essere perfetto perché, ad esempio, il sistema probabilmente non avrà informazioni sul nome Stati Uniti in tedesco. Tuttavia, se l'applicazione o l'utente desidera un contesto "de-US", i dati restituiti sono i migliori disponibili. 

Le app che usano LOCALE_ICONSTRUCTEDLOCALE per rifiutare le impostazioni locali ed eseguire il fall-back a impostazioni locali diverse in genere hanno un'esperienza peggiore, ad esempio il de-DE o en-US in questo esempio. Nessuno dei due è vicino alla richiesta originale per la lingua tedesca con un'Stati Uniti geografica.

