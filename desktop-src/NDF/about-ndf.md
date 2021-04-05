---
title: Informazioni su NDF
description: Il Framework di diagnostica di rete (NDF) riduce il coinvolgimento degli amministratori di rete e degli utenti dei computer gestendo problemi di rete comuni quando si verificano.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b638298fe321d314815c74fced49d3dfb623022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709790"
---
# <a name="about-ndf"></a>Informazioni su NDF

Il Framework di diagnostica di rete (NDF) riduce il coinvolgimento degli amministratori di rete e degli utenti dei computer gestendo problemi di rete comuni quando si verificano. Utilizzando le funzionalità di diagnostica e ripristino di NDF, gli utenti e gli amministratori non necessitano di strumenti aggiuntivi per gestire alcuni problemi relativamente comuni. NDF viene fornito come parte di Windows Vista, Windows Server 2008 e versioni successive. È disponibile ogni volta che un sistema viene avviato, ma non può essere eseguito in modalità provvisoria.

## <a name="ndf-helper-classes"></a>Classi helper NDF

NDF include classi helper che consentono di diagnosticare i problemi di rete non appena si verificano. Ognuna di queste classi helper contiene la logica necessaria per risolvere almeno un componente o un'applicazione.

Le singole classi helper NDF eseguono le attività primarie della sessione di diagnostica. Ogni classe helper è un'unità di codice progettata per valutare un aspetto di integrità del rispettivo componente di rete. La classe helper comprende inoltre le possibili opzioni di ripristino disponibili per ripristinare l'integrità del componente, nonché i costi e i rischi di una particolare opzione di ripristino.

Ogni classe helper si connette a Global Network Diagnostics Framework. Se un componente di rete di terze parti include una classe helper NDF, i problemi relativi a tale componente possono essere risolti da altre applicazioni che utilizzano NDF, senza che sia necessario disporre di una conoscenza specifica di tale componente.

Le classi helper sviluppate da Microsoft forniscono agli sviluppatori software la funzionalità di diagnostica e ripristino primaria. Esiste anche un piccolo set di API che gli sviluppatori possono usare per diagnosticare i problemi di rete con NDF. Per ulteriori informazioni, vedere l'esempio relativo alle [funzioni NDF](ndf-functions.md) e alla [diagnostica NDF](ndf-diagnostics-example.md).

## <a name="extensible-helper-classes"></a>Classi helper estendibili

In alcuni casi, gli sviluppatori di applicazioni possono fornire funzionalità di diagnostica e ripristino più specifiche.

Alcune delle classi helper di Microsoft NDF sono progettate per essere estese per fornire funzionalità di diagnostica e ripristino aggiuntive. Questo significa che gli sviluppatori possono includere funzionalità per usare le funzionalità di diagnostica e ripristino di NDF per risolvere i problemi specifici del software o dell'hardware.

Ad esempio, il team wireless di Microsoft fornisce una classe helper estendibile che consente a qualsiasi fornitore wireless di terze parti di aggiungere una logica di risoluzione dei problemi specifica per l'hardware e/o il software specifico. Questa operazione può essere eseguita sviluppando un'estensione della classe helper NDF. Per ulteriori informazioni, vedere la pagina relativa alle [classi di helper estendibili di diagnostica Wireless 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md).

Un'estensione della classe helper NDF, per definizione, estende la funzionalità di una classe helper estendibile esistente. Se una classe helper non è estendibile, nessuno può scrivere un'estensione per tale classe helper.

## <a name="benefits-of-helper-class-extensions"></a>Vantaggi delle estensioni delle classi helper

NDF offre diversi vantaggi distinti per incentivarne l'utilizzo da parte degli sviluppatori di componenti di rete. Nella parte superiore dell'elenco i clienti del software del fornitore potranno liberare alcune risorse di risoluzione dei problemi e ridurranno il costo totale di proprietà. Un'estensione di classe helper ben scritta offre inoltre i vantaggi seguenti:

-   Consente a un team di determinare quando il componente non è la causa di un problema di connettività. Ad esempio, la rete viene spesso accusata di problemi di connettività che non sono in realtà il risultato di un errore di un componente di rete. Scrivendo un'estensione di classe helper, un team può più facilmente escludere un determinato componente come la provocazione di un errore di connettività.
-   Consente a un team di diagnosticare rapidamente ed eseguire il debug di un problema all'interno del componente. Il tempo impiegato per il debug e la risoluzione dei problemi può essere eliminato se viene scritta una classe helper per eseguire tutti i passaggi di diagnostica standard che dovrebbero comunque essere necessari.
-   Elimina la necessità di scrivere e supportare gli strumenti monouso per diagnosticare i problemi. Una classe helper può essere il repository centrale per le funzionalità di diagnostica di un componente e le tecniche di raccolta delle informazioni.
-   Rende disponibili le applicazioni di diagnostica specifiche per i componenti, senza richiedere alcuna conoscenza diretta sul componente.

 

 




