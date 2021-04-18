---
description: Un oggetto pool di archiviazione modella un pool di archiviazione in un sottosistema di archiviazione.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Oggetto pool di archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318592"
---
# <a name="storage-pool-object"></a>Oggetto pool di archiviazione

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto pool di archiviazione modella un pool di archiviazione in un sottosistema di archiviazione.

Un pool di archiviazione contiene extent di unità da una o più unità gestite dallo stesso provider hardware.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| Enumerazioni associate                           | [**VDS \_ \_Tipo di RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ \_ \_ stato del pool di archiviazione VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)e [**\_ \_ \_ tipo di pool di archiviazione VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).                                                                                                                                  |
| Strutture associate                             | [**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ attributi del pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ attributi personalizzati del pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ extent dell'unità del pool di archiviazione VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)e la [**\_ \_ \_ prop del pool di archiviazione VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop). |



 

 

 
