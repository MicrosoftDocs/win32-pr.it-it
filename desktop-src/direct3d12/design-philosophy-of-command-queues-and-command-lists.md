---
title: Filosofia di progettazione delle code dei comandi e degli elenchi di comandi
description: Gli obiettivi dell'abilitazione del riutilizzo del rendering del lavoro e del ridimensionamento multithreading richiedono modifiche fondamentali al modo in cui le app Direct3D inviano il lavoro di rendering alla GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- Elenco comandi
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103993"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Filosofia di progettazione delle code dei comandi e degli elenchi di comandi

Gli obiettivi dell'abilitazione del riutilizzo del rendering del lavoro e del ridimensionamento multithreading richiedono modifiche fondamentali al modo in cui le app Direct3D inviano il lavoro di rendering alla GPU. In Direct3D 12, il processo di invio del lavoro di rendering è diverso rispetto alle versioni precedenti in tre modi importanti:

<dl> 1. Eliminazione del contesto immediato. Questo consente il multithreading.  
2. Le app ora possiedono il modo in cui le chiamate di rendering vengono raggruppate in elementi di lavoro GPU (Graphics Processing Unit). Questo consente di riutilizzare.  
3. Le app ora controllano in modo esplicito quando il lavoro viene inviato alla GPU. In questo modo vengono abilitati gli elementi 1 e 2.  
</dl>

-   [Rimozione del contesto immediato](#removal-of-the-immediate-context)
-   [Raggruppamento di elementi di lavoro GPU](#grouping-of-gpu-work-items)
-   [Invio di lavoro GPU](#gpu-work-submission)
-   [Argomenti correlati](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Rimozione del contesto immediato

Il passaggio più grande da Microsoft Direct3D 11 a Microsoft Direct3D 12 è che non è più disponibile un unico contesto immediato associato a un dispositivo. Al contrario, per eseguire il rendering, le app creano elenchi di comandi in cui è possibile chiamare le API di rendering tradizionali. Un elenco di comandi è simile al metodo di rendering di un'app Direct3D 11 che ha usato il contesto immediato in quanto contiene chiamate che prevedono la generazione di primitive o la modifica dello stato di rendering. Analogamente ai contesti immediati, ogni elenco di comandi non è a thread libero. Tuttavia, è possibile registrare contemporaneamente più elenchi di comandi, che sfruttano i vantaggi dei processori multicore moderni.

Gli elenchi di comandi vengono in genere eseguiti una volta. Tuttavia, un elenco di comandi può essere eseguito più volte se l'applicazione garantisce il completamento delle esecuzioni precedenti prima di inviare nuove esecuzioni. Per ulteriori informazioni sulla sincronizzazione degli elenchi di comandi, vedere [esecuzione e sincronizzazione degli elenchi di comandi](executing-and-synchronizing-command-lists.md).

## <a name="grouping-of-gpu-work-items"></a>Raggruppamento di elementi di lavoro GPU

Oltre agli elenchi di comandi, Direct3D 12 sfrutta attualmente le funzionalità presenti in tutti i componenti hardware aggiungendo un secondo livello di elenchi di comandi, detti *bundle*. Per facilitare la distinzione di questi due tipi, gli elenchi di comandi di primo livello possono essere definiti *elenchi di comandi diretti*. Lo scopo dei bundle è quello di consentire alle app di raggruppare un numero ridotto di comandi API insieme per una successiva esecuzione ripetuta dall'interno di elenchi di comandi diretti. Al momento della creazione di un bundle, il driver eseguirà il maggior quantità possibile di pre-elaborazione per rendere efficiente l'esecuzione successiva. I bundle possono quindi essere eseguiti da più elenchi di comandi e più volte nello stesso elenco di comandi.

Il riutilizzo dei bundle è un grande driver di efficienza migliorata con singoli thread della CPU. Poiché i bundle sono pre-elaborati e possono essere inviati più volte, esistono alcune restrizioni sulle operazioni che possono essere eseguite all'interno di un bundle. Per altre informazioni, vedere [creazione e registrazione di elenchi di comandi e bundle](recording-command-lists-and-bundles.md).

## <a name="gpu-work-submission"></a>Invio di lavoro GPU

Per eseguire il lavoro sulla GPU, un'app deve inviare esplicitamente un elenco di comandi a una coda di comandi associata al dispositivo Direct3D. Un elenco di comandi diretto può essere inviato più volte per l'esecuzione, ma l'app è responsabile di garantire che l'esecuzione dell'elenco dei comandi diretto sia terminata sulla GPU prima di inviarla nuovamente. I bundle non hanno restrizioni per l'uso simultaneo e possono essere eseguiti più volte in più elenchi di comandi, ma non è possibile inviare i bundle direttamente a una coda di comandi per l'esecuzione.

Qualsiasi thread può inviare un elenco di comandi a qualsiasi coda dei comandi in qualsiasi momento e il runtime eseguirà automaticamente la serializzazione dell'elenco dei comandi nella coda dei comandi, conservando l'ordine di invio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




