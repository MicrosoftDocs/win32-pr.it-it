---
description: Enumerazione e aggiornamento
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Enumerazione e aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f19d28d44234b773988f3038666212caf447fb45dee39435b0d99169f92212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125921"
---
# <a name="reenumerating-and-refreshing"></a>Enumerazione e aggiornamento

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

L'operazione di enumerazione individua i dispositivi appena connessi e disconnessi. L'operazione di aggiornamento aggiorna le informazioni di configurazione dei dispositivi esistenti.

**Per enumerare nuovamente gli oggetti del provider software**

-   Chiamare il [**metodo IVdsService::Reenumerate.**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) Questo metodo individua tutti i dischi appena connessi e disconnessi e le unità CD-ROM e garantisce che tutti i dischi abbia il proprietario appropriato. VDS è proprietario di dischi non elaborati o dischi con errori; il provider di base è proprietario dei dischi di base; e il provider dinamico è proprietario di dischi dinamici. Questa operazione può comportare l'analisi dei bus interni del sottosistema e l'attesa di timeout.

**Per enumerare e aggiornare gli oggetti del provider software**

-   Chiamare il [**metodo IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) e quindi il [**metodo IVdsService::Refresh.**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) Oltre a individuare i dischi appena connessi e disconnessi e le unità CD-ROM, questa combinazione di metodi aggiorna tutte le informazioni su disco, volume e plex nella cache VDS per i dischi che non sono stati connessi o disconnessi di recente. Chiamare **Refresh** da solo per aggiornare le informazioni sulle proprietà degli oggetti esistenti nella cache. Questa operazione può comportare l'analisi dei bus interni del sottosistema e l'attesa di timeout. Si noti che VDS aggiorna automaticamente la cache ogni volta che si verifica una modifica che attiva una notifica. Inoltre, la **chiamata di Refresh** in risposta a una notifica VDS potrebbe causare l'invio di un ciclo infinito di notifiche. Per questi motivi, **l'aggiornamento** deve essere chiamato solo quando risulta che la cache non viene aggiornata correttamente.

**Per enumerare nuovamente i sottosistemi hardware**

-   Chiamare il [**metodo IVdsHwProvider::Reenumerate.**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) A seconda del provider, questa operazione può comportare l'invio di pacchetti di rete e l'attesa di timeout, la nuova analisi dei bus SCSI e l'attesa dei timeout e così via.

**Per enumerare nuovamente gli oggetti del sottosistema hardware**

-   Chiamare il [**metodo IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) per eseguire l'inventario degli oggetti (in genere unità) nel sottosistema. A seconda del sottosistema, questa operazione può comportare l'analisi dei bus interni del sottosistema e l'attesa di timeout.

**Per aggiornare i sottosistemi hardware e gli oggetti del sottosistema**

-   Chiamare il [**metodo IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) per aggiornare la cache VDS delle informazioni sui sottosistemi esistenti gestiti dai provider di hardware VDS. Si noti che VDS aggiorna automaticamente la cache ogni volta che si verifica una modifica che attiva una notifica. Inoltre, la [**chiamata di Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in risposta a una notifica VDS potrebbe causare l'invio di un ciclo infinito di notifiche. Per questi motivi, **l'aggiornamento** deve essere chiamato solo quando risulta che la cache non viene aggiornata correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
