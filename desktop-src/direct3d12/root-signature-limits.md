---
title: Limiti della firma radice
description: La firma radice è una proprietà di primo livello e sono previsti limiti e costi severi da considerare.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103579"
---
# <a name="root-signature-limits"></a>Limiti della firma radice

La firma radice è una proprietà di primo livello e sono previsti limiti e costi severi da considerare.

-   [Limiti di memoria e costi](#memory-limits-and-costs)
-   [Costi per le prestazioni](#performance-costs)
-   [Campionatori statici](#static-samplers)
-   [Argomenti correlati](#related-topics)

## <a name="memory-limits-and-costs"></a>Limiti di memoria e costi

La dimensione massima di una firma radice è 64 DWORD.

Questa dimensione massima viene scelta per evitare abusi della firma radice come modalità di archiviazione dei dati in blocco. Ogni voce nella firma radice ha un costo rispetto a questo limite di 64 DWORD:

-   Le tabelle dei descrittori costano 1 DWORD.
-   Le costanti radice costano 1 DWORD, perché sono valori a 32 bit.
-   I descrittori radice (indirizzi virtuali GPU a 64 bit) costano 2 DWORD ciascuno.

I sampler statici non hanno alcun costo nelle dimensioni della firma radice.

## <a name="performance-costs"></a>Costi per le prestazioni

Il costo delle prestazioni (in termini di livelli di riferimento indiretto) è zero per una costante radice, 1 per un descrittore radice e 2 per una tabella descrittore. Se una firma radice è di grandi dimensioni e si verifica un overflow della memoria più veloce in una memoria leggermente più lenta (che può verificarsi in alcuni componenti hardware), aggiungere 1 al costo in termini di prestazioni per gli elementi di overflow alla fine della firma radice.

È possibile che si verifichi un overflow nell'hardware che potrebbe avere, ad esempio, una dimensione fissa di 16 DWORD per lo spazio degli argomenti radice. Questo limite può essere ulteriormente ridotto di uno se viene usato l'assembler di input. In questo caso, se la firma radice è troppo grande per la memoria nativa DWORD 15 o 16, si verifica un overflow in memoria leggermente più lenta. In altri componenti hardware non esiste una memoria di argomenti radice nativa fissa, quindi la situazione di overflow non si verifica mai.

Per tutti i componenti hardware, se viene modificato un argomento radice, il driver deve mantenere una versione di tutti gli argomenti radice (a differenza di altre risorse di archiviazione quali gli heap dei descrittori e le risorse del buffer, che non vengono sottoporre a controllo delle versioni dal driver). Nell'hardware in cui si verifica una situazione di overflow, è necessario eseguire il controllo delle versioni solo dell'area nativa o di overflow, a seconda della posizione in cui si è verificata la modifica. La quantità di controllo delle versioni deve essere ovviamente mantenuta al minimo necessario.

In genere, tenere presenti le linee guida seguenti:

-   Usare una firma radice di dimensioni ridotte in base alle esigenze, anche se bilanciarla con la flessibilità di una firma radice più grande.
-   Disporre i parametri in una firma radice di grandi dimensioni in modo che i parametri con maggiore probabilità vengano modificati spesso o se la latenza di accesso bassa per un determinato parametro è importante, prima di tutto.
-   Se è opportuno, usare le costanti radice o le visualizzazioni di buffer costanti radice per inserire viste del buffer costanti in un heap del descrittore.

## <a name="static-samplers"></a>Campionatori statici

I sampler statici, ovvero i Sampler in cui lo stato è completamente definito e non modificabile, fanno parte delle firme radice, ma non vengono conteggiati per il limite DWORD 64. Se un campionatore può essere definito come statico, non è necessario che il campionatore faccia parte di un heap del descrittore.

Non vi sono costi in termini di prestazioni per l'uso di Sampler statici e una firma radice può contenere una combinazione di Samplers statici (archiviati nella firma radice o nello spazio riservato su alcuni hardware) e i sampler dinamici (archiviati in un heap del descrittore del campionatore). I Sampler in un heap dei descrittori possono essere assegnati dinamicamente e indicizzati, i sampler statici non possono.

I sampler statici possono essere scritti come parte della firma radice in HLSL shader (vedere specificare le [firme radice in HLSL](specifying-root-signatures-in-hlsl.md)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 




