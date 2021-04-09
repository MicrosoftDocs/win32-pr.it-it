---
title: Recupero di informazioni su un dispositivo
description: Recupero di informazioni su un dispositivo
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- Comando MCI_GETDEVCAPS
- Comando MCI_STATUS
- Comando MCI_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955792"
---
# <a name="retrieving-information-about-a-device"></a><span data-ttu-id="a28c3-106">Recupero di informazioni su un dispositivo</span><span class="sxs-lookup"><span data-stu-id="a28c3-106">Retrieving Information About a Device</span></span>

<span data-ttu-id="a28c3-107">Ogni dispositivo risponde ai comandi [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**\_ stato MCI**](mci-status.md)) e [**info**](info.md) ([**\_ informazioni MCI**](mci-info.md)).</span><span class="sxs-lookup"><span data-stu-id="a28c3-107">Every device responds to the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)), and [**info**](info.md) ([**MCI\_INFO**](mci-info.md)) commands.</span></span> <span data-ttu-id="a28c3-108">Questi comandi ottengono informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a28c3-108">These commands obtain information about the device.</span></span> <span data-ttu-id="a28c3-109">Ad esempio, il comando seguente restituisce "true" Se un dispositivo **CDAudio** può espellere il disco:</span><span class="sxs-lookup"><span data-stu-id="a28c3-109">For example, the following command returns "true" if a **cdaudio** device can eject the disc:</span></span>


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="a28c3-110">I flag elencati per i comandi required e Basic forniscono una quantità minima di informazioni su un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a28c3-110">The flags listed for the required and basic commands provide a minimum amount of information about a device.</span></span> <span data-ttu-id="a28c3-111">Molti dispositivi integrano i comandi obbligatori e di base con i flag estesi per fornire informazioni aggiuntive sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a28c3-111">Many devices supplement the required and basic commands with extended flags to provide additional information about the device.</span></span>

 

 




