---
description: Controller (oggetto)
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Controller (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104558103"
---
# <a name="controller-object"></a>Controller (oggetto)

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto controller modella un controller in un sottosistema. I controller sono contenuti in sottosistemi e ogni controller dispone di una o più porte del controller attraverso le quali il computer host può scrivere e leggere da lun. Un singolo controller può essere impostato contemporaneamente su attivo per un LUN e inattivo per altri. Un controller attivo per un LUN specificato ha la responsabilità di gestire l'input e l'output del LUN. Questa idea è illustrata nella figura seguente.

![Diagramma che mostra un "controller" con un LUN attivo a sinistra e due LUN attivi a destra.](images/vdscontroller.png)

**VDS 1,0:** Ognuno dei controller di un sottosistema è impostato su attivo o inattivo in relazione a ogni LUN del sottosistema.

Le applicazioni VDS usano il metodo [**IVdsSubSystem:: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) per determinare i controller contenuti in un sottosistema specifico. I chiamanti possono ottenere un puntatore a un controller specifico selezionando l'oggetto controller desiderato dall'enumerazione restituita dal metodo **QueryControllers** . Con un oggetto controller, un chiamante può impostare lo stato del controller, eseguire una query per i LUN associati, eseguire una query per le porte del controller e scaricare e invalidare la cache.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto controller includono lo stato e l'integrità del controller e un conteggio delle porte.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                              | Elemento                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                                                 | [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| Interfacce sempre esposte da questo oggetto in VDS 1,1 e 2,0 Fibre Channel solo provider | [**IVdsControllerControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| Interfacce che possono essere esposte da questo oggetto                                                     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| Enumerazioni associate                                                                           | [**VDS \_ \_stato del controller**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).                                                                      |
| Strutture associate                                                                             | [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) Notifiche del controller prop e del [**\_ controller \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
