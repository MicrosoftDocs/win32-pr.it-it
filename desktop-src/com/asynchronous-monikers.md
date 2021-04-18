---
title: Moniker asincroni
description: Moniker asincroni
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19323af3a972a2b83a290176a4b26fb79382da0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300524"
---
# <a name="asynchronous-monikers"></a>Moniker asincroni

L'architettura del moniker OLE fornisce un modello di programmazione coerente ed estendibile per l'utilizzo di oggetti Internet, fornendo metodi per l'analisi dei nomi, che rappresentano i localizzatori di risorse universali (URL) come nomi stampabili e l'individuazione e l'associazione agli oggetti rappresentati da stringhe URL. Vedere anche [moniker URL](url-monikers.md). I moniker OLE standard (in particolare, i moniker di elementi, file e puntatori), tuttavia, non sono appropriati per Internet perché sono sincroni, restituendo un puntatore a un oggetto o alla relativa archiviazione solo in un momento in cui tutti i dati sono disponibili. A seconda della quantità di dati da scaricare, l'associazione in modo sincrono può bloccare l'interfaccia utente del client per periodi prolungati.

Internet richiede nuovi approcci alla progettazione dell'applicazione. Le applicazioni devono essere in grado di eseguire tutte le operazioni di rete dispendiose in modo asincrono per evitare di bloccare l'interfaccia utente. Un'applicazione deve essere in grado di attivare un'operazione e ricevere una notifica al completamento completo o parziale. A questo punto, l'applicazione deve avere la possibilità di procedere con il passaggio successivo dell'operazione o fornire informazioni aggiuntive, se necessario. Durante il download, un'applicazione deve anche essere in grado di fornire agli utenti informazioni sullo stato di avanzamento e l'opportunità di annullare l'operazione in qualsiasi momento.

I moniker asincroni forniscono queste funzionalità, oltre a diversi livelli di comportamento di binding asincrono, garantendo al tempo stesso la compatibilità con le versioni precedenti per le applicazioni che non sono a conoscenza di o che non richiedono un comportamento asincrono. Un'altra tecnologia OLE, archiviazione asincrona, funziona con moniker asincroni per fornire il download asincrono dello stato persistente di un oggetto Internet. Il moniker asincrono attiva l'operazione di associazione e imposta i componenti necessari, inclusi oggetti di archiviazione e di flusso, oggetti della matrice di byte e sink di notifica. Una volta connessi i componenti, il moniker viene eliminato e il resto del binding viene eseguito principalmente tra i componenti che implementano i componenti di archiviazione asincrona e l'oggetto.

Per altre informazioni, vedere i seguenti argomenti:

-   [Moniker asincroni e sincroni](./asynchronous-vs.-synchronous-monikers.md)
-   [Associazione asincrona e sincrona](./asynchronous-vs.-synchronous-binding.md)
-   [Archiviazione asincrona e sincrona](./asynchronous-vs.-synchronous-storage.md)
-   [Modello di pull dei dati e modello di Data-Push](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker URL](url-monikers.md)
</dt> </dl>

 

 