---
description: Le funzionalità relative ai colori dei dispositivi, ad esempio le visualizzazioni e le stampanti, possono variare da monocromatico a migliaia di colori.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Nozioni di base sui colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226705"
---
# <a name="color-basics"></a>Nozioni di base sui colori

Le funzionalità relative ai colori dei dispositivi, ad esempio le visualizzazioni e le stampanti, possono variare da monocromatico a migliaia di colori. Poiché un'applicazione potrebbe avere la necessità di generare l'output per i dispositivi in tutto questo intervallo, è consigliabile prepararsi a gestire le diverse funzionalità di colore.

Un'applicazione può individuare il numero di colori disponibili per un determinato dispositivo usando la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) per recuperare il valore NUMCOLORS. Questo valore specifica il numero di colori disponibili per l'utilizzo da parte dell'applicazione. In genere, questo conteggio corrisponde a una proprietà fisica del dispositivo di output, ad esempio il numero di inchiostri nella stampante o il numero di segnali di colore distinti che l'adattatore di visualizzazione può trasmettere al monitor.

Sebbene il valore NUMCOLORS specifichi il numero di colori, non identifica i colori disponibili. Un'applicazione è in grado di individuare i colori disponibili enumerando tutte le penne con il \_ tipo a tinta unita PS. Poiché il driver di dispositivo che supporta un determinato dispositivo ha in genere una gamma completa di penne solide e perché il sistema richiede che le penne solide abbiano solo colori che possono essere generati dal dispositivo, l'enumerazione di tali penne è spesso equivalente all'enumerazione dei colori. Un'applicazione può enumerare le penne usando la funzione [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) . Per un esempio di codice, vedere [enumerazione dei colori](enumerating-colors.md).

Per altre informazioni, vedere i seguenti argomenti:

-   [Valori dei colori](color-values.md)
-   [Approssimazioni di colori e dithering](color-approximations-and-dithering.md)
-   [Colore nelle bitmap](color-in-bitmaps.md)
-   [Combinazione di colori](color-mixing.md)

 

 



