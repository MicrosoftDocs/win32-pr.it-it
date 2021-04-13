---
title: Prestazioni e utilizzo di memoria in WOW64
description: Le prestazioni e l'utilizzo della memoria in WOW64 sono determinate dai fattori seguenti.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- prestazioni in programmazione Windows WOW64 a 64 bit
- utilizzo di memoria in programmazione Windows WOW64 a 64 bit
- Programmazione Windows WOW64 a 64 bit, prestazioni
- Programmazione Windows WOW64 a 64 bit, utilizzo della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8928e7d50c8396aa2b5b34081af3e4ee2719e044
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399583"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Prestazioni e utilizzo di memoria in WOW64

Le prestazioni e l'utilizzo della memoria in WOW64 sono determinate dai fattori seguenti:

-   Hardware del processore. Viene eseguita l'emulazione di istruzioni sul chip. Nel processore x64, le istruzioni x86 vengono eseguite in modo nativo dal processore. La velocità di esecuzione in WOW64 in x64 è quindi simile alla velocità in Windows a 32 bit. Sul processore Intel Itanium e su tutti i processori di ARM64, viene richiesto un maggior numero di software nell'emulazione e le prestazioni subiscono di conseguenza.
-   Overhead del thunk dell'API. Questo overhead è ridotto rispetto alle chiamate di sistema al kernel NT. Le funzioni kernel NT sono progettate per essere chiamate raramente.
-   Dimensioni della memoria virtuale. Nel processore Intel Itanium, WOW64 aggiunge un sovraccarico significativo se due o più istanze della stessa applicazione a 32 bit vengono eseguite simultaneamente. Ciò è dovuto alle pagine native da 8 KB di Intel Itanium, che complica l'emulazione delle pagine native da 4 KB sull'architettura x86 (altre pagine sono contrassegnate come scrivibili; tutte le pagine scrivibili sono private per il processo). Questo può influire negativamente sulla scalabilità di Servizi terminal in determinati processori. Questo non è il caso del processore x64.
-   Working set. WOW64 aumenta le dimensioni dell'working set dell'applicazione.

WOW64 consente alle applicazioni a 32 bit di sfruttare il kernel a 64 bit. Pertanto, le applicazioni a 32 bit possono utilizzare un numero maggiore di handle di kernel e di finestre. Tuttavia, le applicazioni a 32 bit potrebbero non essere in grado di creare tutti i thread in WOW64 come possono essere eseguiti in modalità nativa su sistemi basati su x86 perché WOW64 alloca un ulteriore stack a 64 bit (in genere 512 KB) per ogni thread. Inoltre, una certa quantità di spazio di indirizzi è riservata per WOW64 e per le strutture di dati utilizzate. La quantità riservata dipende dal processore. altri sono riservati a Intel Itanium rispetto ai processori x64 o ARM64.

Se per l'applicazione è impostato il flag di rilevamento [**\_ \_ \_ indirizzi grande \_**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) per il file di immagine nell'intestazione dell'immagine, ogni applicazione a 32 bit riceve 4 GB di spazio degli indirizzi virtuali nell'ambiente WOW64. Se il flag di rilevamento **\_ \_ \_ indirizzi \_ grande** per il file di immagine non è impostato, ogni applicazione a 32 bit riceve 2 GB di spazio degli indirizzi virtuali nell'ambiente WOW64.

 

 