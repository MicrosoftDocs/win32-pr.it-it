---
title: Recupero delle informazioni sul sistema MCI
description: Recupero delle informazioni sul sistema MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Comando MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955372"
---
# <a name="obtaining-mci-system-information"></a><span data-ttu-id="d6770-104">Recupero delle informazioni sul sistema MCI</span><span class="sxs-lookup"><span data-stu-id="d6770-104">Obtaining MCI System Information</span></span>

<span data-ttu-id="d6770-105">Il comando [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) ottiene informazioni di sistema sui dispositivi MCI.</span><span class="sxs-lookup"><span data-stu-id="d6770-105">The [sysinfo](sysinfo.md) ([**MCI\_SYSINFO**](mci-sysinfo.md)) command obtains system information about MCI devices.</span></span> <span data-ttu-id="d6770-106">MCI gestisce questo comando senza inoltrarlo a un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d6770-106">MCI handles this command without relaying it to any MCI device.</span></span> <span data-ttu-id="d6770-107">Per l'interfaccia del messaggio di comando, MCI restituisce le informazioni di sistema nella struttura [**\_ \_ parametri di MCI sysinfo**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d6770-107">For the command-message interface, MCI returns the system information in the [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

<span data-ttu-id="d6770-108">È possibile usare il comando **sysinfo** (MCI \_ sysinfo) per recuperare informazioni come il numero di dispositivi MCI in un sistema, il numero di dispositivi MCI di un determinato tipo, il numero di dispositivi Open MCI e i nomi dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d6770-108">You can use the **sysinfo** (MCI\_SYSINFO) command to retrieve information such as the number of MCI devices on a system, the number of MCI devices of a particular type, the number of open MCI devices, and the names of the devices.</span></span> <span data-ttu-id="d6770-109">Questo comando viene spesso chiamato più di una volta per recuperare una particolare informazione.</span><span class="sxs-lookup"><span data-stu-id="d6770-109">This command is often called more than once to retrieve a particular piece of information.</span></span> <span data-ttu-id="d6770-110">Ad esempio, è possibile recuperare il numero di dispositivi di un determinato tipo nella prima chiamata, quindi enumerare i nomi dei dispositivi nella successiva.</span><span class="sxs-lookup"><span data-stu-id="d6770-110">For example, you might retrieve the number of devices of a particular type in the first call and then enumerate the names of the devices in the next.</span></span>

 

 




