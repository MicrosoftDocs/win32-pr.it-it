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
# <a name="retrieving-information-about-a-device"></a>Recupero di informazioni su un dispositivo

Ogni dispositivo risponde ai comandi [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**\_ stato MCI**](mci-status.md)) e [**info**](info.md) ([**\_ informazioni MCI**](mci-info.md)). Questi comandi ottengono informazioni sul dispositivo. Ad esempio, il comando seguente restituisce "true" Se un dispositivo **CDAudio** può espellere il disco:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



I flag elencati per i comandi required e Basic forniscono una quantità minima di informazioni su un dispositivo. Molti dispositivi integrano i comandi obbligatori e di base con i flag estesi per fornire informazioni aggiuntive sul dispositivo.

 

 




