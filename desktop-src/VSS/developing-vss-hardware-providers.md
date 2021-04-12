---
description: I provider hardware implementano le interfacce IVssProviderCreateSnapshotSet e IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Sviluppo di provider hardware VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233827"
---
# <a name="developing-vss-hardware-providers"></a>Sviluppo di provider hardware VSS

I provider hardware implementano le interfacce [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) e [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) . **IVssProviderCreateSnapshotSet** implementa la sequenziazione dello stato della copia shadow. **IVssHardwareSnapshotProvider** opera su un'astrazione lun. I provider devono essere implementati come server COM out-of-process. I provider usano meccanismi specifici del provider (spesso IOCTL privati) per comunicare con il sottosistema di archiviazione che crea un'istanza dei lun delle copie shadow.

-   [Registrazione e caricamento del provider di copie shadow](shadow-copy-provider-registration-and-loading.md)
-   [Creazione di copie shadow per i provider](shadow-copy-creation-for-providers.md)
-   [Interazioni e comportamenti del provider hardware](hardware-provider-interactions-and-behaviors.md)

 

 



