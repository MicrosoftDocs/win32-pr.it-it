---
title: Filosofia di progettazione delle code di comandi e degli elenchi di comandi
description: Gli obiettivi dell'abilitazione del riutilizzo del lavoro di rendering e della scalabilità multi-thread hanno richiesto modifiche fondamentali al modo in cui le app Direct3D inviano il lavoro di rendering alla GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- elenco dei comandi
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08f996f3de54b63668d44122929feb4fdbef4380fb8b2f7bb1458f50fe274ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124219"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Filosofia di progettazione delle code di comandi e degli elenchi di comandi

Gli obiettivi dell'abilitazione del riutilizzo del lavoro di rendering e della scalabilità multi-thread hanno richiesto modifiche fondamentali al modo in cui le app Direct3D inviano il lavoro di rendering alla GPU. In Direct3D 12 il processo di invio del lavoro di rendering differisce dalle versioni precedenti per tre aspetti importanti:

<dl> 1. Eliminazione del contesto immediato. Ciò consente il multithreading.  
2. Le app ora sono proprietarie del modo in cui le chiamate di rendering vengono raggruppate in elementi di lavoro di unità di elaborazione grafica (GPU). In questo modo è possibile usare di nuovo .  
3. Le app ora controllano in modo esplicito quando il lavoro viene inviato alla GPU. In questo modo vengono abilitati gli elementi 1 e 2.  
</dl>

-   [Rimozione del contesto immediato](#removal-of-the-immediate-context)
-   [Raggruppamento di elementi di lavoro GPU](#grouping-of-gpu-work-items)
-   [Invio di lavoro GPU](#gpu-work-submission)
-   [Argomenti correlati](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Rimozione del contesto immediato

La modifica più importante da Microsoft Direct3D 11 a Microsoft Direct3D 12 è che a un dispositivo non è più associato un singolo contesto immediato. Per eseguire il rendering, invece, le app creano elenchi di comandi in cui è possibile chiamare le API di rendering tradizionali. Un elenco di comandi è simile al metodo di rendering di un'app Direct3D 11 che ha usato il contesto immediato in quanto contiene chiamate che disegnano primitive o modificano lo stato di rendering. Analogamente ai contesti immediati, ogni elenco di comandi non è a thread libero. Tuttavia, è possibile registrare più elenchi di comandi contemporaneamente, sfruttando i moderni processori multi-core.

Gli elenchi di comandi vengono in genere eseguiti una sola volta. Tuttavia, un elenco di comandi può essere eseguito più volte se l'applicazione garantisce che le esecuzioni precedenti siano state completate prima di inviare nuove esecuzioni. Per altre informazioni sulla sincronizzazione degli elenchi di comandi, vedere [Esecuzione e sincronizzazione di elenchi di comandi.](executing-and-synchronizing-command-lists.md)

## <a name="grouping-of-gpu-work-items"></a>Raggruppamento di elementi di lavoro GPU

Oltre agli elenchi di comandi, Direct3D 12 sfrutta le funzionalità presenti in tutto l'hardware aggiungendo un secondo livello di elenchi di comandi, denominati *bundle*. Per distinguere questi due tipi, gli elenchi di comandi di primo livello possono essere definiti *elenchi di comandi diretti.* Lo scopo dei bundle è consentire alle app di raggruppare un numero ridotto di comandi API per l'esecuzione ripetuta successiva dall'interno di elenchi di comandi diretti. Al momento della creazione di un bundle, il driver eseguirà la pre-elaborazione il più possibile per rendere efficiente l'esecuzione successiva. I bundle possono quindi essere eseguiti da più elenchi di comandi e più volte all'interno dello stesso elenco di comandi.

Il nuovo uso delle aggregazioni è un grande driver di miglioramento dell'efficienza con singoli thread della CPU. Poiché i bundle sono pre-elaborati e possono essere inviati più volte, esistono alcune restrizioni sulle operazioni che possono essere eseguite all'interno di un bundle. Per altre informazioni, vedere [Creazione e registrazione di elenchi di comandi e aggregazioni.](recording-command-lists-and-bundles.md)

## <a name="gpu-work-submission"></a>Invio di lavoro GPU

Per eseguire operazioni sulla GPU, un'app deve inviare in modo esplicito un elenco di comandi a una coda di comandi associata al dispositivo Direct3D. È possibile inviare più volte un elenco di comandi diretti per l'esecuzione, ma l'app è responsabile di assicurarsi che l'elenco di comandi diretti abbia terminato l'esecuzione nella GPU prima di inviarlo di nuovo. I bundle non hanno restrizioni per l'uso simultaneo e possono essere eseguiti più volte in più elenchi di comandi, ma non possono essere inviati direttamente a una coda di comandi per l'esecuzione.

Qualsiasi thread può inviare un elenco di comandi a qualsiasi coda di comandi in qualsiasi momento e il runtime serializza automaticamente l'invio dell'elenco di comandi nella coda dei comandi mantenendo l'ordine di invio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




