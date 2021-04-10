---
description: Oggetto unità
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Oggetto unità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231681"
---
# <a name="drive-object"></a>Oggetto unità

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto unità modella un'unità disco fisica che è contenuta all'interno di un sottosistema. Ogni unità si connette a un bus, occupa uno slot e contiene un set di extent di unità. Ogni unità può contribuire a un numero qualsiasi di lun. Un'unità può anche essere designata come riserva a caldo.

Usare il metodo [**IVdsSubSystem:: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) per determinare le unità contenute in un sottosistema specifico. I chiamanti possono ottenere un puntatore a un'unità specifica selezionando l'oggetto unità desiderato dall'enumerazione restituita dal metodo **QueryDrives** oppure richiamando il metodo [**IVdsSubSystem:: getdrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) e passando il bus e il numero di slot desiderati. Con un oggetto unità è possibile impostare lo stato dell'unità e la query per le proprietà dell'unità, gli extent di unità associati e il sottosistema che contiene l'unità.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto unità includono lo stato dell'unità, l'integrità e i flag. dimensioni in byte; e un bus e un numero di slot.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Interfacce che possono essere esposte da questo oggetto     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Enumerazioni associate                           | [**VDS \_ \_Flag unità**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ stato unità VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)e [**\_ \_ extent unità VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Strutture associate                             | [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) [**\_ \_ Notifica**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)dell'unità prop e VDS.                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem:: getdrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
