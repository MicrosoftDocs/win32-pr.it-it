---
description: I provider di hardware implementano le interfacce IVssProviderCreateSnapshotSet e IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Sviluppo di provider di hardware VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29533838b814a07f3da5310302a283f6cd60dc75779b4eb29dcdbf6b10816aa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032711"
---
# <a name="developing-vss-hardware-providers"></a>Sviluppo di provider di hardware VSS

I provider di hardware implementano le interfacce [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) e [**IVssHardwareSnapshotProvider.**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) **IVssProviderCreateSnapshotSet implementa** la sequenziazione dello stato della copia shadow. **IVssHardwareSnapshotProvider** opera su un'astrazione LUN. I provider devono essere implementati come server COM out-of-process. I provider usano meccanismi specifici del provider (spesso IOCL privati) per comunicare con il sottosistema di archiviazione che crea un'istanza dei LUN della copia shadow.

-   [Registrazione e caricamento del provider di copie shadow](shadow-copy-provider-registration-and-loading.md)
-   [Creazione della copia shadow per i provider](shadow-copy-creation-for-providers.md)
-   [Interazioni e comportamenti del provider di hardware](hardware-provider-interactions-and-behaviors.md)

 

 



