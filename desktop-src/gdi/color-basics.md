---
description: Le funzionalità di colore dei dispositivi, ad esempio display e stampanti, possono variare da monocroma a migliaia di colori.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Nozioni di base sui colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29bcae40ee6771a9c46b892af6e6a8bceb4dcbc6498fb863353d39f92d4c2cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105750"
---
# <a name="color-basics"></a>Nozioni di base sui colori

Le funzionalità di colore dei dispositivi, ad esempio display e stampanti, possono variare da monocroma a migliaia di colori. Poiché un'applicazione potrebbe dover generare output per i dispositivi in questo intervallo, deve essere preparata per gestire diverse funzionalità di colore.

Un'applicazione può individuare il numero di colori disponibili per un determinato dispositivo usando la [**funzione GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) per recuperare il valore NUMCOLORS. Questo valore specifica il numero di colori disponibili per l'uso da parte dell'applicazione. In genere, questo conteggio corrisponde a una proprietà fisica del dispositivo di output, ad esempio il numero di inks nella stampante o il numero di segnali di colore distinti che la scheda di visualizzazione può trasmettere al monitor.

Anche se il valore NUMCOLORS specifica il numero di colori, non identifica i colori disponibili. Un'applicazione può individuare i colori disponibili enumerando tutte le penne di tipo PS \_ SOLID. Poiché il driver di dispositivo che supporta un determinato dispositivo ha in genere una gamma completa di penna a tinta unita e poiché il sistema richiede che le penne a tinta unita hanno solo colori che il dispositivo può generare, l'enumerazione di queste penne è spesso equivalente all'enumerazione dei colori. Un'applicazione può enumerare le penne usando la [**funzione EnumObjects.**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) Per un esempio di codice, vedere [Enumerazione dei colori](enumerating-colors.md).

Per altre informazioni, vedere i seguenti argomenti:

-   [Valori dei colori](color-values.md)
-   [Approssimazioni dei colori e dithering](color-approximations-and-dithering.md)
-   [Colore nelle bitmap](color-in-bitmaps.md)
-   [Combinazione di colori](color-mixing.md)

 

 



