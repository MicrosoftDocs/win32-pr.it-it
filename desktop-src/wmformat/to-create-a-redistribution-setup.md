---
title: Per creare un'installazione di ridistribuzione
description: Per creare un'installazione di ridistribuzione
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media Format SDK, ridistribuzione del software
- Advanced Systems Format (ASF), ridistribuzione del software
- ASF (Advanced Systems Format), ridistribuzione del software
- Windows MEDIA Format SDK, ridistribuzione
- Advanced Systems Format (ASF), ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ridistribuzione del software, creazione
- ridistribuzione del software,WMFDist.exe
- ridistribuzione, creazione
- ridistribuzione, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb26b63a2379a72e2d97df876d91d8c57a6da9249c4e40525e81edacaf86542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027299"
---
# <a name="to-create-a-redistribution-setup"></a>Per creare un'installazione di ridistribuzione

1.  Fare in modo che la routine di installazione installi i file dell'applicazione e apportare le impostazioni necessarie prima di richiamare il pacchetto di ridistribuzione.
2.  Installare WMFDist.exe. È possibile usare il flag /Q:A per eseguire un'installazione automatica e non interattiva ed eliminare l'interfaccia utente dell'installazione di ridistribuzione durante l'installazione dell'applicazione. La routine deve quindi rilevare se il riavvio è necessario alla fine.

    Esempio:

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione del software**](software-redistribution.md)
</dt> </dl>

 

 




