---
description: Oggetto porta controller
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Oggetto porta controller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306510"
---
# <a name="controller-port-object"></a>Oggetto porta controller

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto porta del controller modella una porta del controller in un sottosistema. I computer host possono scrivere e leggere da lun attraverso le porte del controller. Le porte del controller sono contenute nei controller di un sottosistema. In VDS 1,1 e VDS 2.0, ognuna delle porte del controller di un sottosistema è impostata su attivo o inattivo in relazione a ogni LUN del sottosistema. Una singola porta del controller, quindi, può essere impostata contemporaneamente su attivo per un LUN e inattivo per altri. Una porta del controller attiva per un determinato LUN ha la responsabilità di gestire l'input e l'output del LUN.

Le porte del controller attive vengono utilizzate come uno degli endpoint dei percorsi MPIO in Fibre Channel provider di hardware, su cui è possibile imporre i criteri di bilanciamento del carico.

Usare il metodo [**IVdsControllerControllerPort:: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) per determinare le porte del controller contenute in un controller specifico. I chiamanti possono ottenere un puntatore a una porta del controller specifica selezionando l'oggetto porta del controller desiderato dall'enumerazione restituita dal metodo **QueryControllerPorts** . Con un oggetto controller, un chiamante può impostare lo stato della porta del controller e la query per i LUN associati.

Le proprietà dell'oggetto controller includono un identificatore di oggetto, un nome, un numero di serie e lo stato della porta del controller.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                              | Elemento                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto in VDS 1,1 e 2,0 Fibre Channel solo provider | [**IVdsControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| Enumerazioni associate                                                                           | [**\_stato porta \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| Strutture associate                                                                             | [**VDS \_ Notifica \_ della porta e della porta**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) [ **VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
