---
description: Stack di configurazione
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Stack di configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566510"
---
# <a name="configuration-stacking"></a>Stack di configurazione

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Lo stacking prevede la concatenazione di un set di mapping dei blocchi logici. È possibile impilare più lun dallo stesso sottosistema in un LUN. È possibile impilare un LUN insieme ai volumi dello stesso pacchetto in un volume. Inoltre, è possibile sovrapporre più LUN esposti da sottosistemi eterogenei in un volume.

Come illustrato nella figura seguente, la creazione di un volume non comporta la modifica dell'associazione esistente di un LUN che contribuisce. Analogamente, l'annullamento dell'associazione di un volume non associa un LUN di contributo. Nella figura è illustrata la configurazione RAID 0 1 (0 + 1). Questa configurazione ben nota combina lo striping (RAID 0) e il mirroring (RAID 1), che abbina l'accesso rapido ai dati di RAID 0 con l'affidabilità di RAID 1.

![Diagramma che mostra una configurazione RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

I LUN che contribuiscono possono avere tipi di binding diversi. Molte configurazioni sono possibili con VDS, ma sono molto improbabili, come la figura successiva. In questo esempio un volume Plex è un LUN con striping e l'altro è un LUN con mirroring a tre vie.

![Diagramma che mostra una configurazione VDS in cui un plex del volume è un LUN con striping e l'altro è un LUN con mirroring a tre vie.](images/vdsstacklunvol.png)

Sebbene non pratico, in questo esempio viene illustrato un aspetto importante dello stacking. Poiché lo stacking concatena i plex, VDS aggiunge i tre Plex di LUN ai due plex del volume per un totale di cinque Plex.

 

 
