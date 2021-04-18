---
description: Descrizione della \_ costante ICONSTRUCTEDLOCALE delle impostazioni locali
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/30/2021
ms.locfileid: "106334293"
---
# <a name="locale_iconstructedlocale"></a>impostazioni locali \_ ICONSTRUCTEDLOCALE

Identificatore da richiedere se le impostazioni locali sono "costruite". L'uso di questo LCTYPE è sconsigliato.

Identifica le impostazioni locali per le quali Windows non dispone di informazioni complete e deve "costruire" informazioni in fase di esecuzione. In genere le informazioni fornite da LOCALE_ICONSTRUCTEDLOCALE sono di uso limitato poiché Windows fornirà la quantità di dati disponibile per ogni impostazione locale. Pertanto, l'utilizzo di questo LCTYPE è sconsigliato.


| Valore | Significato                 |
|-------|-------------------------|
| 0     | Non costruito         |
| 1     | È un'impostazione locale costruita |


Un esempio potrebbe essere una richiesta di "de-US" o del tedesco nel Stati Uniti. NLS utilizzerà i dati in lingua tedesca che è possibile trovare e i dati Stati Uniti area che è possibile trovare. 

Questo potrebbe non essere perfetto come, ad esempio, il sistema non avrà probabilmente informazioni sul nome di Stati Uniti in tedesco. Tuttavia, se l'applicazione o l'utente desidera un contesto "de-US", i dati restituiti sono i migliori disponibili. 

In questo esempio le app che usano LOCALE_ICONSTRUCTEDLOCALE per rifiutare le impostazioni locali e per eseguire il fallback a impostazioni locali diverse si concludono in modo peggiore, ad esempio per l'atterraggio in de-DE o en-US. Nessuno di questi si avvicina alla richiesta originale per la lingua tedesca con un'area Stati Uniti.

