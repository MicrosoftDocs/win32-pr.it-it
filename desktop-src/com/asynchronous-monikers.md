---
title: Moniker asincroni
description: Moniker asincroni
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9e9b5e427df882b7e0be84507b79c9113a46e44dad614e571a831fedecedff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859651"
---
# <a name="asynchronous-monikers"></a>Moniker asincroni

L'architettura del moniker OLE fornisce un modello di programmazione coerente ed estendibile per l'utilizzo di oggetti Internet, fornendo metodi per l'analisi dei nomi, la rappresentazione di URL (Universal Resource Locators) come nomi stampabili e l'individuazione e l'associazione agli oggetti rappresentati da stringhe URL. Vedere anche [URL Moniker.](url-monikers.md) I moniker OLE standard(in particolare, moniker di elementi, file e puntatori), tuttavia, non sono appropriati per Internet perché sono sincroni e restituiscono un puntatore a un oggetto o alla relativa archiviazione solo quando tutti i dati sono disponibili. A seconda della quantità di dati da scaricare, l'associazione in modo sincrono può collegare l'interfaccia utente del client per periodi prolungati.

Internet richiede nuovi approcci alla progettazione delle applicazioni. Le applicazioni devono essere in grado di eseguire tutte le operazioni di rete costose in modo asincrono per evitare di bloccare l'interfaccia utente. Un'applicazione deve essere in grado di attivare un'operazione e ricevere una notifica al completamento completo o parziale. A questo punto, l'applicazione deve scegliere se procedere con il passaggio successivo dell'operazione o fornire informazioni aggiuntive in base alle esigenze. Durante il download, un'applicazione deve anche essere in grado di fornire agli utenti informazioni sullo stato di avanzamento e la possibilità di annullare l'operazione in qualsiasi momento.

I moniker asincroni forniscono queste funzionalità, nonché vari livelli di comportamento di associazione asincrona, garantendo al tempo stesso la compatibilità con le versioni precedenti per le applicazioni che non sono a conoscenza o non richiedono un comportamento asincrono. Un'altra tecnologia OLE, l'archiviazione asincrona, funziona con moniker asincroni per fornire il download asincrono dello stato persistente di un oggetto Internet. Il moniker asincrono attiva l'operazione di associazione e configura i componenti necessari, inclusi gli oggetti di archiviazione e flusso, gli oggetti matrice di byte e i sink di notifica. Una volta connessi i componenti, il moniker viene smisato e il resto dell'associazione viene eseguito principalmente tra i componenti che implementano i componenti di archiviazione asincroni e l'oggetto .

Per altre informazioni, vedere i seguenti argomenti:

-   [Moniker asincroni e sincroni](./asynchronous-vs.-synchronous-monikers.md)
-   [Associazione asincrona e sincrona](./asynchronous-vs.-synchronous-binding.md)
-   [Operazioni asincrone e sincrone Archiviazione](./asynchronous-vs.-synchronous-storage.md)
-   [Modello di pull dei dati e Data-Push dati](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker URL](url-monikers.md)
</dt> </dl>

 

 