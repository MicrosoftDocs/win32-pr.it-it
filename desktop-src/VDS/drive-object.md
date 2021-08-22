---
description: Oggetto Unità
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Oggetto Unità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04ec68fab408c4ed6412990296c0ebb265b8c3e4c4c9b05645b1f4bd1e625fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603421"
---
# <a name="drive-object"></a>Oggetto Unità

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto unità modella un'unità disco fisico contenuta in un sottosistema. Ogni unità si connette a un bus, occupa uno slot e contiene un set di extent di unità. Ogni unità può contribuire a un numero qualsiasi di LUN. Un'unità può anche essere designata come riserva a caldo.

Usare il [**metodo IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) per determinare le unità contenute in un sottosistema specifico. I chiamanti possono ottenere un puntatore a un'unità specifica selezionando l'oggetto unità desiderato dall'enumerazione restituita dal metodo **QueryDrives** o richiamando il metodo [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) e passando il bus e il numero di slot desiderati. Con un oggetto unità, è possibile impostare lo stato dell'unità ed eseguire query per le proprietà dell'unità, gli extent di unità associati e il sottosistema contenente l'unità.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto unità includono lo stato, l'integrità e i flag dell'unità. dimensioni in byte; e un bus e un numero di slot.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Interfacce che possono essere esposte da questo oggetto     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Enumerazioni associate                           | [**VDS \_ FLAG \_ DI UNITÀ**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), STATO [**\_ UNITÀ VDS \_**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)ED [**\_ \_ EXTENT UNITÀ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Strutture associate                             | [**VDS \_ NOTIFICA \_ DI DRIVE PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) e [**VDS \_ DRIVE \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
