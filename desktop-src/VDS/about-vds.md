---
description: Informazioni su VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Informazioni su VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911145fda8f2dd63c886530af3d8507c38d8e829
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104563232"
---
# <a name="about-vds"></a>Informazioni su VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Il servizio dischi virtuali è un servizio di Microsoft Windows che esegue operazioni di query e configurazione su richiesta di utenti finali, script e applicazioni. Il servizio estende le funzionalità di archiviazione esistenti dei sistemi operativi Windows Server nei modi seguenti:

-   Fornisce un'API per le funzionalità di gestione di volumi e dischi esistenti in Windows.
-   Unifica la gestione dei volumi e la gestione RAID (Array of Independent Disks) hardware ridondante in un'unica API.

VDS non esegue le attività di gestione dell'archiviazione seguenti:

-   Gestione del sottosistema hardware, ad esempio il monitoraggio della temperatura o il monitoraggio delle statistiche sulle prestazioni per gli array di dischi.
-   Gestione dell'infrastruttura SAN (Storage Area Network), come la suddivisione in zone e la sicurezza di Host-Based Adapter (HBA).

Le sezioni seguenti descrivono l'architettura di VDS, il ruolo dei provider VDS e l'API.

## <a name="service-architecture"></a>Architettura del servizio

VDS definisce tre interfacce: una singola interfaccia tra il livello dell'applicazione e il servizio e due interfacce tra il servizio e i programmi del provider nel livello dati. Nella figura seguente vengono illustrati il limite da applicazione a servizio e il limite da servizio a provider.

![Diagramma che mostra l'architettura del servizio suddivisa nelle sezioni "applicazioni", "servizio dischi virtuali" e "provider VDS".](images/vdsoverview.png)

L'architettura a più livelli consente a VDS di coordinarsi con le funzioni del file System, sincronizzare le attività del provider e arbitrario tra le applicazioni. Tra l'applicazione e il provider, VDS presenta una funzionalità uniforme per le applicazioni anche se alcuni dei provider sottostanti potrebbero non avere tale uniformità.

Il servizio implementa funzionalità comuni: formattazione di volumi, aggiunta e rimozione di lettere di unità o cartelle montate, nonché gestione di dischi non allocati, ovvero i dischi privi di informazioni sulla partizione. VDS restituisce anche le notifiche degli eventi alle applicazioni registrate. Per informazioni dettagliate, vedere [notifiche VDS](vds-notification-model.md).

## <a name="role-of-providers"></a>Ruolo dei provider

VDS definisce due interfacce del provider, una per un provider software e una per un provider hardware. Ogni provider implementa una parte diversa dell'API definita da VDS:

-   Un *provider di software* è un programma basato su host supportato da un driver in modalità kernel nello stack i/O di archiviazione. Il runtime del kernel del provider interagisce con il gestore di montaggio in fase di avvio oppure con la gestione Plug and Play (PnP) al momento dell'individuazione per richiedere ogni disco. I provider di software operano su volumi, dischi e partizioni disco.

    VDS include due tipi di provider. Il provider software di base gestisce i dischi di base e non offre alcun binding a tolleranza di errore. Il provider di software dinamico gestisce i dischi dinamici e offre una gestione degli errori, se applicabile. Il comportamento del provider software è coerente con il comportamento dei dischi di base e dinamici nell'host. Se, ad esempio, il sistema operativo di un determinato host supporta dischi dinamici a tolleranza di errore, VDS supporta anche questo comportamento nell'host.

-   Un *provider hardware* implementa i metodi utilizzati per gestire un sottosistema di archiviazione, ovvero un array di dischi hardware o una scheda adattatore che consente la creazione di dischi logici configurati per migliorare le prestazioni, la disponibilità dei dati o il ripristino dei dati. Molti produttori di cabinet RAID principali hanno prodotto un provider hardware progettato per l'uso con VDS. I consumer del servizio devono ottenere un provider hardware e l'hardware associato dal produttore.

    Le funzionalità di un provider hardware dipendono dalle funzionalità dell'hardware sottostante. Di conseguenza, il grado di implementazione dell'API da parte di ogni produttore può variare. I produttori, ad esempio, possono includere metodi aggiuntivi per ottimizzare le configurazioni, monitorare e ottimizzare dinamicamente le prestazioni, automatizzare la gestione degli errori o fornire altre funzionalità utili.

    I provider hardware offrono diverse opzioni di configurazione che non sono disponibili per i provider di software. La più importante è il modello di configurazione di automagic, che presenta una visualizzazione basata su attributi dell'archiviazione per ogni applicazione. Gli hint per l'associazione, ad esempio "letture prevalentemente" o "ripristino arresto anomalo rapido", sostituiscono la complessità dell'associazione dell'archiviazione fisica all'archiviazione virtuale. Ogni provider hardware esegue il mapping degli extent, l'allocazione dello spazio e la selezione del tipo di binding in base agli hint inviati da un'applicazione. Per la descrizione completa del provider hardware, incluse le opzioni di configurazione, vedere la documentazione fornita dal produttore del sottosistema.

## <a name="application-programming-interface"></a>Interfaccia di programmazione delle applicazioni

Le applicazioni possono richiamare metodi VDS per eseguire query e configurare dischi basati su host, archiviazione RAID o entrambi. Per una panoramica dell'API, vedere il [modello a oggetti VDS](vds-object-model.md).

Le applicazioni tipiche per VDS risolvono i problemi di gestione della configurazione e di monitoraggio e variano da sistemi di gestione dell'archiviazione dedicati alle applicazioni back-Office, cercando un migliore controllo sulla configurazione o la gestione degli errori. Attualmente le applicazioni seguenti usano VDS:

-   Lo snap-in Gestione disco consente di configurare e gestire i dischi controllati da un computer host. Gli amministratori di sistema e gli utenti finali possono eseguire query e configurare volumi e dischi locali (o remoti) con questo strumento dell'interfaccia utente.
-   Diskpart.exe è un'utilità da riga di comando che consente di configurare e gestire dischi, volumi e partizioni.
-   Diskraid.exe è un'utilità da riga di comando che consente di configurare e gestire i sottosistemi RAID hardware. Questa utilità può interagire con qualsiasi hardware di archiviazione accompagnato da un provider hardware VDS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio dischi virtuali](virtual-disk-service-portal.md)
</dt> <dt>

[Notifiche VDS](vds-notification-model.md)
</dt> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> </dl>

 

 
