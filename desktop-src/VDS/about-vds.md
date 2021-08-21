---
description: Informazioni su VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Informazioni su VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1215251bf86c3ac4ba9a7a342a483de19653d20a21978715261b87aa7bea31a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603716"
---
# <a name="about-vds"></a>Informazioni su VDS

\[A partire da Windows 8 e Windows Server 2012, [l'interfaccia](virtual-disk-service-portal.md) COM del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Servizio dischi virtuali è un servizio microsoft Windows che esegue operazioni di query e configurazione su richiesta di utenti finali, script e applicazioni. Il servizio estende le funzionalità di archiviazione esistenti dei Windows server nei modi seguenti:

-   Fornisce un'API alle funzionalità di gestione dei volumi e dei dischi esistenti in Windows.
-   Unifica la gestione dei volumi e la gestione RAID (Redundant Array of Independent Disks) hardware con una singola API.

VDS non esegue le attività di gestione dell'archiviazione seguenti:

-   Gestione del sottosistema hardware, ad esempio il monitoraggio della temperatura o il monitoraggio delle statistiche sulle prestazioni per gli array di dischi.
-   Archiviazione Gestione dell'infrastruttura SAN (Area Network), ad esempio la suddivisione Host-Based Adapter (HBA) per la suddivisione in zone e la sicurezza.

Le sezioni seguenti descrivono l'architettura di VDS, il ruolo dei provider VDS e l'API.

## <a name="service-architecture"></a>Architettura del servizio

VDS definisce tre interfacce: una singola interfaccia tra il livello applicazione e il servizio e due interfacce tra il servizio e i programmi provider nel livello dati. La figura seguente mostra il limite da applicazione a servizio e il limite da servizio a provider.

![Diagramma che illustra l'architettura del servizio suddivisa nelle sezioni "Applicazioni", "Servizio dischi virtuali" e "Provider VDS".](images/vdsoverview.png)

L'architettura a più livelli consente a VDS di coordinarsi con le funzioni del file system, sincronizzare le attività del provider e arbitrate tra le applicazioni. Tra l'applicazione e il provider, VDS presenta funzionalità uniformi alle applicazioni anche se alcuni provider sottostanti potrebbero non avere tale uniformità.

Il servizio implementa funzionalità comuni: la formattazione dei volumi, l'aggiunta e la rimozione di lettere di unità o cartelle montate, nonché la gestione di dischi non allocati, ovvero dischi senza informazioni di partizione. VDS restituisce anche le notifiche degli eventi alle applicazioni registrate. Per informazioni dettagliate, vedere [Notifiche VDS](vds-notification-model.md).

## <a name="role-of-providers"></a>Ruolo dei provider

VDS definisce due interfacce provider, una per un provider software e una per un provider hardware. Ogni provider implementa una parte diversa dell'API definita da VDS:

-   Un *provider di software* è un programma basato su host supportato da un driver in modalità kernel nello stack di I/O di archiviazione. Il runtime del kernel del provider interagisce con Mount Manager in fase di avvio o con Plug and Play (PnP) Manager in fase di individuazione per richiedere ogni disco. I provider di software operano su volumi, dischi e partizioni del disco.

    VDS include due tipi di provider. Il provider software di base gestisce i dischi di base e non offre alcuna associazione a tolleranza di errore. Il provider di software dinamico gestisce i dischi dinamici e offre la gestione degli errori laddove applicabile. Il comportamento del provider di software è coerente con il comportamento dei dischi di base e dinamici nell'host. Ad esempio, se il sistema operativo di un determinato host supporta dischi dinamici a tolleranza di errore, VDS supporta anche questo comportamento nell'host.

-   Un *provider hardware* implementa i metodi usati per gestire un sottosistema di archiviazione, ovvero un array di dischi hardware o una scheda di scheda che consente la creazione di dischi logici configurati per migliorare le prestazioni, la disponibilità dei dati o il ripristino dei dati. Molti dei principali produttori di archivi RAID hanno prodotto un provider di hardware progettato per l'uso con VDS. Gli utenti del servizio devono ottenere un provider di hardware e l'hardware associato dal produttore.

    Le funzionalità di un provider di hardware dipendono dalle funzionalità dell'hardware sottostante. Di conseguenza, il grado di implementazione dell'API da parte di ogni produttore può variare. Ad esempio, i produttori possono includere metodi aggiuntivi per ottimizzare le configurazioni, monitorare e ottimizzare dinamicamente le prestazioni, automatizzare la gestione degli errori o fornire altre funzionalità vantaggiose.

    I provider di hardware offrono diverse opzioni di configurazione che non sono disponibili per i provider di software. La cosa più importante è il modello di configurazione automagic, che presenta una visualizzazione basata su attributi dell'archiviazione per ogni applicazione. Gli hint di associazione, ad esempio "principalmente operazioni di lettura" o "ripristino rapido dell'arresto anomalo del sistema richiesto", sostituiscono la complessità dell'associazione dell'archiviazione fisica all'archiviazione virtuale. Ogni provider hardware esegue il mapping di extent, l'allocazione dello spazio e la selezione del tipo di associazione in base ai suggerimenti inviati da un'applicazione. Per la descrizione completa del provider di hardware, incluse le opzioni di configurazione, vedere la documentazione fornita dal produttore del sottosistema.

## <a name="application-programming-interface"></a>Interfaccia di programmazione delle applicazioni

Le applicazioni possono richiamare metodi VDS per eseguire query e configurare dischi basati su host, archiviazione RAID o entrambi. Per una panoramica dell'API, vedere il [modello a oggetti VDS.](vds-object-model.md)

Le applicazioni tipiche per VDS risolvono i problemi di gestione e monitoraggio della configurazione e vanno dai sistemi di gestione dell'archiviazione dedicati alle applicazioni back-office che cercano un controllo migliore sulla configurazione o sulla gestione degli errori. Le applicazioni seguenti usano attualmente VDS:

-   Lo snap-in Gestione disco configura e gestisce i dischi controllati da un computer host. Gli amministratori di sistema e gli utenti finali possono eseguire query e configurare dischi e volumi locali (o remoti) con questo strumento dell'interfaccia utente.
-   Diskpart.exe è un'utilità della riga di comando che configura e gestisce dischi, volumi e partizioni.
-   Diskraid.exe è un'utilità della riga di comando che configura e gestisce i sottosistemi RAID hardware. Questa utilità può interagire con qualsiasi hardware di archiviazione associato a un provider di hardware VDS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio dischi virtuali](virtual-disk-service-portal.md)
</dt> <dt>

[Notifiche VDS](vds-notification-model.md)
</dt> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> </dl>

 

 
