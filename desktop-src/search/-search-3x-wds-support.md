---
description: .
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Processo di notifica in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7dd37979eab7ef32a5a8917ba6a3589e976105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128586"
---
# <a name="notifications-process-in-windows-search"></a>Processo di notifica in Windows Search

Questo argomento è organizzato nel modo seguente:

-   [Panoramica del processo di notifica](#overview-of-the-notifications-process)
-   [Ricerche per indicizzazione](#crawls)
-   [Notifiche gestite dall'indicizzatore](#indexer-managed-notifications)
-   [Notifiche gestite dal provider](#provider-managed-notifications)
-   [Notifiche per i set di righe](#notifications-on-rowsets)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Panoramica del processo di notifica

Esistono tre approcci che consentono di indicizzare i dati dell'archivio dati:

-   Ricerche per indicizzazione
-   Notifiche gestite dall'indicizzatore
-   Notifiche gestite dal provider

I vantaggi di ogni approccio sono descritti nelle sezioni seguenti.

## <a name="crawls"></a>Ricerche per indicizzazione

Le origini abilitate per le notifiche eseguono una ricerca per indicizzazione incrementale all'avvio e quindi utilizzano notifiche o un comando esplicito per eseguire la ricerca per indicizzazione. Questa operazione viene eseguita automaticamente in Windows Vista e versioni successive. Nei sistemi operativi precedenti a Windows Vista, è necessario configurare un evento pianificato nell' [utilità di pianificazione](../taskschd/task-scheduler-start-page.md) che chiama il codice per avviare una ricerca per indicizzazione sulle pagine iniziali. Non è necessario implementare alcuna forma di notifiche. Come processo in background, l'indicizzatore attraversa l'ambito di ricerca per indicizzazione, cercando le modifiche e aggiornando il catalogo. Questa opzione è consigliata per quasi tutte le situazioni.

## <a name="indexer-managed-notifications"></a>Notifiche Indexer-Managed

Con le notifiche gestite dall'indicizzatore, viene implementata una strategia di notifica che informa l'indicizzatore quando i dati nell'archivio dati sono stati modificati e l'indicizzatore gestisce il rilevamento delle notifiche e l'indicizzazione dei dati. In questa situazione, il componente (che chiameremo un provider di notifiche) monitora l'archivio dati, raccoglie informazioni sulle modifiche apportate all'archivio e quindi invia periodicamente una notifica all'indicizzatore con un elenco di elementi che richiedono l'indicizzazione. L'indicizzatore è responsabile del ripristino e della risoluzione delle notifiche in caso di errore. Questa opzione, che è possibile considerare come la strategia "Send it and forget it", riduce la frequenza delle ricerche nell'indicizzatore.

## <a name="provider-managed-notifications"></a>Notifiche Provider-Managed

Con le notifiche gestite dal provider, viene implementata una strategia di notifica simile al secondo approccio, ad eccezione del fatto che il provider di notifiche deve tenere traccia delle notifiche ed è responsabile del ripristino e della risoluzione delle notifiche in caso di errore. In questa situazione, il provider di notifiche monitora l'archivio dati, raccoglie e gestisce le informazioni sulle modifiche apportate all'archivio, informa periodicamente l'indicizzatore con un elenco di elementi che richiedono l'indicizzazione, riceve gli aggiornamenti di stato dall'indicizzatore e invia nuovamente le notifiche in caso di errore.

> [!Note]  
> Questa opzione **non è consigliata** , a meno che non si prevedano ricerche per indicizzazione incrementali dell'archivio dati per ostacolare significativamente le prestazioni ed è necessario un controllo granulare o informazioni dettagliate sullo stato di indicizzazione.

 

## <a name="notifications-on-rowsets"></a>Notifiche per i set di righe

In Windows 7 e versioni successive, l'indicizzazione di eventi consente ai provider di ricevere notifiche relative ai set di righe. I provider che utilizzano gli eventi di indicizzazione possono mantenere i set di righe in modo analogo al comportamento dei percorsi di file system effettivi. Le librerie e le ricerche sono gli esempi principali di percorsi non di file System in Windows 7. Gli eventi dell'indicizzatore sono viste libreria come notifiche per le visualizzazioni di file-cartelle. Per ricevere notifiche di eventi, è necessario implementare l'interfaccia [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) . Il livello dati è il client primario degli eventi dell'indicizzatore e decide cosa fare con gli eventi nell'interfaccia utente della visualizzazione elementi. Per ulteriori informazioni, vedere [indicizzazione di priorità e eventi del set di righe in Windows 7](indexing-prioritization-and-rowset-events.md).

Al contrario, in Windows Vista, le visualizzazioni basate su query non hanno eventi associati, ad eccezione della cache della Shell per le modifiche alle proprietà dei file. Quando si esegue una ricerca, i risultati restituiti sono statici. Di conseguenza, se un altro documento viene aggiunto al sistema che corrisponde al termine di ricerca, la visualizzazione non viene aggiornata in modo da includere la nuova aggiunta. Questo comportamento è standard per i risultati statici basati sul Web. Tuttavia, i risultati statici sono meno accettabili quando si tenta di fornire una visualizzazione basata su query su un percorso di archiviazione. Gli utenti si aspettano che il contenuto dell'indicizzatore sia aggiornato. Per ulteriori informazioni, vedere [notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md). Per la documentazione di riferimento, vedere [interfacce di notifica](-search-notifications-interfaces-entry-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione, query e notifiche in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Contenuto dell'indice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di indicizzazione in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Esecuzione di query sul processo in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Requisiti per la formattazione degli URL](url-formatting-requirements.md)
</dt> </dl>

 

 
