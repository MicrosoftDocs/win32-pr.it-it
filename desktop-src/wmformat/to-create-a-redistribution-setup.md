---
title: Per creare una configurazione di ridistribuzione
description: Per creare una configurazione di ridistribuzione
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media Format SDK, ridistribuzione software
- ASF (Advanced Systems Format), ridistribuzione del software
- ASF (formato avanzato dei sistemi), ridistribuzione del software
- Windows Media Format SDK, ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ASF (formato avanzato dei sistemi), ridistribuzione
- ridistribuzione del software, creazione
- ridistribuzione del software, WMFDist.exe
- ridistribuzione, creazione
- ridistribuzione, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221360"
---
# <a name="to-create-a-redistribution-setup"></a>Per creare una configurazione di ridistribuzione

1.  Chiedere alla routine di installazione di installare i file dell'applicazione e apportare le impostazioni necessarie prima di richiamare il pacchetto di ridistribuzione.
2.  Installare WMFDist.exe. È possibile utilizzare il flag/Q: a per eseguire un'installazione automatica e non interattiva ed escludere l'interfaccia utente della configurazione di ridistribuzione durante l'installazione dell'applicazione. La routine deve quindi rilevare se il riavvio è necessario alla fine.

    Ad esempio:

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione del software**](software-redistribution.md)
</dt> </dl>

 

 




