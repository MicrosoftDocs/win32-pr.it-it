---
description: Oggetto sottosistema
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Oggetto sottosistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af9837da90497b07d133362c0a61549a63665f2c75d4c97b2d07369e4589fa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603151"
---
# <a name="subsystem-object"></a>Oggetto sottosistema

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un sottosistema a oggetti modella un sottosistema di archiviazione. Un sottosistema è uno chassis RAID o una scheda RAID PCI. Un singolo computer host può essere connesso a un numero qualsiasi di sottosistemi. Ogni sottosistema è gestito esattamente da un provider di hardware. In una configurazione SAN, la classe del sottosistema rappresenta un'enclosure di archiviazione SAN.

Un sottosistema può contenere un numero qualsiasi di controller e unità e può visualizzare (annullare il mascheramento) qualsiasi numero di LUN nel computer in cui è in esecuzione il provider hardware. I sottosistemi di fascia superiore possono annullare il mascheramento dei LUN ad altri computer della rete. Ogni unità disco all'interno di un sottosistema è connessa a un bus e occupa uno slot nel bus. Ogni controller all'interno di un sottosistema ha una o più porte del controller.

La figura seguente mostra i dispositivi fisici contenuti in un sottosistema (i LUN non vengono visualizzati) e le relazioni tra di essi.

![Diagramma che mostra un sottosistema che inizia con "Porte" a sinistra, passando a "Controller" e quindi a "Bus" con "Slot" che porta a singole "unità".](images/vdssubsystem.png)

Le applicazioni VDS usano il metodo [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) per eseguire query nei sottosistemi che appartengono a un provider hardware specifico. I chiamanti possono ottenere un puntatore a un sottosistema specifico selezionando l'oggetto sottosistema desiderato dall'enumerazione restituita dal **metodo QuerySubSystems.** Con un oggetto sottosistema è possibile impostare lo stato del sottosistema, creare LUN, sostituire unità ed eseguire query per controller, unità e LUN.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà degli oggetti del sottosistema includono lo stato, l'integrità e i flag del sottosistema. conteggio di controller, slot e bus; e un'impostazione di priorità di ricompilazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Interfacce sempre esposte da questo oggetto solo nei provider iSCSI VDS 1.1 e 2.0 | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) e [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Interfacce che possono essere esposte da questo oggetto                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) e [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Enumerazioni associate                                                                   | [**VDS \_ SUB \_ SYSTEM \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) e [**VDS SUB SYSTEM \_ \_ \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Strutture associate                                                                     | [**VDS \_ SUB \_ SYSTEM \_ PROP e**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) [**VDS SUB SYSTEM \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
