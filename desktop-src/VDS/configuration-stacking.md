---
description: Stacking della configurazione
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Stacking della configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9018a2484ce4e5b9121d08abffee54911531b7f421cfef75643594e827fe350e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905563"
---
# <a name="configuration-stacking"></a>Stacking della configurazione

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

L'impilamento comporta la concatenazione di un set di mapping di blocchi logici. È possibile eseguire lo stack di più LUN dello stesso sottosistema in un unico LUN. È possibile impilare un LUN insieme ai volumi dello stesso pacchetto in un unico volume. Inoltre, è possibile impilare più LUN che vengono evinte da sottosistemi eterogenei in un unico volume.

Come illustrato nella figura seguente, la creazione di un volume non modifica l'associazione esistente di un LUN che contribuisce. Analogamente, l'annullamento dell'associazione di un volume non annulla l'associazione di un LUN che contribuisce. La figura illustra la configurazione RAID 0 1 (0+1). Questa configurazione nota combina lo striping (RAID 0) e il mirroring (RAID 1), che associa l'accesso rapido ai dati di RAID 0 con l'affidabilità di RAID 1.

![Diagramma che mostra una configurazione RAID 0 1 (0+1).](images/vdsstacklunvolzeroplusone.png)

I LUN che contribuiscono possono avere tipi di binding diversi. Molte configurazioni sono possibili con VDS, ma sono altamente improbabile, come nell'illustrazione successiva. In questo esempio, un volume plex è un LUN con striping e l'altro è un LUN con mirroring a tre modi.

![Diagramma che mostra una configurazione VDS in cui un volume plex è un LUN con striping e l'altro è un LUN con mirroring a 3 modi.](images/vdsstacklunvol.png)

Anche se poco pratico, questo esempio illustra un aspetto importante dell'impilamento. Poiché l'impilamento concatena i plex, VDS aggiunge i tre plex LUN ai due plex di volume per un totale di cinque plex.

 

 
