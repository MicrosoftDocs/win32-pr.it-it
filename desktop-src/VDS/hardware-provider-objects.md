---
description: Oggetti provider hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Oggetti provider hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c0050b6a9754b25b6a5027d9470cb2fc46911bf4ab3ef852454d1f0698a1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125966"
---
# <a name="hardware-provider-objects"></a>Oggetti provider hardware

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Il modello a oggetti VDS include un set di oggetti per eseguire query e configurare entità del provider hardware. Si noti che anche se VDS include un provider di software, è necessario acquistare separatamente un provider hardware e l'hardware associato per sfruttare i vantaggi degli oggetti provider di hardware. Questi oggetti provider di hardware rappresentano dispositivi fisici (ad esempio sottosistemi, unità e controller) e dispositivi virtuali (ad esempio LUN e plex LUN).

Un provider hardware deve creare un oggetto COM per ogni dispositivo fisico o virtuale.

La figura seguente illustra la relazione tra l'oggetto provider e il set di oggetti provider hardware, nonché la relazione tra i vari oggetti provider hardware stessi.

![Diagramma che mostra la relazione tra 'Provider' e 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive' e 'Spindle'. ](images/vdshwobjects.png)

Un oggetto provider può contenere un numero qualsiasi di sottosistemi. Tutti i provider hardware sono in grado di gestire più istanze dello stesso modello di sottosistema. Molti provider di hardware sono anche in grado di gestire più istanze di modelli di sottosistema diversi. Un singolo computer può ospitare un numero qualsiasi di provider di hardware.

Un oggetto sottosistema può contenere un numero qualsiasi di controller e unità e può visualizzare qualsiasi numero di LUN. Un oggetto LUN è costituito da almeno un plex LUN e ogni lun plex esegue il mapping a una o più unità, a seconda del tipo di plex. Gli oggetti controller possono gestire l'input/output dei dati per un numero qualsiasi di oggetti LUN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> </dl>

 

 
