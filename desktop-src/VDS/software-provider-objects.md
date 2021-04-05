---
description: Oggetti provider di software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Oggetti provider di software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "103885895"
---
# <a name="software-provider-objects"></a>Oggetti provider di software

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Gli oggetti del provider di software modellano i dispositivi fisici, ad esempio dischi IDE e CD-ROM, ed elementi virtuali come pacchetti, volumi e Plex del volume. Nella figura seguente viene illustrata la relazione tra l'oggetto provider e il set di oggetti provider software, nonché la relazione tra i vari oggetti provider di software.

![Diagramma che mostra la relazione tra gli oggetti ' provider ' e provider software, ad esempio ' Pack ' è volume '.](images/vdsswobjects.png)

Un oggetto provider può contenere zero o più pacchetti. Un oggetto Pack può contenere zero o più dischi e volumi. Un volume è costituito da almeno un plex del volume e ogni volume Plex può essere mappato a uno o più dischi, a seconda del tipo di Plex. VDS gestisce i dischi non allocati direttamente, senza un contenitore Pack. Gli argomenti rimanenti di questa sezione descrivono gli oggetti Pack, disk, volume e Plex del volume.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> </dl>

 

 
