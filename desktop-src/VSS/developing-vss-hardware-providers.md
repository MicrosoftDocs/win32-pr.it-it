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
# <a name="developing-vss-hardware-providers"></a><span data-ttu-id="5dfc6-103">Sviluppo di provider hardware VSS</span><span class="sxs-lookup"><span data-stu-id="5dfc6-103">Developing VSS Hardware Providers</span></span>

<span data-ttu-id="5dfc6-104">I provider hardware implementano le interfacce [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) e [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) .</span><span class="sxs-lookup"><span data-stu-id="5dfc6-104">Hardware providers implement the [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) and [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) interfaces.</span></span> <span data-ttu-id="5dfc6-105">**IVssProviderCreateSnapshotSet** implementa la sequenziazione dello stato della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="5dfc6-105">**IVssProviderCreateSnapshotSet** implements the shadow copy state sequencing.</span></span> <span data-ttu-id="5dfc6-106">**IVssHardwareSnapshotProvider** opera su un'astrazione lun.</span><span class="sxs-lookup"><span data-stu-id="5dfc6-106">**IVssHardwareSnapshotProvider** operates on a LUN abstraction.</span></span> <span data-ttu-id="5dfc6-107">I provider devono essere implementati come server COM out-of-process.</span><span class="sxs-lookup"><span data-stu-id="5dfc6-107">Providers must be implemented as an out-of-process COM server.</span></span> <span data-ttu-id="5dfc6-108">I provider usano meccanismi specifici del provider (spesso IOCTL privati) per comunicare con il sottosistema di archiviazione che crea un'istanza dei lun delle copie shadow.</span><span class="sxs-lookup"><span data-stu-id="5dfc6-108">Providers use provider-specific mechanisms (often private IOCTLs) to communicate with the storage subsystem that instantiates the shadow copy LUNs.</span></span>

-   [<span data-ttu-id="5dfc6-109">Registrazione e caricamento del provider di copie shadow</span><span class="sxs-lookup"><span data-stu-id="5dfc6-109">Shadow Copy Provider Registration and Loading</span></span>](shadow-copy-provider-registration-and-loading.md)
-   [<span data-ttu-id="5dfc6-110">Creazione di copie shadow per i provider</span><span class="sxs-lookup"><span data-stu-id="5dfc6-110">Shadow Copy Creation for Providers</span></span>](shadow-copy-creation-for-providers.md)
-   [<span data-ttu-id="5dfc6-111">Interazioni e comportamenti del provider hardware</span><span class="sxs-lookup"><span data-stu-id="5dfc6-111">Hardware Provider Interactions and Behaviors</span></span>](hardware-provider-interactions-and-behaviors.md)

 

 



