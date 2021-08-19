---
title: Informazioni su NDF
description: La Framework di diagnostica di rete (NDF) riduce il coinvolgimento degli amministratori di rete e degli utenti di computer gestendo i problemi di rete comuni non appena si verificano.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2ce4890645e83c27e9c1cf594d7fbf4d81ce3d662a2b470ce652c71e7d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798903"
---
# <a name="about-ndf"></a>Informazioni su NDF

La Framework di diagnostica di rete (NDF) riduce il coinvolgimento degli amministratori di rete e degli utenti di computer gestendo i problemi di rete comuni non appena si verificano. Usando le funzionalità di diagnostica e ripristino di NDF, utenti e amministratori non necessitano di strumenti aggiuntivi per gestire alcuni problemi relativamente comuni. NDF viene fornito come parte di Windows Vista, Windows Server 2008 e versioni successive. È disponibile ogni volta che un sistema viene avviato (ma non può essere eseguito in Cassaforte sistema).

## <a name="ndf-helper-classes"></a>Classi helper NDF

NDF include classi helper che diagnosticano i problemi di rete non appena si verificano. Ognuna di queste classi helper contiene la logica necessaria per risolvere i problemi relativi ad almeno un componente o un'applicazione.

Le singole classi helper NDF eseguono le attività principali della sessione di diagnostica. Ogni classe helper è un'unità di codice progettata per valutare un aspetto di integrità del rispettivo componente di rete. La classe helper comprende anche le possibili opzioni di ripristino disponibili per ripristinare l'integrità del componente, nonché il costo e il rischio di qualsiasi opzione di ripristino specifica.

Ogni classe helper si collega alla classe Framework di diagnostica di rete. Se un componente di rete di terze parti include una classe helper NDF, i problemi con tale componente possono essere risolti da altre applicazioni che usano la funzione NDF, senza che sia necessario avere una conoscenza specifica di tale componente.

Le classi helper sviluppate da Microsoft forniscono agli sviluppatori di software le principali funzionalità di diagnostica e ripristino. È anche disponibile un piccolo set di API che gli sviluppatori possono usare per diagnosticare i problemi di rete tramite NDF. Per altre informazioni, vedere [Funzioni NDF e](ndf-functions.md) Esempio [di diagnostica NDF.](ndf-diagnostics-example.md)

## <a name="extensible-helper-classes"></a>Classi helper estendibili

In alcuni casi, le funzionalità di diagnostica e ripristino più specifiche possono essere fornite dagli sviluppatori di applicazioni.

Alcune delle classi helper NDF di Microsoft sono progettate per essere estese per offrire funzionalità di diagnostica e ripristino aggiuntive. Ciò significa che gli sviluppatori possono includere funzionalità per l'uso di funzionalità di diagnostica e ripristino NDF per risolvere i problemi specifici del software o dell'hardware.

Ad esempio, il team wireless di Microsoft fornisce una classe helper estendibile che consente a fornitori wireless di terze parti di aggiungere logica di risoluzione dei problemi specifica per l'hardware e/o il software specifico. A tale scopo, sviluppano un'estensione della classe helper NDF. Per altre informazioni, vedere [802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

Un'estensione della classe helper NDF, per definizione, estende la funzionalità di una classe helper estendibile esistente. Se una classe helper non è estendibile, nessuno può scrivere un'estensione per tale classe helper.

## <a name="benefits-of-helper-class-extensions"></a>Vantaggi delle estensioni delle classi helper

La funzione definita dall'utente offre diversi vantaggi distinti per incoraggiarne l'uso da parte degli sviluppatori di componenti di rete. All'inizio dell'elenco si trova il fatto che i clienti del software del fornitore liberano alcune delle proprie risorse di risoluzione dei problemi e riducono il costo totale di proprietà. Un'estensione di classe helper ben scritta offre anche i vantaggi seguenti:

-   Consente a un team di determinare quando il componente non è la causa di un problema di connettività. Ad esempio, la rete viene spesso incolpata per problemi di connettività che non sono effettivamente il risultato di un errore del componente di rete. Scrivendo un'estensione della classe helper, un team può escludere più facilmente un determinato componente come causa di un errore di connettività.
-   Consente a un team di diagnosticare ed eseguire rapidamente il debug di un problema all'interno del componente. Il tempo impiegato per il debug e la risoluzione dei problemi può essere eliminato se viene scritta una classe helper per eseguire tutti i passaggi di diagnostica standard che sarebbero comunque necessari.
-   Elimina la necessità di scrivere e supportare strumenti one-off per diagnosticare i problemi. Una classe helper può essere il repository centrale per le funzionalità di diagnostica e le tecniche di raccolta di informazioni di un componente.
-   Rende disponibile la diagnostica specifica del componente per le applicazioni, senza che sia necessario che abbia una conoscenza diretta del componente.

 

 




