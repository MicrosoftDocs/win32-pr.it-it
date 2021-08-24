---
title: Prestazioni e utilizzo della memoria in WOW64
description: Le prestazioni e l'utilizzo della memoria in WOW64 sono determinati dai fattori seguenti.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- prestazioni in WOW64 a 64 bit Windows programmazione
- utilizzo di memoria in WOW64 a 64 bit Windows programmazione
- WOW64 64-bit Windows programmazione , prestazioni
- WOW64 64-bit Windows programmazione , utilizzo di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d5dd20cb42245318bf2666da788b9eea9e371c3945155c1b03b876fa513f5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613831"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Prestazioni e utilizzo della memoria in WOW64

Le prestazioni e l'utilizzo della memoria in WOW64 sono determinati dai fattori seguenti:

-   Hardware del processore. L'emulazione delle istruzioni viene eseguita sul chip. Nel processore x64 le istruzioni x86 vengono eseguite in modo nativo dal processore. Pertanto, la velocità di esecuzione in WOW64 in x64 è simile alla velocità in condizioni di 32 bit Windows. Nel processore Intel Itanium e in qualsiasi processore ARM64, più software è coinvolto nell'emulazione e di conseguenza le prestazioni ne risentiranno.
-   Sovraccarico del thunk dell'API. Questo sovraccarico è ridotto rispetto alle chiamate di sistema al kernel NT. Le funzioni del kernel NT devono essere chiamate raramente.
-   Dimensioni della memoria virtuale. Nel processore Intel Itanium WOW64 aggiunge un sovraccarico significativo se due o più istanze della stessa applicazione a 32 bit vengono eseguite contemporaneamente. Ciò è dovuto alle pagine native da 8 KB in Intel Itanium, che complica l'emulazione delle pagine native da 4 KB nell'architettura x86 (più pagine sono contrassegnate come scrivibili; tutte le pagine scrivibili sono private per il processo). Ciò può influire negativamente sulla scalabilità di Servizi terminal in determinati processori. Questo non è il caso per il processore x64.
-   Working set. WOW64 aumenta le dimensioni dell'applicazione working set.

WOW64 consente alle applicazioni a 32 bit di sfruttare i vantaggi del kernel a 64 bit. Pertanto, le applicazioni a 32 bit possono usare un numero maggiore di handle del kernel e handle di finestra. Tuttavia, le applicazioni a 32 bit potrebbero non essere in grado di creare il maggior numero possibile di thread in WOW64 quando vengono eseguite in modo nativo in sistemi basati su x86 perché WOW64 alloca uno stack aggiuntivo a 64 bit (in genere 512 KB) per ogni thread. Inoltre, una certa quantità di spazio degli indirizzi è riservata a WOW64 e alle strutture di dati che usa. La quantità riservata dipende dal processore. more è riservato in Intel Itanium rispetto ai processori x64 o ARM64.

Se nell'intestazione dell'immagine è impostato il flag [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE,**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) ogni applicazione a 32 bit riceve 4 GB di spazio degli indirizzi virtuali nell'ambiente WOW64. Se il flag **IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE** non è impostato, ogni applicazione a 32 bit riceve 2 GB di spazio degli indirizzi virtuali nell'ambiente WOW64.

 

 