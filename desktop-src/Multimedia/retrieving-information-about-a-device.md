---
title: Recupero di informazioni su un dispositivo
description: Recupero di informazioni su un dispositivo
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS comando
- MCI_STATUS comando
- MCI_INFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412ccfb8819ac1c76cd3f0114fa114c877280de959f605535fd4bb83d224a91e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689091"
---
# <a name="retrieving-information-about-a-device"></a>Recupero di informazioni su un dispositivo

Ogni dispositivo risponde [](capability.md) alla funzionalità [**(MCI \_ GETDEVCAPS),**](mci-getdevcaps.md) [**allo**](status.md) stato [**(STATO MCI) \_**](mci-status.md)e alle [**informazioni**](info.md) [**(MCI \_ INFO).**](mci-info.md) Questi comandi ottengono informazioni sul dispositivo. Ad esempio, il comando seguente restituisce "true" se un **dispositivo cdaudio** può espulso il disco:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



I flag elencati per i comandi obbligatori e di base forniscono una quantità minima di informazioni su un dispositivo. Molti dispositivi integrano i comandi obbligatori e di base con i flag estesi per fornire informazioni aggiuntive sul dispositivo.

 

 




