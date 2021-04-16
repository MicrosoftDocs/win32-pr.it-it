---
description: Oggetto sottosistema
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Oggetto sottosistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550183"
---
# <a name="subsystem-object"></a>Oggetto sottosistema

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto del sottosistema modella un sottosistema di archiviazione. Un sottosistema è un'enclosure RAID o una scheda RAID PCI. Un singolo computer host può essere connesso a un numero qualsiasi di sottosistemi. Ogni sottosistema è gestito da un solo provider hardware. In una configurazione SAN la classe del sottosistema rappresenta un'enclosure di archiviazione SAN.

Un sottosistema può contenere un numero qualsiasi di controller e unità e può rendere visibile (annullare il mascheramento) un numero qualsiasi di lun nel computer in cui è in esecuzione il provider hardware. I sottosistemi di fascia superiore possono annullare il mascheramento dei LUN in altri computer della rete. Ogni unità disco all'interno di un sottosistema è connessa a un bus e occupa uno slot del bus. Ogni controller all'interno di un sottosistema dispone di una o più porte del controller.

L'illustrazione seguente mostra i dispositivi fisici contenuti in un sottosistema (i LUN non vengono visualizzati) e le relazioni tra di essi.

![Diagramma che mostra un sottosistema che inizia con "Ports" a sinistra, che passa a "Controllers" e quindi a "bus" con "slot" che portano a singole "unità".](images/vdssubsystem.png)

Le applicazioni VDS usano il metodo [**IVdsHwProvider:: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) per eseguire query sui sottosistemi che appartengono a un provider hardware specifico. I chiamanti possono ottenere un puntatore a un sottosistema specifico selezionando l'oggetto del sottosistema desiderato dall'enumerazione restituita dal metodo **QuerySubSystems** . Con un oggetto sottosistema è possibile impostare lo stato del sottosistema, creare lun, sostituire unità ed eseguire query per controller, unità e lun.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto sottosistema includono lo stato, l'integrità e i flag del sottosistema. numero di controller, slot e bus; e un'impostazione della priorità di ricompilazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0 | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) e [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Interfacce che possono essere esposte da questo oggetto                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) e [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Enumerazioni associate                                                                   | [**VDS \_ \_ \_ Flag del sottosistema**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) e [**\_ \_ \_ stato del sottosistema VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Strutture associate                                                                     | [**VDS \_ Sottosistema \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) e [**\_ \_ \_ notifica del sottosistema VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
