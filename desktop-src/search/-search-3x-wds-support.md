---
description: Processo di notifica nella Windows ricerca
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Processo di notifica nella Windows ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf6d9b2c7e13dd2d0c48490c4de835563a4c91b46c2290bf747211fd998c5eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119396441"
---
# <a name="notifications-process-in-windows-search"></a>Processo di notifica nella Windows ricerca

Questo argomento è organizzato come segue:

-   [Panoramica del processo di notifica](#overview-of-the-notifications-process)
-   [Striscia](#crawls)
-   [Notifiche gestite dall'indicizzatore](#indexer-managed-notifications)
-   [Notifiche gestite dal provider](#provider-managed-notifications)
-   [Notifiche sui set di righe](#notifications-on-rowsets)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Panoramica del processo di notifica

Esistono tre approcci in base ai quali è possibile indicizzare i dati dell'archivio dati:

-   Striscia
-   Notifiche gestite dall'indicizzatore
-   Notifiche gestite dal provider

I vantaggi di ogni approccio sono descritti nelle sezioni seguenti.

## <a name="crawls"></a>Striscia

Le origini abilitate per le notifiche e fanno una ricerca per indicizzazione incrementale all'avvio e quindi si basano sulle notifiche o su un comando esplicito per eseguire nuovamente la ricerca per indicizzazione. Questa operazione viene eseguita automaticamente Windows Vista e versioni successive. Nei sistemi operativi precedenti a Windows Vista è necessario configurare un evento pianificato nel [Utilità di pianificazione che](../taskschd/task-scheduler-start-page.md) chiama il codice per avviare una ricerca per indicizzazione nelle pagine iniziale. Non è necessario implementare alcuna forma di notifica. Come processo in background, l'indicizzatore attraversa l'ambito della ricerca per indicizzazione, cercando le modifiche e aggiornando il catalogo. Questa opzione è consigliata per quasi tutte le situazioni.

## <a name="indexer-managed-notifications"></a>Indexer-Managed notifiche

Con le notifiche gestite dall'indicizzatore, si implementa una strategia di notifica che notifica all'indicizzatore quando i dati nell'archivio dati sono stati modificati e l'indicizzatore gestisce il rilevamento delle notifiche e l'indicizzazione dei dati. In questa situazione, il componente ( che verrà chiamato provider di notifiche) monitora l'archivio dati, raccoglie informazioni sulle modifiche apportate all'archivio e quindi invia periodicamente una notifica all'indicizzatore con un elenco di elementi che devono essere indicizzati. L'indicizzatore è responsabile del ripristino e della risoluzione delle notifiche in caso di errore. Questa opzione, che può essere vista come la strategia "inviala e dimentica", riduce la frequenza delle ricerche per indicizzazione.

## <a name="provider-managed-notifications"></a>Provider-Managed notifiche

Con le notifiche gestite dal provider, si implementa una strategia di notifica simile al secondo approccio, ad eccezione del fatto che il provider di notifiche deve tenere traccia delle notifiche ed è responsabile del ripristino e della risoluzione delle notifiche in caso di errore. In questo caso, il provider di notifiche monitora l'archivio dati, raccoglie e gestisce le informazioni sulle modifiche apportate all'archivio, invia periodicamente una notifica all'indicizzatore con un elenco di elementi che devono essere indicizzati, riceve gli aggiornamenti dello stato dall'indicizzatore e invia di nuovo le notifiche in caso di errore.

> [!Note]  
> Questa opzione **non** è consigliata a meno che non si prevede che le ricerche per indicizzazione incrementali dell'archivio dati impediranno in modo significativo le prestazioni e non sia necessario un controllo granulare o informazioni dettagliate sullo stato dell'indicizzazione.

 

## <a name="notifications-on-rowsets"></a>Notifiche sui set di righe

In Windows 7 e versioni successive, l'indicizzazione degli eventi consente ai provider di ricevere notifiche sui set di righe. I provider che usano l'indicizzazione degli eventi possono mantenere i set di righe in modo simile al comportamento delle posizioni file system righe. Le librerie e le ricerche sono gli esempi principali di percorsi non di file system in Windows 7. La gestione degli eventi dell'indicizzatore è per le visualizzazioni di libreria, in quanto le notifiche sono relative alle visualizzazioni delle cartelle file. [**L'interfaccia IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) deve essere implementata per ricevere le notifiche degli eventi. Il livello dati è il client principale dell'evento dell'indicizzatore e decide cosa fare con gli eventi nell'interfaccia utente della visualizzazione Elementi. Per altre informazioni, vedere [Indexing Prioritization and Rowset Events in Windows 7](indexing-prioritization-and-rowset-events.md).

Al contrario, in Windows Vista, le viste basate su query non hanno eventi associati, ad eccezione della cache della shell per le modifiche alle proprietà dei file. Quando si esegue una ricerca, i risultati restituiti sono statici. Di conseguenza, se al sistema viene aggiunto un altro documento che corrisponde al termine di ricerca, la visualizzazione non viene aggiornata per includere la nuova aggiunta. Questo comportamento è standard per i risultati statici basati sul Web. Tuttavia, i risultati statici sono meno accettabili quando si tenta di fornire una visualizzazione basata su query su una posizione di archiviazione. Gli utenti si aspettano che il contenuto dell'indicizzatore sia corrente. Per altre informazioni, vedere [Notifica dell'indice delle modifiche.](-search-3x-wds-notifyingofchanges.md) Per la documentazione di riferimento, vedere [Interfacce di notifica.](-search-notifications-interfaces-entry-page.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione, esecuzione di query e notifiche nella Windows ricerca](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Elementi inclusi nell'indice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di indicizzazione nella Windows ricerca](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di query nella Windows ricerca](querying-process--windows-search-.md)
</dt> <dt>

[Requisiti di formattazione url](url-formatting-requirements.md)
</dt> </dl>

 

 
