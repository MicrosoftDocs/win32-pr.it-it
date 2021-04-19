---
description: Oggetti provider hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Oggetti provider hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320217"
---
# <a name="hardware-provider-objects"></a>Oggetti provider hardware

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Il modello a oggetti VDS include un set di oggetti per eseguire query e configurare le entità del provider hardware. Si noti che mentre VDS include un provider di software, è necessario acquistare un provider hardware e l'hardware associato separatamente per sfruttare i vantaggi degli oggetti provider hardware. Questi oggetti provider hardware rappresentano i dispositivi fisici (ad esempio, sottosistemi, unità e controller) e i dispositivi virtuali, ad esempio lun e i PLEX LUN.

Un provider hardware deve creare un oggetto COM per ogni dispositivo fisico o virtuale.

Nell'illustrazione seguente viene illustrata la relazione tra l'oggetto provider e il set di oggetti provider hardware, nonché la relazione tra i vari oggetti provider hardware.

![Diagramma che mostra la relazione tra' provider ' è Subsystem ',' controller ',' LUN ',' LUN Plex ',' drive ' è mandrino '. ](images/vdshwobjects.png)

Un oggetto provider può contenere un numero qualsiasi di sottosistemi. Tutti i provider hardware sono in grado di gestire più istanze dello stesso modello di sottosistema. Molti provider di hardware sono inoltre in grado di gestire più istanze di modelli di sottosistema diversi. Un singolo computer può ospitare un numero qualsiasi di provider hardware.

Un oggetto sottosistema può contenere un numero qualsiasi di controller e unità e può presentare un numero qualsiasi di lun. Un oggetto LUN è costituito da almeno un PLEX LUN e ogni PLEX LUN esegue il mapping a una o più unità, a seconda del tipo di Plex. Gli oggetti controller possono gestire l'input/output dei dati per qualsiasi numero di oggetti LUN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> </dl>

 

 
