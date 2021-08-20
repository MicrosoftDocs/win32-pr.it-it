---
title: Enumerazione dei driver di acquisizione installati
description: Enumerazione dei driver di acquisizione installati
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- Funzione capGetDriverDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8fe85103259354bcc3b42834ecaff03d660eb408cda8191e5e0abea7393d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988650"
---
# <a name="enumerating-installed-capture-drivers"></a>Enumerazione dei driver di acquisizione installati

Nell'esempio seguente viene utilizzata [**la funzione capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) per ottenere i nomi e le versioni dei driver di acquisizione installati.


```C++
char szDeviceName[80];
char szDeviceVersion[80];

for (wIndex = 0; wIndex < 10; wIndex++) 
{
    if (capGetDriverDescription(
            wIndex, 
            szDeviceName, 
            sizeof (szDeviceName), 
            szDeviceVersion, 
            sizeof (szDeviceVersion)
        )) 
    {
        // Append name to list of installed capture drivers
        // and then let the user select a driver to use.
    }
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




