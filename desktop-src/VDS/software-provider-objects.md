---
description: Oggetti provider software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Oggetti provider software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507abb00b67b51ad68eb0592ff4fa7b5201cff5be0587b7170662556238feb50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137159"
---
# <a name="software-provider-objects"></a>Oggetti provider software

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Gli oggetti del provider software modellano dispositivi fisici, ad esempio dischi IDE e CD-ROM, ed elementi virtuali come pacchetti, volumi e plex di volumi. Nella figura seguente viene illustrata la relazione tra l'oggetto provider e il set di oggetti provider software, nonché la relazione tra i vari oggetti provider software stessi.

![Diagramma che mostra la relazione tra un 'Provider' e gli oggetti provider software, ad esempio 'Pack' e 'Volume'.](images/vdsswobjects.png)

Un oggetto provider può contenere zero o più pacchetti. Un oggetto pack può contenere zero o più dischi e volumi. Un volume è costituito da almeno un volume plex e ogni volume plex può essere mappato a uno o più dischi, a seconda del tipo di plex. VDS gestisce direttamente i dischi non allocati, senza un contenitore pack. Gli argomenti rimanenti di questa sezione descrivono gli oggetti pack, disk, volume e volume plex.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> </dl>

 

 
