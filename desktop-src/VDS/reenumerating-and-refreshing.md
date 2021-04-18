---
description: Rienumerazione e aggiornamento
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Rienumerazione e aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313247"
---
# <a name="reenumerating-and-refreshing"></a>Rienumerazione e aggiornamento

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

L'operazione di rienumerazione individua dispositivi appena connessi e appena disconnessi. L'operazione di aggiornamento aggiorna le informazioni di configurazione dei dispositivi esistenti.

**Per rienumerare gli oggetti provider software**

-   Chiamare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) . Questo metodo individua tutti i dischi e le unità CD-ROM appena connesse e disconnesse e garantisce che tutti i dischi dispongano del proprietario appropriato. VDS possiede dischi RAW o dischi con errori; il provider Basic possiede i dischi di base; e il provider dinamico possiede dischi dinamici. Questa operazione può implicare l'analisi dei bus di sottosistema interni e l'attesa di timeout.

**Per rienumerare e aggiornare gli oggetti provider software**

-   Chiamare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) , quindi chiamare il metodo [**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) . Oltre a individuare i dischi appena connessi e disconnessi e le unità CD-ROM, questa combinazione di metodi Aggiorna tutte le informazioni su disco, volume e Plex nella cache VDS per i dischi che non sono stati connessi o disconnessi di recente. Chiamare solo **Refresh** per aggiornare le informazioni sulle proprietà degli oggetti esistenti nella cache. Questa operazione può implicare l'analisi dei bus di sottosistema interni e l'attesa di timeout. Si noti che VDS aggiorna automaticamente la cache ogni volta che viene apportata una modifica che attiva una notifica. Inoltre, la chiamata di **Refresh** in risposta a una notifica VDS potrebbe causare l'invio di un ciclo infinito di notifiche. Per questi motivi, è consigliabile chiamare **Refresh** solo quando sembra che la cache non venga aggiornata correttamente.

**Per rienumerare i sottosistemi hardware**

-   Chiamare il metodo [**IVdsHwProvider:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) . A seconda del provider, questa operazione può implicare l'invio di pacchetti di rete e l'attesa di timeout, la ripetizione dell'analisi dei bus SCSI e l'attesa di timeout e così via.

**Per rienumerare gli oggetti del sottosistema hardware**

-   Chiamare il metodo [**IVdsSubSystem:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) per eseguire l'inventario degli oggetti (in genere unità) nel sottosistema. A seconda del sottosistema, questa operazione può comportare l'analisi di bus di sottosistema interni e l'attesa di timeout.

**Per aggiornare sottosistemi hardware e oggetti sottosistema**

-   Chiamare il metodo [**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) per aggiornare la cache VDS delle informazioni sui sottosistemi esistenti gestiti dai provider hardware VDS. Si noti che VDS aggiorna automaticamente la cache ogni volta che viene apportata una modifica che attiva una notifica. Inoltre, la chiamata di [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in risposta a una notifica VDS potrebbe causare l'invio di un ciclo infinito di notifiche. Per questi motivi, è consigliabile chiamare **Refresh** solo quando sembra che la cache non venga aggiornata correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VDS](using-vds.md)
</dt> <dt>

[**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
